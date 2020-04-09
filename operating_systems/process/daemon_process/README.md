Daemon process is the one that runs in the background. It is an intentional orphan process.
The daemon process is created by the parent process forking the child and then immediately
exiting so that the orphan child process gets adopted by the Unix’s init process
