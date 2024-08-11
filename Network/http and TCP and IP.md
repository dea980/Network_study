Http and TCP/IP is not the same thing and these are interact each other
http is containing the TCP.
HTTP means that the type of the protocol that is based on the TCP

For clarification, We need to understand OSI 7 Layer ![[Screenshot 2023-10-02 at 8.42.41 PM.png]]
source : https://hwan-shell.tistory.com/271

If we supposed to type the domain name at the internet search line : "www.google.com", for the internet window, it need to get into the www.google.com for getting the service with several format. 
In this term, for the every activities that user does for the www.google.com is called Application Layer which is the seventh layer of the OSI 7 Layer.
From the Application Layer, it added the Header for the what kind of the data and types of the protocols for the server, and these called the packet, and it happened when we press the enter key to the browser after we type the address. 
For the process, 'Browser (Application) -> own computer lan card'  it adds the several packet for every layers (OSI 7 Layer)

As the photo shown, Started with the Data, and it adds the several packets through the 7 layers. For example 2nd layer, presentation layer, it add the encrypt or decrypt (암호화 또는 복호화).

Is http is equal to tcp?
It might be confusing about http and tcp because they both the same functions  and characteristics. By the point of view, it could be equal and different at the same time. (for example, 4th layer view, TCP and HTTP are same but 7th layer view, TCP and HTTP are different.)

What is the characteristic for TCP?
- Connection oriented (연결 지향적)
	- Connection oriented means that Client and server were connected each other.
- Ensure reliability with 3-way handshake and 4-way handshake operations. (신뢰성 보장)
	- when making a tcp communication, make sure that the servers are ready to communicate and that they can connect to each other to send and receive data.
	- If you're ready, you can communicate, and if you're not ready, you can show the user a message or error that the server is not ready.
- Order guarantees(순서 보장)
	- Sending data over TCP guarantees the order of packets.
		- if 1 to 100 packets are sent, 1 to 100 packets will arrive at the server in turn.
	- There's the opposite concept, udp, and can think of it as the opposite of the above explanation.
	- UDP sends data to the server, which means that the server and the client are not connected to each other.
		- which means, we don't care if the server is alive or dead, an we don't send data to that address and we don't check it.
		- there's no 3-way handshake. also the order is not guaranteed.
- All the features of this tcp are http
- why? because the packet based on tcp is http.
HTTP vs TCP Socket
different point is one
- Will you provide information about the client's request in accordance with the established rules and disconnect it  
- Or
- Will you stay connected to each other forever without rules or anything like that?
	- It could lead to another question, "Isn't it HTTP if I program with TCP Socket communication, receive client data, and disconnect the client from the server?"
		- *Point is principle is similar but different each other.*
		- *Protocol is different so defined header datas are different each other*
- Comparing TCP Socket network and HTTP network
	- TCP Socket
	- 

![[Screenshot 2023-10-02 at 10.15.05 PM.png]]
- source :https://hwan-shell.tistory.com/271
- This packet, One of the developer, create the JAVA for the chatting server and connect with the other computer.
- As Protocol shows, TCP-based S101 was used and blue block below is the string I sent to the server.
HTTP
![[Screenshot 2023-10-02 at 10.23.44 PM.png]]
This is the http server that one of the developer created with C++. It shows that json communication is based on HTTP.
- Socket communication, which is typically used for programming, starts at Layer 4, and packets are generated.
- For HTTP communications, packets are generated starting from layer 7.
Then TCP Socket cannot do HTTP network?
- Available but need to implement it.
- For to code it, we need packet-wise coding skills and know how to define headers attached to each layer.
- It also does not control input and output in a non-blocking asynchronous manner, so we have to implement it ourselves.
- Since hard to implement, and it's annoying, we used an API or framework that supports the http protocol. If we use these things, they provide functions that make it easier to maintain sessions and bind.
- HTTP consists of TCP.  
	- Therefore, they both go through 3-way handshake and 4-way handshake.  
  
- So from a four-tier perspective, these two are connection-oriented communication,  From a Layer 7 perspective, http is disconnected (because it does not maintain client-server connectivity)  
- Socket communication is about being connection-oriented (because clients and servers remain connected as they exchange data)

*Now I have to try some simple coding for figure out the HTTP and TCP in clearly*