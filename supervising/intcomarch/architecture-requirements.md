Computers are needed in a variety of different circumstances, and the requirements for the architecture of this computer will be dictated by these circumstances.

For example, [[embedded]] or battery-powered devices will likely want low power consumption as a primary goal, as opposed to [[supercomputers]] that want high performance over anything else.

These goals lead to different design decisions. For example, embedded devices might opt for a processor with a simple [[scalar]] [[pipelining|pipeline]], with [[in-order-execution|in-order execution]], in order to maintain low power consumption. On the other hand, processors in desktop computers might opt for [[multiple-core]] designs [[superscalar]] pipelines.

We might have different [[memory-hierarchy|memory hierarchies]] for different purposes, for example [[cache-inclusion-policy|inclusive caches]] can simplify the [[cache-coherence]] protocol, but an [[cache-inclusion-policy|exclusive cache]] can increase the cache's effective capacity.

In the modern age, we often have [[system-on-chip|system-on-chips]] (SoCs),  which are "an ensemble of processors, memories, and interconnects tailored to an application domain". For example, a mobile phone will use an SoC that might contain specific [[accelerator|accelerators]] for video and audio codecs tailored to the hardware of the phone, [[heterogeneous]] cores, etc.

#computer-architecture 