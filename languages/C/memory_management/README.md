Use hooks for malloc and free so that we can catch the points of allocation and the addresses. Then from free we can match the same addresses if freed or not

Int *p = 100
Print %x, p

This means that the p is pointing to a location whose address is 100 . It is implementation dependent that if it will point to virtual address, physical address in stack, heap etc. not known 

How is Malloc internally implemented 
It is a user space function and it internally calls the system calls. It uses the sbrk and brk system calls. To move the fragments up and down. Mmap is a system call that will get the mapping of large memory chunk from device directly to the process that can now access this space like an array of bytes. So it does not have to do a read/write to/from user space to actual file. 