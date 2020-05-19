There are three ways to transfer the data:
1. Polling
2. Interrupt
3. DMA


Memory based data transfer in which no special CPU instructions are needed. Devices are considered as memory areas and same load store instructions can be used with device addresses

Now to transfer data from memory to device as per the program requirements the cpu has to execute some instructions. It has to issue load and store instructions to read from one address and store it in different address which can be device in case of memory mapped io. Now this process is extremely time consuming as the processor will continue to be occupied for reading every byte. Now to free up the CPU from this task this work of issuing load store instructions is given to DMA controller. After the DMA controller is done with its job the CPU is interrupted and CPU can resume the process function.

Now the transfer of data takes from kernel space to user space thus two copies of data. If we want the kernel space to be bypassed we can program our user software to directly access the device memory as an array. To do this we have mmap function that allows the user program to access the device memory. But device cannot accesa the user space memory. To enable reverse we have DMA



memory mapped io is that the user process can access the device as if it is a memory block. So all data that needs to be passed to the device is like writting to memory but actually this is getting written to device

Mapping of device means association of a range of user space addresses with the device memory. Whenever a program reads or writes to this address it is actually writing to the device

Without memory mapped io the user space has to interact with device via the kernel system calls and data is copied from kernel to user space. With this extra data buffer is not maintained in kernel. So directly user space buffer is accessed. Kernel still remains in communication via system calls. Processor will still be involved in transfering data from the memory to device


Port based io in which the processor has special instructions to instruct ports of device
