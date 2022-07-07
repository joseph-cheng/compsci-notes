Each entry in our cache looks like the following:

Tag|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Block&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Flags
----|--------|----

From a memory address, we form two new numbers: the **tag** and the **index**. The index is used to determine what [[cache-set|cache set]] a block should be in, and the cache tag is used to distinguish different blocks in the same set from another.

The **block** is the actual data from memory.

The **flags** are extra information about the block, for example a valid bit. We might also store [[cache-directory|directory]] information for directory-based [[cache-coherence|cache coherence]].

The cache block can be of a varying size, and may change depending on where in the [[memory-hierarchy|memory hierarchy]] the cache is. Larger block sizes can reduce [[cache-misses|compulsory misses]], but can increase [[cache-pollution|cache pollution]], reducing [[cache-hit-rate|hit rate]].

#computer-architecture 
#caches
