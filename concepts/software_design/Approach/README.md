To design a software, following are the three steps that are required:à

Define the problem and constraints:à Following are the techniques to achieve this:à


Write down question and answers on paper


Talk to the customer


Identify the minimum viable problem



Identify the possible solutions:à Following are the techniques to achieve this:à


Draw the UML diagram like sequence diagram, activity diagram, etc


Breaking down solution into blocks and defining the purpose of each block



Implementation of the solution:à Following are the techniques to achieve this:à


Test driven development


pair programming


Implement critical parts first


Implement end to end with some parts mocked or hardcoded


 By defining the problem we also mean that one shall be able to define the input and output of the system.
Identifying the possible solutions also mean that how the input will be tranformed to Output.
Possible solutions can be written using the pseudo code also.

 To implement the solution, there is a need to create code structure that can be easily understood and fits our requirements.
There are several design patterns that are available and proven in the industry to solve problems. We need to select one out of those.


Gaining more insight into the design of systems, following is the elaboration:à

Input and Output of system


what are the input parameters to the system?


What constraints are applicable on those inputs like space, processing, etc?


What are the use cases that we need to handle?


What are the type of inputs?


What is the expected output?


What is the format of output?



Work on breaking down the black box produced above into smaller components that will process the input variables and generate the output. This is called the

high level design:à

The smaller components will be some type of standard components like REST API processor, database, etc.


Some APIs that need to be provided.


Provide the interconnection between components like what protocol they shall use to communicate like TCP, UDP or a message queue.


Define the purpose of each box.


Also, here we can have sequence diagram for every use case that shows the interaction between various components created above.



Now design the core components created above. This means what code they shall have so that they can generate the output which act as input to the next component. Here u can create an activity diagram which will have the logic to generate the output.



There is a difference between the software design and architecture.

Software architecture is about creating the high level desing (the block diagram) of the software showing the components involved
and the interfaces between them.

Software design is about the object oriented modelling of the software showing how the code will be organized.

For either of the above, there are following steps to be performed:à

Requirement analysis. Clearly define the output of the software. For example:à


Display text on GUI


Store the file uploaded by user in databse



List down the inputs that will be given to create the output. For example:à


In #1.b, input will be a file uploaded by user

There can be situations where the input needs to be defined by you only. So whatever be the case, input is must.


Constraint analysis. Analayse the constraint along with which the software has to be created. For example:à


Cost


Time


Latency


Accuracy


Scalability



Now create an architecture. From input to the output, create a block diagram. Define the responsibility of every block and interation between them. For example:à


For #1.b, uploaded data will be accepted via interface which will then dump in to the database



For every block in the above diagram, check if any responsibility can be achieved via technology already available. For example:à


For #4.a, we can use mysql as database.



Selection in #5 shall statisfy the constraints imposed. For example:à


If constraint is cost, oracle DB cannot be selected.



After #5, focus on the blocks whose responsibilities that cannot be achieved via availabe technologies. Now work on designing them. For example:à


Creating APIs and setting up the protocol to be used by this component.



Calculate the performance of the above system. There shall be a familiarity with the speed of computer components like disk read write, RAM access, cache, etc


Work on scaling the system. For example:à


instantiate multiple instances using load balancer.


Spawn on demand using orchestrator in micro service architecture.


With the knowledge shared in the trailing email as base more readings from the internet helped in creating the above steps.

