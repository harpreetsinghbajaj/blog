Vlan tag is configured on switch. When client attached to some port in the switch sends packet then switch adds the vlan tag.

In vlan two ports types are there one is access port and other is Trunk port.

Vlan is layer 2 concept with tagging in it. No trunk no vlan.

In vlan instead of installing different switches a same large numbered port switch is logically divided into multiple switches.

Its possible that different customers are using same vlans inside there network. So to distinguish inner tag and outer tag are used. 

Inner tag is same as the vlan id added by the customer. When this packet goes on trunk line then tag will be added for customer.  This is outer tag 

Layer 3 switch is capable of determining the  subnet and then sending it to correct vlan. To determine the MAC address of destination arp has to be sent. Layer 3 router shall send arp request to only the nodes present in the vlan to which the up 

belongs there not sending arp to other vlan nodes 