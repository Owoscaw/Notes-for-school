An IP address is a number used for packet routing that unique. It identifies each computer on a network and consists of 4 octets (in IPv4), writen as 0.0.0.0 - 255.255.255.255, or 00000000.00000000.00000000.00000000 - 11111111.11111111.11111111.11111111.

Some IP adresses cannot be used as they are reserved for other purposes. 192.168.x.y, 10.x.y.z and 172.16.0.1 - 172.31.255.255 are non routable addresses used for LANs or private WANs, they cannot be used to [[Packet switching and Routers||route packets over the internet]]. x.y.z.0 represents an entire network, the last address in a network (x.y.z.255) is reserved as the broadcast address on that network for sending data to all hosts on said network. 127.x.y.z is reserved for loopback, where a host's IP software treats an outgoing packet as an incoming packet.

IPv4 only provides a theoretical maximum of $2^{32}$ addresses, which is not enough. IPv6 uses 128 bits, expressed as a 32 digit long hexadecimal number. This provides $16^{32}$ possible addresses, which is a lot bigger. In an IPv4 address, the left-hand bits of a 32-bit number are used to define the network where nodes are communicating. The right-hand bits of the 32-bit number are used to identify seperate nodes on the network. Since both IDs occupy complementary sets of bits within the IP addresses, they can be added together to form the IP address. For example: Network ID - 142.67.0.0, Host ID - 57.253, full address - 142.67.0.0 + 57.253 = 142.67.57.253. Note that it is not always the first two octets for network and the last two for host, it could be split in any other way. This split can be indicated with a suffix of /x, where x is the number of bits used for the network.  This is known as classless addressing.

IP addresses used to be categorised into various classes to help identify the network and host IDs of various ranges. The most significant bits of an IP address were used to indicate the class type, 0 = A, 10 = B, 110 = C, 1110 = D, 1111 = E. 

## Subnets:

A subnet mask is used together with an IP address to identify the network ID within the address. This mask has all network ID bits sent to 1 and all host ID bits set to 0, so the bitwise AND operation is performed with the IP address and the subnet mask. The output of this operation is the network ID of the IP address. For example, a network with a subnet mast x.y.z.w/28 will have 4 bits remaining for the host ID, and will therefore be able to service $2^{4}$, or 16 hosts. Note that the split between host and network ID does not have to be between octets.

An organisation can choose to further subdivide the number of available host IDs that they have between individual subnetworks. This reduces the broadcast domain, improving security, as well as reducing the number of data collisions.

An IP address can be public or private. These ranges are considered private and are non-routable:
\> 10.0.0.1 - 10.255.255.255
\> 172.16.0.1 - 172.31.255.255
\> 192.168.0.1 - 192.168.255.255

These addresses are reserved for use within LANs and private WANs, they cannot be routed accross the wider internet.

