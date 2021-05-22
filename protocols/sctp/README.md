Sctp uses 4 way hand shake in which the resources are allocated only when the handshake completes. In sctp the init message is responded back with a cookie which has to be sent back by the sender in the next message and then the resources are allocated.

In sctp multi homing is supported which means that multiple ip addresses each belonging to different subnets which means different routes  and be allocated to a host and all these addresses can be used to send data. This is mainly for network failure issues resolution so that the redundant path can be used.

In sctp there are multiple streams possible which means that more than one stream of data can be used to send data. Thus the head of the line blocking problem which means that till the time the current packet is  it sent successfully the subsequent packets cannot be sent.

Graceful shutdown is supported by sctp in which when the process is started both the parties cannot send and receive data.

