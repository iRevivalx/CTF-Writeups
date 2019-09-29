# sharks on wire 1
Points: 150

# Category
Forensics

# Question
We found this packet capture. Recover the flag. You can also find the file in /problems/shark-on-wire-1_0_13d709ec13952807e477ba1b5404e620.

# Hints
Try using a tool like Wireshark
What are streams?

# Solution 
This was easily able to be done through the Wireshark tool. The hint gave us a clue that we have to follow the streams.
Following streams (such as UDP connections) in Wireshark gives a different view of network traffic.

![wireshark](https://user-images.githubusercontent.com/55530196/65829575-834aaa80-e2d9-11e9-8ad7-eebaf59630ef.png)

Therefore, we are able to find the flag in one of the packet.

``` Flag: picoCTF{StaT31355_636f6e6e} ```
