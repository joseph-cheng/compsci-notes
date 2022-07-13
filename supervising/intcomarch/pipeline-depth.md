In [[pipelining]], pipeline depth refers to how many stages a pipeline has. This depth has numerous consequences.

For example, by increasing the pipeline depth, we might be able to increase the clock frequency by reducing the length of the critical path.

There are limits to increasing pipeline depth, however, as it becomes progressively more difficult to split pipeline stages even smaller, especially if we need to preserve state through pipeline registers. These extra registers lead to higher power consumption. Furthermore, the overhead [[flip-flops|latching time ]] on the pipeline registers becomes relatively larger.

Furthermore, very long pipelines suffer worse from pipeline flushes (due to something like a [[branch-prediction|branch mispredict]] or other [[hazards]]), since more work has to be flushed from the pipeline.

This is why we have generally moved from very deep pipelines, like the 20-31 stages seen on the Pentium 4. The Pentium 4 [[micro-architecture]] actually had a target [[clock-frequency]] of 10GHz, which we have seen historically is unlikely to be an actually used clock frequency.

https://courses.engr.illinois.edu/ece411/fa2017/extra/optimum_pipelining.pdf