# Open Systems Interconnection (OSI) Model

The Open System Interconnection is a framework that describes the function of a networking system that’s made up of seven layers. The purpose of the OSI model is to simplify troubleshooting, enable interoperability and break down complex data transmission processes into manageable, modular components. The OSI model is helpful when visualizing the flow of data from sender to receiver. When following the components of each layer, it makes it easier to pinpoint networking issues.
As mentioned earlier, there are seven layers in the OSI model. When communicating from one person to the other, communication flows from layer 7 to layer 1. Each layer needs to complete its specific duties before moving on to the next layer. 

**Layer 7- Application layer**

The application layer is the closest layer to the end-user. Software applications like web browsers and email clients rely on the application layer to initiate communications. Client software applications are not part of the application layer, but rather the application layer is responsible for the protocols and data manipulation that the software relies on to present valuable data to the user. Layer 7 applications use protocols like HTTP for web browsing, SMTP for email, and FTP for file transfers.

**Layer 6- Presentation Layer**

The presentation layer is responsible for preparing data so that it can be used by the application layer. Devices that are communicating with one another may use different encoding methods so layer 6 is responsible for translating the data into syntax that the application layer of the receiving device can interpret.

If the devices are communicating over an encrypted connection, layer 6 is in charge of adding the encryption on the sender’s end while decoding the encryption on the receiver’s end so that the data is decrypted and readable data. 

The presentation layer also compresses data that comes from the application layer before it sends it on to Layer 5, the session layer.

**Layer 5- Session Layer**

The session layer handles opening and closing data network communications between interacting devices. The “session” refers to the time between the opening and closing of the interaction. The session layer makes sure the session is open for a long enough period of time for all the necessary data to be sent through, then closes the session to prevent expending unnecessary resources.

**Layer 4- Transport Layer**

The transport layer is responsible for end-to-end communication between two devices. This includes taking data from the session layer and breaking it up into segments before sending it to the network layer. The transport layer on the receiving device is responsible for reassembling the segments into data the session layer can consume.

The transport layer takes care of managing the flow and any necessary error messages that need to be sent in the event something goes wrong. To manage data flow, the transport layer makes sure it is not being sent so quickly that the receiver’s device can’t handle it. In order to control errors, the transport layer checks to see if the data transmitted was done completely. If it is not, this layer will request a retransmission. Transport layer protocols include the Transmission Control Protocol (TCP) and the User Datagram Protocol (UDP).

**Layer 3- Network Layer**

The network layer facilitates the transfer of data when two networks are communicating with each other. If two communicating devices are using the same network, then there isn’t a need for the network layer. The network layer divides the segments that come from the transport layer which are referred to as packets. The division of the segments into packets happens on the sender’s device, and they are reassembled on the receiving device.

The network layer also functions as an efficiency tool. It figures out the optimal physical path needed to get the data to its destination. This function is known as routing.

**Layer 2- Data Link Layer**

The data link layer is similar to the network layer, except the data link layer facilitates data transfer between two devices on the same network. The data link layer takes packets from the network layer and breaks them into pieces called frames. Like the network layer, the data link layer is also responsible for flow control and error control in intra-network communication.

**Layer 1- Physical Layer**

This layer includes the physical equipment involved in the data transfer, such as the cables and switches. This is also the layer where the data gets converted into a binary stream, which is a string of 1s and 0s. The physical layer of both devices must also agree on a signal convention so that the 1s can be distinguished from the 0s on both devices.

Data flows down the seven OSI layers on the sender's device (encapsulation) and up the layers on the receiver's device (de-encapsulation). Data starts as user input (Application Layer), is formatted/encrypted (Presentation), managed (Session), segmented (Transport), packetized (Network), framed (Data Link), and converted to bits (Physical) for transmission. The receiving device reverses the process, moving from Layer 1 up to Layer 7.

**Open Systems Interconnection (OSI) Model using Cisco Packet Tracer**

Cisco Packet Tracer was used to design and test a basic network topology that demonstrates communication across the layers of the OSI model. The topology includes one switch, one server, and three PCs connected within the same local network. 

<img width="975" height="520" alt="Image" src="https://github.com/user-attachments/assets/225ee568-954e-43ff-9be6-12af13133efd" />

All devices were configured on the network 192.168.1.0/24 using the subnet mask 255.255.255.0. The server was assigned the IP address 192.168.1.254.  

<img width="975" height="516" alt="Image" src="https://github.com/user-attachments/assets/d7335ae6-a103-4778-a464-464d33dad751" />

PC0 was configured with 192.168.1.2. 

<img width="975" height="522" alt="image" src="https://github.com/user-attachments/assets/2b689ee0-8722-4470-9820-f83c474c2b0b" />

PC1 was configured with 192.168.1.3. 

<img width="975" height="516" alt="image" src="https://github.com/user-attachments/assets/c57ad2d6-3f4f-4f5b-8ad4-552ca530ec39" />

PC2 was configured with 192.168.1.4. 

<img width="975" height="519" alt="image" src="https://github.com/user-attachments/assets/834830a3-364c-4173-b0ea-2532d86a376f" />

Email configuration involves setting up a mail server and client devices so that messages can be sent and received across a network. The server is configured with SMTP (Simple Mail Transfer Protocol) for sending email and POP3 or IMAP for receiving email. 

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/daaab5b4-1de5-4ea4-8f0b-d6c1671294bb" />
 
Each PC client is configured with the mail server’s IP address, a username, password, and the appropriate incoming and outgoing mail protocol settings. 

<img width="975" height="519" alt="image" src="https://github.com/user-attachments/assets/75fe919a-e573-4e21-b582-e5c29a1d2efe" />

<img width="975" height="517" alt="image" src="https://github.com/user-attachments/assets/4af16f59-4aa1-42b3-9e2f-6f52368accb3" />

After configuration, email messages can be successfully transmitted between users on the network, confirming proper communication.

<img width="975" height="522" alt="image" src="https://github.com/user-attachments/assets/e5e46acb-306e-41cd-81ff-d4f81a8778d2" />

To demonstrate application-layer services of the OSI model, a DNS record was created on the server for the domain www.watch.com. This allowed any PC in the network to resolve the domain name to the server’s IP address. 

<img width="975" height="516" alt="image" src="https://github.com/user-attachments/assets/d1843e14-09a8-428e-9497-f14970bd550f" />

Web browsing was then tested from a PC to confirm successful name resolution, network communication, and service delivery across the OSI layers. The successful connection verified proper configuration of addressing, switching, DNS services, and end-to-end communication within the simulated network.

<img width="975" height="515" alt="image" src="https://github.com/user-attachments/assets/98b7eaf3-c846-4ea2-b179-25c45c05c4b6" />

When devices such as PCs and servers communicate, data is encapsulated and transmitted using the four layers of the TCP/IP model: Application, Transport, Internet, and Network Access. Packet Tracer allows users to visualize this process through simulations like ping tests, web browsing, DNS resolution, and email transmission.
 
<img width="975" height="517" alt="image" src="https://github.com/user-attachments/assets/508d09ca-7384-4aa7-a37f-e5ddb5c25ff0" />

 

 


