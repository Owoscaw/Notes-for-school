In the client server model, network services, such as [[DHCP]], are handelled by one or more dedicated servers that are connected to multiple clients. These clients can request a service or data from the server. Here, the server is responsible for the bulk of the processing. A server will present it's services to clients that can request said services.
![[Client server.png]]

## APIs:

An Application Programming Interface (API) is an interface between a server and it's services. It is a set of functions and protocols that clients can use to request from a server. A server side web API is a set of web services or web resources that enable programmers to build web applications. Sometimes programmers use multiple server side web APIs to create combined web applications called mashups. 

A client has to request a "pull" from a server, if too much time passes between establishing a socket connection beteen client and server, and the reciept of a client's request, the server will drop the connection so that it can conserve resources.

## WebSocket protocol:

The WebSocket protocol includes an API for establishing a persistent TCP socket connection. This is designed for a web browser and server, but any type of client and server can use it. This connection is full-duplex (simultanious bidirectional), and allows the client and server to send data at any time. A server can "push" data to a client. This can be thought of as a "pipline" between client and server, packets do not need as much header information as they are travelling down a dedicated path, with known end points. Because this connection is trusted and secure, packet sizes can be greatly reduces as the headers can be made smaller. This can create a very fast, interactive connection between client and server.

## Databases:

Servers often make use of database systems to store and retrieve information. Databases are often accessed through the client server model using the four basic operations, represented by CRUD. Create - write a record to a databse, retrieve - read a record from a databse, Update - amend a record, delete - remove a record from the database. SQL statements are used to interact with a database map.

## Thin/Thick networks:

There are different types of clients. A "thick" client is a client that is each a fully fledged computer. This is the easiest way of setting up a client server network, standard computers are joined as hosts via a network medium. This is expensive. A "thin" client is a low-powered device, designed specifically to act as a network machine. Processing is done on a powerful central server and the hosts are only used to display outputs and take inputs. These clients will have a simple operating system that requires little maintenance and administration. A "zero" client can download the latest OS version and its configuration from a server each time a user switches it on. Whilst there is a cost saving from not requiring an individual machine, a powerful server as well as a good network infrastructure is needed to achieve the same performance. 

In a network with thin clients, there is a single point of failure, the central server. Because this server provides the majority of the computational power to each client, they will not be able to operate if the server fails. Because of this, there are often multiple central servers with seamless switching between them in case of a failure. This allows for no inturruptions to workflow for thin clients if a server goes down for maintenance. Thin clients are easier to set up and maintain, and software can be atuomatically distributied, however there is increased reliance on the server and associated infrastructure.

In a network with thick clients, there is no single point of failure and clients can still work on their own without the server. However, clients need to be more capable with higher specs in order to run all their programs locally. This is generally better for running more powerful applications. Installation of software has to be done manually on each new client added. Because there is a lot of cimmunication between a thick client and the central server, they are susceptible to a man in the middle attack.
