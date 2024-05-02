This project is a collabration between Yanzhong Jiang and Tomisin Salu

The project's goal is to build a dynamic storage allocator for C programs. 
The only file modified is mm.c.


# Following functions are implemented:
• bool mm init(void) - perform any necessary initializations, such as allocating the initial heap area
• void* malloc(size t size) - returns a pointer to an allocated block payload of at least size bytes
• void free(void* ptr) -  frees the block pointed to by ptr
• void* realloc(void* oldptr, size t size) - function returns a pointer to an allocated region of at least size bytes with the following constraints.
– if ptr is NULL, the call is equivalent to malloc(size);
– if size is equal to zero, the call is equivalent to free(ptr);
– if ptr is not NULL, it must have been returned by an earlier call to malloc, calloc, or realloc. 
• bool mm checkheap(int lineno) - check if memory heap is consistent


# First Version Work

 * 64-bit memory allocator based on implicit lists, no coalescing, and first-fit placement. 
 * Blocks must be aligned to 8 bytes bound. Minimum block size is 16 bytes.
 * Yanzhong Jiang's part is to implement mm_init, mm_malloc, and mm_checkheap.
 * Tomisin Salu's part is to implement the mm_free, and realloc functions.
 * Temporary disabled coalescing

# Final Version Work

 * Yanzhong Jiang added explicit circular double linked list for finding fits, enabled coalescing again, and fixed code for bugs.
