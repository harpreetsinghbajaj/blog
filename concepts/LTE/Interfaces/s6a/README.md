
S6a interface is between the HSS and the MME. This is responsible for the following:

	1	Mobility Management (ULR/ULA, CLR/CLA, Purge)
	2	Subscriber Data Handling (IDR/IDA, DSR/DSA)
	3	Authentication (AIR/AIA)
	4	Fault Recovery (RESET)
	5	Notification (NOR/NOA)

 ULR/ULA:

	1	Sent from MME to HSS
	2	Exchange of subscriber data
	3	HSS stores the MME for the location of Subscriber

 CLR/CLA:

	1	Sent from HSS to MME
	2	In case of withdrawal of services of Subscriber, Subscriber sends ULR via some other MME as part of handover
	3	If MME is stored in the HSS then only the CLR is sent

 Purge:

	1	Sent from the MME to HSS
	2	MME informs HSS that a Subscriber’s context is being deleted from the MME as it is inactive over a certain period of time

 IDR/IDA:

	1	Send from HSS to MME
	2	When the subscription information of the Subscriber is modified with some additions

 DSR/DSA:

	1	Sent from the HSS to MME
	2	When the subscription information of the Subscriber is modified with deletion of services from its profile
Reset:

	1	Sent from the HSS to MME
	2	When the HSS goes down and comes up, it informs the MME about its coming up so that MME can resynchronize there information regarding Subscribers

 NOR/NOA:

	1	Send from MME to HSS
	2	MME informs the HSS about the PDN where the subscriber latched

 AIR/AIA:

	1	Sent from the MME to HSS
	2	MME fetches the authentication information of the Subscriber
Following are certain AVPs out of an exhaustive list:
	1	ULR-Flags is a bit mask in which set/unset of a bit indicates special meaning to the HSS.
	2	ULA Flags is a bit mask that are sent from HSS to MME which indicate special meaning.
	3	Visited PLMS is the MNC/MCC of the PLMN in which the MME received attach. This can be used to match the roaming information.
	4	RAT-Type indicates the type of radio access network being used by UE.
	5	IMSI represents UE identity.
	6	Result is either the base diameter result or the application level result code.
	7	Cancellation Type tells the reason for cancellation like the subscription withdrawal, Initial attach procedure, etc.
	8	Subscription data is a composite AVP which has many sub AVPs. This is the service related data of the subscribers.
	9	DSR Flags indicates that what type of data has been withdrawn from the profile of user.
	10	IDR Flags indicates what all data type has been modified.
	11	AVP-Configuration is a grouped AVP in which the APN configuration is available.

Multi apn means that both IPv4 and ipv6 addresses are allowed for a single apn 




