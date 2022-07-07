Most computers are von Neumann machines, where we have a CPU and memory unit (containing both instructions and data), where communication occurs through a shared bus.

This architecture gives rise to a problem known as the von Neumann bottleneck, which is that the speed of CPUs and memory rises much higher than the speed of the bus, so the CPU becomes bottlenecked by the bus.

To mitigate this effect, we use a [[memory-hierarchy|memory hierarchy]]. By separating instruction and data cache, we also make more of a [[harvard-architecture|Harvard architecture]].
