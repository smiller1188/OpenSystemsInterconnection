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
