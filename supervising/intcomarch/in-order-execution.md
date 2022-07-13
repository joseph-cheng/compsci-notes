In-order execution refers to a property of the [[pipeline-stage|pipeline]] of a processor. In particular, a pipeline with in-order execution will only ever execute instructions in the order that they are issued.

Choosing a pipeline to be in-order simplifies its design, since we get a number of guarantees. For example, when handling [[precise-exceptions|precise exceptions]], we want to ensure that any instructions issued before the exception-causing instruction commit their results, and any issued after the exception-causing instruction do not. With an in-order pipeline, we can simply turn all the instructions earlier in the pipeline into [[no-op|no-ops]].

However, choosing a pipeline to be in-order limits the ILP that the processor can exploit.

For example, suppose we had an instruction stream like follows:

`1: lw r0, 0(r1)
`2: add r0, r0, r0`
`3: mul r5, r6 ,r7`

Instruction 2 depends on instruction 1, and due to the [[load-use-delay|load-use delay]], instruction 2 must stall for one cycle if it is scheduled immediately after instruction 1. Instruction 3, however, is independent from both other instructions, so an out-of-order processor would allow for instruction 3 to be scheduled after 1, but before 2, preventing instruction 2 from stalling.

It should be noted, however, that in-order pipelining does not make correctness trivial, there are still numerous [[hazards]] that can occur that require some work to avoid.

This design is contrasted with [[out-of-order-execution|out-of-order execution]], where it is permitted for instructions to overtake one another.