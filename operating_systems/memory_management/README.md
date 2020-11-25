echo 3 > /proc/sys/vm/drop_caches

 free –m

 df -h


cat /proc/meminfo

What is thrashing in os?
It occurs when there are lot of page faults happening. Page fault is that when the virtual address maps to a physical address that is not there in the main memory and hence a page swap is needed to bring that instruction into memory.