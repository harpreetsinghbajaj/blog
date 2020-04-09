Orphan Process is the one whose parent had exited keeping the child process running. After the parent exits, the child process is adopted by the Unix’s init process.
This process has all its resources, memory space, etc available for its operation to continue. 
A process can be intentionally or unintentionally orphan. For intentional creation of orphan 
process, refer daemon process. Unintentional creation is possible if the parent process crashes.


