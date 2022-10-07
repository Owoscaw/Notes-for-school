Devices using private [[IP adresses]] cannot directly access the internet, they must communicate via another network device that can provide Network Address Translation (NAT). This allows for a single public IP address to be shared by any number of hosts with private IP addresses. 

![[NAT.png]]

This allows for only one IP address to represent an entire network, only one IP address is needed to be paid for. This IP address will handle any requests from the private hosts connected to it, and will return data to the private IP address that requested it, once it has recieved the data from the wider internet.

The NAT translation device records the source and destination socket addresses for each request. It then communicates on the host's behalf with the destination IP address. When a response returns, it is passed back to the host that made the original request.

NAT can also provide port forwarding. Servers accessible to the public can be given a non-routable IP address, used within a private network. A public request reaches the external router of the private network using a given port. The data packets are forwarded internally to the correct device, this provides additional filterting.

Some network structure allows for a DMZ (De-Militarized Zone). This is where there is a layer between the public internet, and a private network. Devices that sit within this zone can directly access both the internal network and the external internet. Packets that travel between the DMZ and internal network, aswell as the DMZ and wider internet, do not have to pass through a firewall. This places the responsibility of security on the device in the DMZ.

DHCP (Dynamic Host Configuration Protocol) is used for the automatic assignment of IP addresses and any other network configuration information. This allows limited pools of dynamic IP addresses to be shared out between hosts, and are freed up when not in use. Hosts can therefore reconfigure themselves when moving between networks, which reduces the total number of IP addresses required locally, as not all hosts will require network access at the same time.