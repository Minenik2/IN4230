# 6th plenary session: 12.10.2023 #

In the first part of this session we focused on Home Exam 1. We discussed
various questions that the students had, providing clarifications and further
explanations where needed.

In the second part of the session, we shifted our focus to the Linux kernel
implentations of the Ethernet and ARP protocols, which are two protocols that we
are using in our MIP network stack.

[Here](https://github.com/torvalds/linux) you may find the Linux kernel source
tree. To be able to navigate through the Linux kernel source tree, one needs to
empower the editor with features such as `go to definition`, `go to
implementation`, `go to references` for the symbol under the cursor. Integrated
Development Environments (IDEs) provide these features out of the box and come
with built-in tools for code navigation. Check
[clangd](https://clangd.llvm.org/installation) in case you are using a
customizable text editor such as Vim, or Emacs.

[This](https://github.com/torvalds/linux/blob/master/net/ethernet/eth.c) file
contains the main implementation of Ethernet, whereas the ARP code can be found
[here.](https://github.com/torvalds/linux/blob/master/net/ipv4/arp.c)

Consider exploring the Linux kernel source code to learn about how other
protocols in the TCP/IP stack are implemented.

All the best! :-)

**P.S: Don’t forget, the deadline for submitting Home Exam 1 is October 16, 2023,
at 23:59 Oslo time.**
