communication between cpu and os kernel

What is a system call?
It is a way to get service from the operating system. When the application calls the system call the process changes to the kernel mode and then kernel executes the service and then returns the control back to the user space. When the system call is converted to assembly code then it is translated to the software interrupt using INT instruction. When the processor executes this it refers to the interrupt vector table and then executes the system call code. 