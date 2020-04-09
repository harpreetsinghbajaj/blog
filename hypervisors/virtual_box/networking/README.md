Now the problem is accessing internet from VM. This has been solved. I added a nat network adapter and added the corresponding interface file. This file has addressing as DHCP. So no issues in internet access now

I have removed the bridge interfaces by disabling the virtd service. Remember I disabled not just stopped