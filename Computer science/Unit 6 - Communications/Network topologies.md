

The role of a router is to act as a link between a local network, and the internet. Most modern routers provide 3 to 4 physical RJ-45 ports as well as wireless connections to devices, that use it to gain access to the internet. A LAN (Local Area Network) describes a network that connects many devices to a router over a local area. This may contain as much as multiple switches, wireless access points and servers or as little as two interconnected computers. A WAN (Wide Area Network) describes multiple connected LANs over a wide area. A PAN (Personal Area Network) describes multiple connected devices that are on someone's person, e.g. a smartwatch, mobile phone, and fitness tracker. 

A switch distributes data to the intended device when it arrives from the internet or a connected device. This is much more optimal than a hub that distributes data across all connections, as communication can still occur on connections that aren't sending or receiving data at that moment. 

LANs can enable shared resources over an area, be it files or devices (like printers). It also enables security and remote access over connected devices.

A network topology describes the arrangement of various devices that make up a network. Two popular network topologies are the bus topology, where nodes are connected in a daisy chain along a single central communication channel; and the star topology, where a central node or hub provides a common connections for all other nodes. This shares heavy links to [[Graph theory]] and the [[Graphs]] data structure.


In a bus topology, ends of the central cable have to be terminated in order to prevent signals from bouncing back and forth forever. One major limitation of a bus network is that data often clashes when it is sent on the single cable, causing congestion when sending data. Signals are also sent across the entire network, as opposed to data being sent on a dedicated connection. Data can only be sent across one direction. Carrier Sense Multiple Access / Collision Detection (CSMA/CD) is used to enable nodes to wait a random amount of time before resending data so that it does not collide with other transmissions. Similar algorithms are used on [[Wireless networks]] to solve the issue of limited range obscuring other devices on a network. Only one node in a bus network can successfully send data. However, the bus network is easier and cheaper to set up when compared to other network topologies, this makes it good for a small network.


Every networked device contains a NIC (Network Interface Card), which is attributed a unique MAC (Media Access Control) address that is hardcoded into the device. These unique addresses are used to send data to the correct device. A switch holds all the MAC address for each device connected to it and uses this information to ensure that packets of data reach the correct device. 


In a star network, is it easy to diagnose and isolate problems, as each node has a dedicated connection. Performance is often much better than that of a bus network, as packets are sent to their intended destination instead of being broadcast across the entire network. They are also more secure because of this feature. However, the amount of cable and the cost of switches can add up to make installing a star network expensive. A star network also has a central point of failure, the switch/router at the centre. 


The physical topology of a network defines the physical connections between networked devices, whereas the logical topology defines how devices communicate over the physical topology.




