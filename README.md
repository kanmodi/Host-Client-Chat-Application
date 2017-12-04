# Host-Client-Chat-Application

Implements a host-client chat program in python using standard socket package.

### FRAMEWORK USED
The program is written in standard Python 2.7, using the default built-in GUI tool tkinter. All network code is written using standard socket package. The main thread is the GUI thread. Another thread is running a TCP service that allows clients to connect. The program has been tested on different machines.

### DESCRIPTION
This project is an example of a chat server. It is made up of 2 applications the client application, which runs on the user’s PC and host application, which runs on any PC on the network.

- This project is based on socket programming and network protocols. A socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.

-	Normally, a host runs on a specific computer and has a socket that is bound to a specific port number (IP Address). The host just waits, listening to the socket for a client to make a connection request.

- On the client-side: The client knows the hostname of the machine on which it is running and the port number on which the host is listening. To make a connection request. The client also needs to identify itself to the server so it binds to a local port number that it will use during this connection. This is usually assigned by the system.

-	If everything goes well, the host accepts the connection. Upon acceptance, the server gets a new socket bound to the same local port and also has its remote endpoint set to the address and port of the client. It needs a new socket so that it can continue to listen to the original socket for connection requests while tending to the needs of the connected client.

-	On the client side, if the connection is accepted, a socket is successfully created and the client can use the socket to communicate with the host.

-	The client and server can now communicate by writing to or reading messages from their sockets.
For seamless communication to occur between the client and the host, it is required that the host creates a DMZ via its default gateway.
It is designed to not need a central server and so work very well on LANs that are not connected to the internet. One user starts the program in host mode, listening on a port of their choosing, and then other users connect to their machine and run the client code. 

### Chat platform: 
- It contains a rich display screen which cannot be edited but only displays the messages from one user to another, including the self-sent message, as in any chat application.

- It contains a textbox for messages to be written that is sent across the network. 

- It contains a Send button.

- When the sent button is clicked, in the background, the text in the textbox is encoded and sent as a packet over the network to the client machine. Here this message is decoded and is shown in the rich textbox. 

- To make it more realistic, the self-sent message is shown in the rich textbox as well. Both the messages are differentiated by the help of the identifier name at the beginning of each message in the rich text box.
