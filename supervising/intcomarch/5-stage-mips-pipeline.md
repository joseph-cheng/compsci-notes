The classic 5-stage MIPS pipeline is widely studied in computer architecture classes as an introduction into [[pipelining]].

It has, as the name suggests, 5 stages:

 - Instruction Fetch (IF)
 - Instruction Decode and Register Fetch (ID/RF)
 - Execute (EX)
 - Memory Access (MA)
 - Register Writeback (WB)

In the IF stage, the [[instruction-cache|instruction cache]] is queried for the instruction, with address given by the [[program-counter|program counter]].

In the ID/RF stage, the instruction is decoded (i.e. we determine whether the instruction is an addition, branch, etc.) and simultaneously we fetch register operands from the [[register-file|register file]]. In the [[isa|instruction set architecture (ISA)]] we usually ensure that all instructions have their register parameters in the same location in the instruction encoding so that register fetch does not depend on register decode and we can really do them in parallel. If the instruction uses an immediate operand instead, then we can use a [[mux]] to select between the register value and the decoded immediate.

In the EX stage, we perform any arithmetic, e.g. if the instruction is an ADD then we will add the two operands together, or if it requires computation of an address (for load/store or branch target computation) then the address will be computed.

In the MA stage, we access memory if required, e.g. if it is a load/store instruction.

In the WB stage, we write back our results to the register file.

We can note that the placement of the the EX stage before the MA stage means that we can have instructions that access an offset to a base address, e.g. `lw r0 0x10(r1)` which loads 16 bytes after the address in `r1`. However, we cannot have instructions that load from an address and perform some computation on the value loaded in the same instruction. Interchanging the two stages would allow for this, but prevent the first type of instruction.

