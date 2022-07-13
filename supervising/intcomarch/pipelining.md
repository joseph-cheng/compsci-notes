Pipelining is a technique in computer architecture that aims to increase performance by reducing the length of the [[critical-path|critical path]] (and thus allowing for an increase in [[clock-frequency|clock frequency]]), as well as increasing [[instruction-level-parallelism|instruction-level parallelism]] by executing different parts of different instructions simultaneously. We might be fetching the arguments to one instruction, at the same time as performing arithmetic for another instruction, at the same time as accessing memory  for another instruction, for example.

Pipelines work by dividing the work into [[pipeline-stage|stages]].

The pipeline frequently studied in introduction to computer architecture classes is the [[5-stage-mips-pipeline|5-stage MIPS pipeline]].
