Info leaks is command in gdb to get leak information.


So if we have to detect memory leak without valgrind we have to do either of the following


Use gdb where u can write a script so that the u can break point at the malloc and free to print the allocated memory and free memory addresses. Later on compare.