invite is sent from the caller to the callee.


UAC will search for the P-CSCF in the zone it is present
P-CSCF will coordinate with the I-CSCF to fetch the S-CSCF that is serving the UAC.
I-CSCF performs LIR query with the HSS and informs the P-CSCF with the S-CSCF address.
P-CSCF will forward the invite to the S-CSCF
100 Trying is sent to the UAC
S-CSCF now performs LIR query with the HSS to fetch the S-CSCF of the destination party
Continuation of the invite procedure:-
Scscf of the originator will forward it to the Scscf of the destination party
Scscf of the destination party will use the ip address details (fetched using via header) to send the invite to the UAC via proxies.
The destination UAC decodes the SDP information and checks what is feasible at its end to create the session. It sends 183 session in progress along with the list of the selected codes as SDP body.
Originating UAC sends prack message to the destination party along with the selected codec.
Both the sender and receiver of the invite now initiate pdp context activation 
Destination UAC will initiate the create dedicated bearer procedure to set up the dedicated bearer having property as per the negotiated SDP
For originating UAC, the pcscf will be initiating the network initiated dedicated bearer request by communicating with the pcrf
The originating UAC will send the update sip message to the destination UAC so that the session properties can be modified. Destination responds with a 200 ok for this update message.
Now that the bearers are created, the destination UAC will send 180 ringing to the originating UAC which responds with a prack. Prack is responded with a 200 ok
Destination UAC sends 200 OK and the originator responds back with an ack message