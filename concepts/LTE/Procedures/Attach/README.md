Subscriber of the LTE network needs to have an initial attach procedure so that it can latch into the network. Following is the procedure followed
for the UE to attach to a network:

1. UE ID acquisition: Means to make the MME aware of the IMSI
	1. RRC connection establishment: For UE to send messages to Enode-b over Air interface:
		1. UE sends RRC connection request to enode-b
		2. Enode-b sends back the SRB to the UE
		3. UE sends RRC Connection complete to the Enode-b inside this NAS message Attach Request is also sent.
	2. S1 Signalling Establishment: For the Enode-b to send NAS messages from UE to the MME
		1. Signalling S1-ap messages flow between the enode-b and the MME.
		2. S1 connection for a specific UE is identified by a pair of IDs (enode-b UE S1ap id and MME UE S1ap id)
		3. NAS message attach request is sent to the MME as a NAS PDU in a s1-ap message Initial UE message
	3. ECM connection Establishment:
		1. UE is now capable of sending NAS messages to the MME
		2. UE moves to state ECM Connected, EMM registered and RRC-Connected.
	4. MME reads the attach message and gets the IMSI of UE that wants to attach
2. Authentication: IMSI received in above steps needs to be authenticated.
	1. MME performs AIR/AIA with the HSS to receive authentication information over s6a interface
	2. MME and User mutually authenticate each other using the NAS protocol
		1. MME keeps an XRES with it and sends the other information received by the HSS to UE in NAS authentication request message packed in a Downlink S1AP message
		2. UE sends back the authentication response message to the MME in an Uplink s1ap message
		3. MME compares the response from UE and XRES
3. NAS security setup: To setup security mechanism between UE and MME
	1. MME sends security mode command in a downlink s1ap message to UE
	2. UE generates the security keys and sends back the Security mode complete to the MME in an uplink Nas transport message
4. MME exchanges ULR/ULA with the HSS to retrieve the subscriber data
5. MME fetches the APNs from the UE by sending NAS request ESM information request
6. ESM session creation procedure for the UE:
	1. MME sends a create session request to the SGW/PGW which perform the following processing:
		1. PGW performs the following action:
			1. PGW allocates an IP address to the UE
			2. CCR/CCA is performed over the gx interface to exchange the access profile information with the PCRF
			3. PGW decides based upon the received information that what properties shall be used to create the session
	2. Create session response is send to MME with the IP address of the user and the tunnel ID for the bearer on SGW/PGW
	3. MME sends the initial context setup request to the Enode-b in which it sends the attach accept NAS message for the UE
	4. Enode-b receives the s5 tunnel id and forwards the attach accept NAS PDU to the UE
7. Enode-b exchange the security mode command/complete with the UE to secure the RRC connection and bearer data
8. Dedicated bearer (DRB) is created between the UE and Enode-b using the RRC reconfigure. Inside RRC reconfigure, attach accept is send to the UE
9. Enode-b sends back the initial context setup response with the s1 enode-b tunnel ID corresponding to the s5 tunnel id received earlier
10. MME sends the modify bearer request to the SGW/PGW so that they can complete the pair of Ids with them.
11. Now the S1 bearer is established