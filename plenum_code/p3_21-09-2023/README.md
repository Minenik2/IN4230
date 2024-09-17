# 3rd plenary session: 21.09.2023 #

This plenary session was entirely focused on RAW sockets and MIP-ARP protocol.
Through a simple example of a 3-node topology (A - B - C), we covered the main
functions that a host needs to call in order to:

	- send a simple ARP request via a RAW socket
	- send a ARP reply in response to a BROADCAST ARP request
	- walk through all the interfaces of a host and store their MAC addreses
	- etc.

Enough with words and hands on the C code!  

Check the code
[here](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p3_21-09-2023/greet-your-neighbor)
and feel free to adapt it for the Home Exams.  

Since we had some time left, we started discussing topics planned for the next
session as well. One such topic was an additional approach for sending data over
the network by copying a `struct` into a byte array (serialization), sending it
via a RAW socket, and then deserializing the data at the receiving end. One can
chose to use serialization/deserialization or encapsulating the information into
`struct msghdr` in order to send/receive MIP packets via RAW sockets. Both
examples are available
[here](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p4_28-09-2023/).  


**NOTE:** These examples that we are coding in the plenaries are very simple and
some stuff might be hardcoded. Make sure to write clean and efficient code in C,
with proper functions and
better comments.  

All the best! :-)
