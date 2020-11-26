communication between os kernel and os processes
ctrl+c creates a kill signal

kill -TERM pid


Signal is the notification sent to a process that some event has occurred in the system

Signal is an event for which a process will register with the os so that whenever those events happens they are Redirected to the process for handling. Signals can also be used for inter process communication using which one process can send signal to other process. Signals are asynchronous
