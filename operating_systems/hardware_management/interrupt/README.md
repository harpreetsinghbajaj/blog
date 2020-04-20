Software interrupt is a special instruction that tells the CPU to stop execute. This instruction is placed by the debugger in the binary at which the breakpoint is applied


To execute the system call the application software generates a 0x80 interrupt and place the arguments of the system call in process registers. Now processor will make the kernel to execute this system call