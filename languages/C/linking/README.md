It is the process of connecting all the object code (written by us and supporting libraries) to create an executable.

If the extern is used then depending upon linux and windows this definition has little different implementation
In the shared object there has to be one definition so windows give a compilation linking error because it is possible that at run time multiple processes using this shared object can provide definition of these variables so which one to use 

In linux the first definition is used and has to be used by other processes as well 