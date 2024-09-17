# 5th plenary session: 05.10.2023 #

At the beginning of the plenary session, we encountered technical issues with
the HDMI cable, so it was impossible to project onto the screen. Despite trying
various troubleshooting techniques, such as restarting devices and utilizing
different adaptors and HDMI cables, all we could see on the wall was a blue
screen with a "no signal" error message.

I even thought I could use the Windows PC and started setting up an SSH
	connection in Putty, but that didn't work out as intended.

Although this situation caused a delay, it provided a valuable lesson to stay
away of Windows machines. :D

We then continued the session in another room and focused on two main aspects:

	- Home exam 1
	- Implementing a Wireshark dissector for our Hi Protocol, which we had discussed in the previous session.

We discussed about a Mininet script that I had previously shared on Mattermost for
testing in Home Exam 1. The script automates the initialization of MIP daemons
and applications with appropriate argument sequencing, enabling the evaluation
of specific scenarios:

	- A pings B
	- C pings B
	- A pings C (expecting a timeout)
	- A pings B again (the reported Round-Trip Time should be shorter due to ARP cache utilization)

You may find the script
[here](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p5_05-10-2023/he1/he1-mn-script.py).
In addition,
[Here](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p5_05-10-2023/he1/he1-grading-guidelines.md)'s
a summary of the implementation requirements for Home Exam 1.

The last part of the session was focused on implementing a wireshark dissector
for our HiP protocol, following the tutorial in
[this](https://mika-s.github.io/wireshark/lua/dissector/2017/11/04/creating-a-wireshark-dissector-in-lua-1.html)
webpage.

Here is the final code of the plugin written in Lua. Place the `hip.lua` file in
`~/.local/lib/wireshark/plugins/` and run the Mininet project in the `synack`
directory. Wireshark will be able to capture the HIP\_SYN and the HIP\_SYNACK
packets exchanged between the client and server and print the correct packet
type. See the screenshots in the
[wireshark-plugin](https://codeberg.org/kr1stj0n/plenaries-in3230-in4230-h23/src/branch/main/p5_05-10-2023/wireshark-plugin)
directory.

Homework: Modify the Lua code of the plugin to capture MIP packets.

All the best! :-)
