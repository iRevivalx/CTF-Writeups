# Super Secret Communications
96 Points obtained at that moment

# Category
Forensic

# Question
Okay, the note's right here. Hold on... uh... Okay.
You'll never discover our secrets! Our method is so secure you'll never get in! We've even given you a full packet capture of everything we sent! Do your worst, ELVES!
Yeah, we don't know either. Just try to find the secret message.

[captured.pcap](https://drive.google.com/file/d/1prJGtolMEdmBf9QwdZliT713ozSjoh79/view)

Author: plaaosert

# Solution
Wireshark is a network protocol analyzer that is frequently used in CTF challenges to examine network traffic that has been captured. Wireshark records traffic using the PCAP filetype. PCAPs are frequently distributed as part of CTF challenges in order to provide recorded traffic history.

When you first open wireshark, you can see the network traffic presented in the sequence in which the packets were captured. Packets can be filtered by protocol, source IP address, destination IP address, length, and other factors.

![Wireshark](https://user-images.githubusercontent.com/55530196/145665736-ad5599dd-444f-485d-8f56-76592eac739f.png)

Upon examining some of the packets, i am able to clearly see some of the data that has contains some information to solving the challenge. Therefore, i decided to follow a particular TCP conversation between the hosts. I am able to do so by applying filters, which you can simply just enter the constraining factor such as ```tcp.stream eq 0```, in the display filter bar or you can click the **Analyse** tab in the toolbar and then click the **Follow** and subsequently the **TCP Stream**.

After further examination, i was able to figure out that flag is it is broken into 10 fragments as highlighted in yellow. 
![Wireshark TCP Stream](https://user-images.githubusercontent.com/55530196/145666098-4b6200df-eb4b-426b-88a0-694d7a9372b3.png)

The flag fragments are consisted in the order of: 
1. X-M 
2. AS{y0 
3. u_cr4C 
4. K4d_ 
5. thE_c0 
6. d3!_ 
7. afa 
8. 03 
9. 819d 
10. ef2f}


By piecing together the fragments, i was able to correctly deduced the correct flag.

``` Flag: X-MAS{y0u_cr4CK4d_thE_c0d3!_afa03819def2f} ```
