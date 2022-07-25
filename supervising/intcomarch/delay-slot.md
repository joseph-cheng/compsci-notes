Delay slots occur in non-[[interlocked-hardware|interlocked hardware]]. There are two kinds of delay slot: a **branch delay slot** and a **load delay slot**. In essence, delay slots are locations where hazards will not be automatically avoided by the processor.

# Branch delay slots
Suppose we have the following code:

```asm
1: CMP r0, r1
2: BEQ my_label
3: ????
...
my_label:
...
```

Depending on our hardware, we might have some branch delay slots (e.g. MIPS has a single branch delay slot). If we have $n$ branch delay slots, then the next $n$ instructions after a branch will always be executed, *regardless* of the outcome of the branch. If no independent instructions can be found to fill the delay slots, the programmer/compiler should fill the slots with [[no-op|no-ops]].

Branch delay slots occur due to [[pipelining]]. Often, fetching an instruction and decoding an instruction are in separate pipeline stages. This means that when we fetch a branch instruction, we can only know it is a branch instruction in the decode stage, at which point another instruction will be in the fetch stage, which is the instruction in the delay slot.

# Load delay slots
Load delay slots occur again in non-[[interlocked-hardware|interlocked hardware]] because of the [[load-use-delay|load-use delay]].

Because of the load-use delay, the instruction directly following a load instruction will not have access to the just-loaded value.
