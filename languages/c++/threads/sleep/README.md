Sleep causes the threads to move into different states like idle, ready, etc. One queue is there for every state. Once the interrupts are send to OS kernel after regular intervals, it check the queues and take the relevant action.