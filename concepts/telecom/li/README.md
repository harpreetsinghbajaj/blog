lawful interception is based on the standards 33107 and 33108. 

33107 defines the various interfaces involved in the LI architecture. These are x1_1 interfaces between the admf and node.

X2 interface is between the node and df2 and x3 is between the node and df3 

Df2 and df3 are further connected to li server via hi2 and hi3 interfaces.

X1_1 is for pushing the configuration of li to the node. The configuration includes the df2 ip and port df3 ip and port. Also list of identities for which the li has to be performed.

In the system there is a specific user only that will be able to use the li commands. So such user has to be configured via cli and need to be added to Linux system using add user command 

For every identity it has to be configured that if iri or/and cc is required.

Iri is the type of records that are sent over x2 interface and cc are record type that are sent over x3 interface

Iri events for eps were to be sent as part of our feature. Events are listed corresponding to selective messages.

Now the format in which the mesages need to be sent are defined by asn used by handover interfaces.