* Synchronization
* Mutual Exclusion
* Signalling


Mutual exclusion means that only a single thread should be able to access the shared resource at any given point of time. A thread should be able to execute a set of instructions atomically.


Synchronization means that you synchronize/order the access of multiple threads to the shared resource.

Signalling is required to indicate that a dependent work has been completed and further work can be started by someone else.

The thread that acquires the mutex is the only one that can release it

Recursive mutex is the one which once taken by a thread can be acquired again and again by the same thread not by the other thread.


Spin locks are better if the mutex is to be acquired again and again and for a very short duration. They keep checking in a loop if the mutex is available for accusition. Thus causing busy waiting.

Mutex serves the purpose of mutual exclusion.
