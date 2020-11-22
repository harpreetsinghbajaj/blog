The IPv6 address is 16 bytes long.
It can have many canonical form

in ipv6 there is no broadcast address. The concept of broadcast is implemented via the multicast.


Link prefix is the address part of the network that is same across all nodes in the link 

Address auto configuration is the method by which the node itself generates an address for local communications within the local lan. This address has a prefix fixed by standard fe08 and followed by the MAC address of interface. Thus the address is expected to be unique 

The generated address is then validated over the network for its duplication. For this neighbour solicit message is used. The generated address is sent to all the hosts on the link. If any host is using that address it responds back with neighbour advertisement message and the address is marked duplicate.

When the host becomes active it sends out a router solicitation message to the router so that router can assign an IP address to the node which the node can use for packet forwarding. 

The router sends the router advertisement message to the node with the IP address, Mitu size etc information.

The flow label is there in the ipv6 header. This identify that the packets are part of some specific communication and need to be handled in a definite manner. For example a volte call can have a flow lable but the other voip calls like Skype etc may not have that. But all of them will have the same dscp value. 

Header length is fixed thus making the hardware level processing of the header possible this makes the packet forwarding fast.

Link local address has a fix prefix 
