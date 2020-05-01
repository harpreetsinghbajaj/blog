ABORT is for handling the dialogue
Cancel and Reject are for handling the components
Cancel is send when the timeout condition is occurred.
Reject is send when some invalid component is found.
TCAP is a layer that provides the transactional capabilities to the layers above it.
Following are the two categories under which all the messages fall:à
1.    Request is a message that is passed from the user of TCAP layer to the TCAP layer.
2.    Indication is a message that is passed from the TCAP layer to the TCAP user.
If a message is marked both as a Request and indication then it means that it will be initiated by the TCAP user and needs to be delivered to the remote
party where it will become indication when transferred from TCAP stack to the TCAP user.
TCAP messages are also divided among the categories depending upon they are for supporting dialogue or component.
Following messages support dialogue:à
1.    Begin
2.    Continue
3.    End
Following messages support component:à
1.    Invoke
2.    Cancel
3.    Reject
4.    Result
CDPA is the called party address which is the destination address
CGPA is the calling party address which is the originator’s address
TP-MMS bit shows if the message is segmented and there are more segments in this SMS:à
 
Notice the difference between 0 and 1 value explanation.

Map-Mo-Forward-Short-Message Service:à

1.       This is send from the MSC to the SMSC

2.       The purpose is to request the SMSC to start the delivery of SMS to destination

3.       The SMS is originated from Mobile





Map-Ready-For-SM:à

1.       This is send from the MSC to the HLR

2.       The purpose is to indicate the HLR that Subscriber indicated availability of storage space and is ready to

accept the SMS





Map-Inform-Service-Centre:à

1.       This is send from the HLR to SMSC

2.       The purpose is to inform the SMSC that the SMS is in the storage area of HLR and has not been delivered to the destination Subscriber





Map-Send-Info-For-MT-SMS:à

1.       This is send from the SMSC to HLR

2.       The purpose is to fetch the location information of the Subscriber so that SMS can be delivered to it





Map-Send-Info-For-Mo-Sms-Service:à

1.       This request is send from the MSC to HLR

2.       The purpose is to fetch the





Map-Mt-Forward-Short-Message-Service:à

1.       This request is send from one SMSC to another SMSC to forward the MT SMS


Alert-Service-Centre-Request:à

1.       This is send from the:à

a.    HSS to MSC

b.   HSS to IP-SM-GW

2.       The HSS informs the destination that the Subscriber is available/ready to receive the SMS

3.       Response message is Alert Service Centre Answer





Report-SM-Delivery-Status-Request:à

1.       This is send from the:à

a.    MSC to HSS

b.   IP-SM-GW to HSS

2.       This is also a subscription request to the HSS to notify the sender when the SMS gets delivered to the destination party

3.       Response message is Report SM Delivery Status Response

