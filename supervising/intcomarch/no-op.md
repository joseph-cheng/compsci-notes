A no-op (or NOP) is an instruction included in most (maybe every?) [[isa|instruction set]] that performs no action at all.

They have numerous uses:

  - In non-[[interlocked-hardware|interlocked hardware]], NOPs can be necessary if an independent instruction cannot be found to fill a [[delay-slot|delay slot]].
  - The processor may often convert an instruction in the [[pipelining|pipeline]] to a NOP in order to prevent it having any further side effects (e.g. if a branch was mispredicted). These are often called [[pipeline-bubble|pipeline bubbles]].