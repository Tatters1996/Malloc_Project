# Checkpoint 1 Work

 * 64-bit memory allocator based on implicit lists, no coalescing, and first-fit placement. 
 * Blocks must be aligned to 8 bytes bound. Minimum block size is 16 bytes.
 * Yanzhong Jiang's part is to implement mm_init, mm_malloc, and mm_checkheap.
 * Tomisin Salu's part is to implement the mm_free, and realloc functions.
 * Temporary disabled coalescing

# Final Submission Work

 * Yanzhong Jiang added explicit circular double linked list for finding fits, enabled coalescing again, and fixed code for bugs.
