Zombie process is the one that has completed all its execution and all the system resources
associated with it have been released. But the process’s entry is still there in the process table.
This entry may be required by the parent process to read the exit status of the process.
To create a zombie process, the parent process shall not call the wait system call.
If the parent process has registered for signal SIG_IGN that is ignore signal, then the zombie
process will not be created and the child process will die after it completes execution.