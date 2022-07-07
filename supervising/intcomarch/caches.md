Caching is storing a small portion of memory closer to the processor which is designed for low latency over high capacity. They are intended to exploit [[locality-of-reference|locality of reference]].

Caches are usually made using [[SRAM]] (whereas [[main-memory|main memory]] will be made using [[DRAM]]). We typically separate the first one or two levels into a [[split-cache|split cache]], having one cache for data and one cache for instructions.

[[cache-entry|Cache entries]] contain data in a 'cache line' or 'cache block'. Typically, these lines/blocks will be bigger than the [[word]] size, in order to reduce [[cache-misses|compulsory misses]].

When memory needs to be read, if it is not in the cache, it is fetched from lower down in the [[memory-hierarchy|memory hierarchy]]. A cache block is then chosen based on the [[cache-placement-policy|cache placement policy]]. If there is a free entry, it is used, and if not then we consult the [[cache-eviction-policy|cache eviction policy]] to choose an existing entry to be replaced. We may also use a [[victim-cache|victim cache]] in the case of eviction.

Caches may also be either [[write-through]] or [[write-back]].

#computer-architecture 
#caches




