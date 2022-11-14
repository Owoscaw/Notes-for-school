The TCP/IP protocol stack is a set of rules used in turn to formar a message so that it can be sent over a network. The layers are as follows:
\> Sender sends a message
\> Application
\> Transport
\> Network
\> Link
\> Message goes from sender router to recipient router
\> Link
\> Network
\> Transport
\> Application
\> Recipient recieves message

## Application layer:
The application layer acts as an interface between applications on a computer that wish to communicate across the internet and the lower layers of the stack. High level protocols like SMTP, FTP, and HTTP(S) are used here to set an agreed standard for communication between end points. This does not determine how data is transmitted, however it specifies the rules of what is to be sent. Protocols that sit on this layer only need to worry about communication with applications, as each layer is self-contained and can be compartmentalised.

## Transport layer:
The transport layer uses TCP (Transmission Control Protocol) to establish an end to end connection with the recipient computer. This layer splits the message into packets, sequentially numbers them and adds the port number to be used (based on application layer). At the recieving end, this layer confirms that packets have been recieved and requests missing packets to be resent.

## Network layer:
The network layer uses the IP (Internet Protocol) to address packets with the source and destination IP addresses. Both port number and IP address are used to determine the socket (endpoint). Each router uses a routing table to instruct the next hop.

## Link layer:
The link layer operates over the physical connection between sender adn reciever. This layer adds the MAC address of the physics NIC that packets should be sent to based on the destination IP address. This MAC address changes with each hop to the MAC address of the next router to be sent to.

When recieving data, the message is based back up from the link layer upwards. The link layer removes the MAC address from each packet and passes it on to the network layer. The network layer removes the IP address from each packet and passes it to the transport layer. The transport layer removes the port number from each packet and reassambles each packet in the right order to be passed on to the application layer. The application layer then presents the message to the user in a browser.

MAC (Media Access Control) addresses uniquely identify a physical device with a Network Interface Card (NIC). This may be the destination computer, or the address of the next router in sequence. This address is hard coded and cannot be changed. Port numbers are used to alert a specific application to deal with data sent to a computer. These are used by protocols to specify what data is being sent. The combination of an IP address and port number is known as a socket.

FTP (File Transfer Protocol) is an application level protocol used to move files accross a network. FTP uses the client server model with seperate data and control channels operating on ports 20 and 21. Usernames and passwords are frequenctly used to protect access to files and to identify users.

SSH, Secure SHell, is an encrypted protocol that allows for secure communication between nodes accross a network. SSH uses public key encryptions to protect data. This protocol can also be used to create a tunnel through a network that passes through a firewall. Ports that are usually blocked by the firewal can be accessed through an SSH tunnel. SSH uses a port that is allowed by the firewall to pass through said firewall, then opens up the ports that need to be used on the other side.

Mail servers are dedicated computers that are responsible for storing mail, providing access to clients and providing services to send emails. The three protocols used for this are SMTP, POP3, and IMAP:
\> SMTP (Simple Mail Transfer Protocol) is used to send emails and forward them between mail servers to their destination.
\> POP3 (Post Office Protocol 3) downloads email stored on a remote server to a local client, which is then removed after download.
\> IMAP (Internet Message Access Protocol) manages emails on a server so that multiple clients can access the same email account.