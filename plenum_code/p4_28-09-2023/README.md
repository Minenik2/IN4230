# 4th plenary session: 28.09.2023 #

The focus of this plenary session was on two approaches for sending a packet
with multiple headers via RAW sockets:

	- using a `struct msghdr`
	- serializing the `struct pdu` into a byte array


Check the code
[here](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p4_28-09-2023)
and feel free to adapt it for the Home Exams.  

In addition. I uploaded two files on Mattermost: one is a mininet script for
testing home exams, and the other is a grading guidelines file summarizing all
the implementation requirements for Home Exam 1. If you recently joined the
channels and cannot see the files, please let me know and I will send them to
you.

**NOTE:** These examples that we are coding in the plenaries are very simple and
some stuff might be hardcoded. Make sure to write clean and efficient code in C,
with proper functions and
better comments.  

All the best! :-)
