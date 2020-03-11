DMA is no CPU at all. The device has programming interface that you can use and then device will directly copy the data to the destination. DMA is a controller in itself which is a special hardware unit that interfaces the main memory with the peripheral devices. DMA controller shares the memory bus with CPU.


In DMA it is required that u have contiguous physical memory else an mmu will be required. MMU is memory management unit


In dma the device can access the user space memory directly.

In dma the device will write in user space memory directly without the involvement of cpu. So dma controller will take care of this
the CPU instructions used to access the memory can also be used for accessing devices


To carry out an input, output or memory-to-memory operation, the host processor initializes the DMA controller with a count of the number of words to transfer, and the memory address to use. The CPU then commands peripheral device to initiate data transfer. The DMA controller then provides addresses and read/write control lines to the system memory. Each time a byte of data is ready to be transferred between the peripheral device and memory, the DMA controller increments its internal address register until the full block of data is transferred.