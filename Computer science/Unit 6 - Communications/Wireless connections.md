
Wi-Fi is a wireless networking technology that provides high speed connection to the internet. Devices connect using Wi-Fi to a WAP (Wireless Access Point). To connect to a wireless network, a Modem, router, ISP, and an NIC are needed. The modem and WAP are often built into a router. 

A station consists of a computer and an NIC, stations share a radio frequency channel. This means that Wi-Fi transmissions can interfere with each other if two stations are transmitting at the same frequency.

The SSID (Service Set IDentifier) identifies each network by a unique name. This can be hidden and set to broadcast within range of an access point. Wireless networks can be less secure than wired networks, unauthorised uses can be hard to spot and transmitted data is easily intercepted. Security protocols are used to counteract this, WPA and WPA2. These two security protocols encrypt each packet with a seperate key asymettrically, WPA2 encrypts packets multiple times to ensure security. MAC addressed can be blacklisted from a network, as well as only allowed devices to be whitelisted.

Several devices may transmit via a single WAP, if they try to transmit simultaneously then collision avoidance algorithms come into effect. CSMA/CA is used to wait a random amount of time before retransmitting a signal if there was a collision. This algorithm is used for other types of [[Network topologies]]. Frequency channels for Wi-Fi communication have an overlap with other channels. Typically, one channel will span 22Mhz, +/- 11Mhz above and below the centre frequency of the channel. After a collision and a wating period, a device can send a request to send signal (a small packet of data to determine if the network is clear). The WAP that it is transmitting to then responds with a clear to send signal, which indicates to the transmitting device that it can transmit. This solves the problem of two nodes that cannot see each other transmitting when they see that the network is clear.