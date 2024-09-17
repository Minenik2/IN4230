# 7th plenary session: 19.10.2023 #

During this session, we discussed in detail Home Exam 2, covering the new
concepts it introduces.. In Home Exam 2, we're expanding our network stack that
we are building during this course. This involves implementing a routing daemon,
which will provide forwarding and routing services to the MIP daemon."

Using a similar topology as in Home Exam 2, we demonstrated step by step how a
routing daemon can:

- discover neighbors using broadcast HELLO messages
- build a routing table and share its routes by unicasting UPDATE messages to neighbors
- detect link failures in the network

The routing daemon should run a simple Distance Vector Routing (DVR) protocol,
with Poisoned Reverse loop protection. An example of DVR protocol is RIPv1,
which due to its limitations is superseeded by RIPv2.

Read more about RIP (Routing Information Protocol) [here](https://en.wikipedia.org/wiki/Routing_Information_Protocol).
