Between pcrf and pcef

Pcef sends ccr request to pcrf to pull rules required to be applied for a user. 

Pcrf uses rar request to push rules to the pcef for a subscriber 

Pcef comes to know of gx session has to be established or not using the information present in the charging characteristics that it receives from HSS. 

Pcef sends ip mobility flow information to the pcrf so that pcrf can select the rules 

Pcrf sends service flow filters to pcef which is the rule to be applied on user packets 
In every IP flow there are following parameters:
	1	Routing address
	2	3 more Params 




1	Service data flow template is the set of service data flow Filters
	2	Service data flow filter is the set of header and value that need to be matched
	3	Service data flow is the set of packets that will match the service data flow Filters
So service data flow filter is something that has the matching criteria. It will be either pre provisioned or pushed dynamically to the PCEF.

Service data flow filter is a part of the PCC rule. The PCC rule also has the action required if the filter matches.

IP mobility information is provided by PCEF in the routing rule AVP.


	1	Gx interface is between pcrf and pcef.
	2	

For service flow template following parameters are there: 
	1	Rule name
	2	
	3	Service flow filter
	4	
	5	Gate status 
	6	
	7	Monitoring key 
	8	
	9	Sponser 
Pcc rules are of two types 
	1	Static
	1	activated or deactivate
	2	communicated using charging rule name avp
	2	Dynamic 
	1	Dynamic rules are installed or modified or uninstalled
	2	communicated using charging rule definition avp 

Traffic shaping is that When the rate increases beyond the maximum allowed value then queue the packets and deliver them after a delay without dropping them.


Traffic policing is drop they packets when the rate increases beyond the maximum allowed limit. Resume sending when the rate gets back below the maximum allowed value.