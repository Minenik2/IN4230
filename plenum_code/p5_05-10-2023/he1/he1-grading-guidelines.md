
# Table of Contents

1.  [Design document (15 points)](#orgc90bb1d)
    1.  [MIP vs. IPv4 (5 points)](#org4ab3b13)
    2.  [MIP-ARP protocol (5 points)](#org25366c7)
    3.  [Flow chart (5 points)](#org73b095f)
2.  [General implementation quality (10 points)](#org9b6f432)
    1.  [Code structure (5 points)](#org039b0b7)
    2.  [Constructive comments (5 points)](#org800cd2e)
3.  [MIP daemon (65 points)](#orgecd5e72)
    1.  [Handling data from client and server using various send/recv funtions (10 points)](#orgae8bf69)
    2.  [MIP-ARP implementation with ARP cache (35 points)](#org8de5032)
    3.  [Constructing and checking header (10 points)](#orgf189d9f)
    4.  [Use of MIP-ARP cache (10 points)](#org6cc7cc3)
4.  [Ping applications (10 points)](#orgb519843)
    1.  [Ping server (5 points)](#orgecfefa1)
    2.  [Ping client (5 points)](#org51ecb51)



<a id="orgc90bb1d"></a>

# Design document (15 points)


<a id="org4ab3b13"></a>

## MIP vs. IPv4 (5 points)


<a id="org25366c7"></a>

## MIP-ARP protocol (5 points)


<a id="org73b095f"></a>

## Flow chart (5 points)


<a id="org9b6f432"></a>

# General implementation quality (10 points)


<a id="org039b0b7"></a>

## Code structure (5 points)

The implementation code must be nominally readable and structured. It is highly
recommended to split the code in several files, rather than having a huge main.c
file. Using headers, source files, a main.c file and a Makefile which compiles
the project is a good practise.


<a id="org800cd2e"></a>

## Constructive comments (5 points)

Code comments should be concise, to the point and useful ("why am I doing this"
rather than "here is what obviously happens").

Functions should be adequately documented as specified in the assignment text.


<a id="orgecd5e72"></a>

# MIP daemon (65 points)


<a id="orgae8bf69"></a>

## Handling data from client and server using various send/recv funtions (10 points)

Students must implement the UNIX socket interface between the MIP daemon and
upper layers.


<a id="org8de5032"></a>

## MIP-ARP implementation with ARP cache (35 points)

Students must implement the MIP-ARP protocol and send ARP Requests/Reply in
order to discover the MAC address of the requested MIP daemon. The results must
be stored in a MIP-ARP cache.


<a id="orgf189d9f"></a>

## Constructing and checking header (10 points)

Students must respect the MIP specifications. The MIP daemon must be able to
populate the MIP header fields properly and also check the header fields.


<a id="org6cc7cc3"></a>

## Use of MIP-ARP cache (10 points)

The Ping messages after the first one should be able to use the MIP-ARP cache
instead of sending a MIP-ARP Request again.


<a id="orgb519843"></a>

# Ping applications (10 points)


<a id="orgecfefa1"></a>

## Ping server (5 points)

Ping server is able to receive text messages via Unix socket from the local MIP
daemon. It should print this text and send back a ping message with content
"PONG:<received message>".


<a id="org51ecb51"></a>

## Ping client (5 points)

The ping client is able to send a message via UNIX socket to the local MIP
daemon. The message contains user-specified content and is addressed to some
user-specified MIP address. Ping messages are built up in the following manner:
'PING:<user-specified message>'.

After receiving a response, the ping client prints the time between sending the
message and obtaining the response. If no response arrives within 1 second, the
ping client should print 'timeout' and exit.

