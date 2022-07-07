From Burks, Goldstine, and von Neumann: 

> Ideally one would desire an indefinitely large memory capacity such that any particular...[[word]] would be immediately available...We are...forced to recognize the possibility of constructing a hierarchy of memories, each of which has greater capacity than the preceding but which is less quickly accessible.

In order to mitigate the [[von-neumann-architecture|von Neumann]] bottleneck, we use a hierarchy of memories in order to increase throughput to the CPU. This takes place as [[caches|caching]].

We use a hierarchy of caches because, intrinsically, larger caches have higher latencies and higher power consumption per access. In order to get the lowest latency and lowest power consumption in the average case, we use a small cache, and then use progressively larger caches to increase the capacity of the hierarchy.


#computer-architecture 
#caches 


