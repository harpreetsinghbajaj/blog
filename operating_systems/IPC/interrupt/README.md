communication between cpu and os kernel

What is a system call?
It is a way to get service from the operating system. When the application calls the system call the process changes to the kernel mode and then kernel executes the service and then returns the control back to the user space. When the system call is converted to assembly code then it is translated to the software interrupt using INT instruction. When the processor executes this it refers to the interrupt vector table and then executes the system call code.

System call is synchronous that is the user process will call the system call and let the os do it’s work. When that system call completes the process will come back to user space and function execution continues.

Hardware Interrupt is that simply means that the cpu has to stop doing what it is doing and start executing the routine corresponding to the interrupt that got generated. Now once the handling of this routine is complete the os  will schedule the process that it was working on at the time interrupt is generated.

Hardware interrupt comes as signal on the micro processor pins. Hardware interrupts are asynchronous which means that it can come anytime a process is being handled by processor.

Software interrupt is generated using an instruction INT 0X80 