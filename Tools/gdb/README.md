To print the first 100 bytes of the stack memory, use the command:
x/100xw $esp
To print all elements in the array, use the following commands:
set print array-indexes on 
set print elements 0 (0 means unlimited)
To check proc memory mappings, use the command:
info proc memory mapping
To dump the content in an address range, use the following commands:
dump memory out.log <start address> <end address>
strings out.log
To get the information of local variables in the stack frame, use the command:
info locals
To check the detail of threads:
info threads
To switch to a different thread context:
t <number of the thread>
To debug the case where a stack variable has been over written by some other variable follow the steps:
When that variable will be accessed there will be a problematic output.
In the GDB, check the proc memory mappings.
Analyse the content of process address space so that we can get an idea of what was the content at that time.
Analyse the stack area content byte by byte and try mapping the values with local variable values
To enable the formatted printing of structures on console, use the command:
set pretty print on
To set the logging of command and output to file also along with stdout, use the command:
set logging on
To print 100 bytes in a buffer, use the command:
x/100xb <buffer>
To print a value in hex format, use the command:
X variable
To print strings of long lengths completely, use the command:
set print elements 0

While debugging the production issue I received only a crash file from which a pcap files was created. It was very interesting to learn this and a great add on. Following are the steps to do this :-

 1. Print the entire buffer in hex format

2. Copy the output to a text file.

3. Replace the addresses with 0, 8, 10, 18, so on in the gap of 8.

4. Remove only 0x from every other value dumped in file.

5. Now execute the command text2pcap on this file.


6. Open the pcap in wireshark 