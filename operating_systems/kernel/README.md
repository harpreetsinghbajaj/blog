kernel code does not create segmentation faults

 To switch from user mode to kernel mode the system call is used. 

# Setup sctp in linux 
To setup sctp in linux kernel follow the following steps:—>
1. Install sctp devel using yum command 
2. Maybe there is requirement to install the sctkp tools 
3. Updatedb command to use locate 
4. Locate sctp.ko
5. If u find the above then sctp is installed 
6. Now to load follow the steps:—>
	1. Go to /etc/modprobe.d folder and check for sctp blacklist file
	2. Comment the line in this file
	3. Restart system
	4. Now perform mod probe sctp to load the module
	5. Check using command lsmod | grep sctp to see if its loaded 
7. Use the command
8. NC - - sctp -l 8080 to check if sctp socket can be opened.
9. Use net stat command to check the above port 