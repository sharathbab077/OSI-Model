# Computer Networks
Implementation of Open Systems Interconnection(OSI) networking model.
In this project we already have a sender machine which sends data by forming frames to the destination machine.To complete the relay of the data frames we build the reciever side of OSI model.

Steps:
1.	Receiver receives frames individually from sender machine.
2.	Receiver physical layer removes datalink layer header appended by sender and forwards frame to its datalink layer.
3.	Receiver datalink layer removes network layer header of sender and forwards packet to its Network layer.
4.	Receiver network layer, if it is the destination machine then it removes transport layer header of sender and forwards packet to its transport layer.
5.	Transport layer removes session layer header of sender and stores the packet in buffer (we implement array here).
Here the packets from second frame of sender obtained, even application and presentation layer header of sender is removed and stored in buffer.
6.	Once all frames are obtained from sender and it reached transport layer, the final message is forwarded to its presentation layer.
7.	Session layer removes presentation layer header of sender and further presentation layer removes application layer header of sender, finally at receiver application layer actual message sent by sender is obtained.
