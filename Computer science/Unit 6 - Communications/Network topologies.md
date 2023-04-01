
The toplogy of a network describes how devices on said network connect to each other and over how large of an area. There are three main scopes of a network, a LAN (Local area network), WAN (Wide area network), and PAN (Personal Area Network). There are four main network topolgies, bus, star, ring, and mesh. These topolgies are often abstracted to graphs, and have heavy links with [[Graph theory|graph theory]]. Every device connected to the network has a Network Interface Card (NIC) that has the device's MAC address hard coded onto it. This address is used by the router/switch to uniquely identify each device on a network and is represented by a string of hexadecimal pair values.

In each of these types of network, there is a router. The role of a router is to act as a link between the internal network and the external network (internet in most cases). A router broadcasts incoming data to every port on the network, and the correct device will listen to the data. A switch is often used to connect devices to these networks. The role of a switch is to distribute incoming and outgoing data to the correct device. A switch stores the information about where computers are located topologically and can send incoming data directly to the intended recipient. This can be much faster than broadcasting to the entire network, as data collision is avoided for the most part.

## Bus:

In a bus topology, ends of the central cable have to be terminated in order to prevent signals from bouncing back and forth forever. One major limitation of a bus network is that data often clashes when it is sent on the single cable, causing congestion when sending data. Signals are also sent across the entire network, as opposed to data being sent on a dedicated connection. Data can only be sent across one direction. Carrier Sense Multiple Access / Collision Detection (CSMA/CD) is used to enable nodes to wait a random amount of time before resending data so that it does not collide with other transmissions. Similar algorithms are used on [[Wireless connections]] to solve the issue of limited range obscuring other devices on a network. Only one node in a bus network can successfully send data. However, the bus network is easier and cheaper to set up when compared to other network topologies, this makes it good for a small network.

## Star:

In a star network, every device has a single connection to a central hub, this can be a router, a switch, or central server. Performance in a star network is much better compared to a bus network, as packets can be sent directly to the recipient through a switch instead of having to be broadcast along a common connection. These networks are often very expensive due to the cost of each dedicated cable and the network switch.

## Ring:

In a ring network, every computer is connected to two other adjacent computers as well as a router/switch. Packets are broadcast from computer to computer until the intended recipient recieves the data that was requested.

## Mesh:

This is the most costly network, as it is a combination of the ring and star network topologies. Every device is connected to every other device, mirroring a complete graph from [[Graph theory|graph theory]]. There are dedicated links to any device that a single device may wish to communicate with. This provides the fastest solution, however the most expensive and messy to set up.



