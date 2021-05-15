Request line is the first line in SIP request message. It has the method, SIP version and Request URI.

 Request URI is the URI of the User to which the request is destined. In register message, it will be the name of domain towards which the user wants to latch.
 
Status line is the first line in SIP response message. It has the response code and the protocol version
 
Some of the header fields are specific to either request or response SIP messages.
 
To header contains the username part of the Request URI. In case of Register message, the value of To header is the username of the Originating user who wants to register in the network.
 
From header is of the originator.
 
Call-Id header detects the dialogue in which multiple messages flow. If multiple register messages are sent out by the same UA then they must have the same call Id.
 
Cseq is the identifier of transactions that take place inside a dialogue.
 
Contact header specifies the other URIs that the UA client wants to be used by others for contacting it. For example:à different telephone numbers
 
Max-Forwards limit the number of hops a message can take to reach the destination.
 
Via header has the IP and transport protocol where the UAC is available to receive the SIP messages.
 
Record-Route is inserted by every proxy to force every future request in that dialogue to route via the same proxy. The entire list of record routes is sent to both the UAs and in every subsequent request and response this header is present.
 
In the response of SIP request, the from and to headers remain the same as those present in the Request.
 
To identify a dialogue, there is a need of call ID and the from and to tags. This is required so as to identify dialogues during SIP forking.
 
Route and Record-Route headers have the same thing but they occur in a different way. Record-Route header occurs only in the first transaction message of the dialogue and then in further transactions Route header will occur.
 
Service Route Header is the URI of the SCSCF that will serve the UA. This header is sent in the 200 OK response of registration message.

Pre Conditions

It is a method to confirm that the resources required for volte call have been reserved prior to ringing 

Curr and desired states for both local and remote are sent with sdp and it is updated in every message as and when progress is getting done.