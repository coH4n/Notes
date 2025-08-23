## DHCP ##   
If you are reading this article, you must have heard of the concepts of Public IP and Private IP addresses. To get into the topic, let's start by explaining what these concepts mean.

**Public Ip:** The IP address given to us by our internet service provider. This IP address identifies us on the internet.

**Private Ip:** The IP address that identifies us within our local network.

### What is DHCP ### 

We can say that DHCP is a protocol that provides a device connected to a network with an IP address and the necessary addresses to access the internet. These address types are the DNS Server IP address, Gateway IP address, and Subnet Mask addresses.

During the period before DHCP, IT professionals would manually assign IP addresses to new devices joining the network through the device's IP settings. If you imagine this process in a large company network with 200 computers, it would be a disaster. The IT staff would have a notepad with the names of the computers and their assigned IP addresses, and they would go around assigning them one by one. It would be especially frustrating if they accidentally assigned the same IP address to two computers, causing a collision on the network. The DHCP server prevents this waste of time and these errors by making these assignments dynamically (automatically).

### How does work DHCP ###

First of all, we should state that if we're explaining a protocol or something within the scope of networking, we need to have at least some knowledge of the OSI layers, especially the process of encapsulation. I believe you can find these topics in the Network Handbook section. Here, I'm going to explain the part you need to know if you're asked about it in an interview. When asked how DHCP works, the first thing that should come to mind is the DORA concept, which stands for Discover, Offer, Request, and ACK. It is through these states that we establish an agreement with a DHCP server when we connect to a network. So what do these terms mean? Let's briefly talk about them.

**Dhcp Dıscovery:** When a device like a computer joins a network, it sends a DISCOVER request as a broadcast to find the DHCP server. This request is directed to all DHCP servers on the network.

**Dhcp Offer:** The DHCP server that receives the discovery request responds with a DHCP OFFER, providing the IP address it has determined and the necessary address information for internet access. 

**Dhcp Request:** The client, which receives the DHCP server's offer, sends a DHCP Request to approve the IP address offer. This step also ensures that the selected IP address is reserved for the device.

**Dhcp Acknowledgment:** After receiving the request, the DHCP server sends a DHCP ACK message. This message confirms that the requested IP address has been approved.

I believe that if I explain these concepts using the diagram below, you will have a better grasp of the subject.

<img width="1000" height="577" alt="dhcp-1" src="https://github.com/user-attachments/assets/ae12c310-23ed-4241-af3a-7baaa404c362" />

If we were to summarize the diagram above in bullet points:

**1.** The client broadcasts a message on the network to find a DHCP server.

**2.** The DHCP server broadcasts the IP address it has determined to the client.

**3.** The client declares the determined IP address to the DHCP server using a unicast broadcast.

**4.** DHCP communicates to the other party that the requested IP address has been declared by the client via a broadcast message.

I tried to summarize the diagram in bullet points above, but there are some things I didn't explain, and I would like to clarify them here. As we saw in the diagram above, there is a term called transaction ID.

**Transaction ID:** We can say that it is a random 32-bit number determined by the client, which allows the other party to track our packets since we do not have an IP address yet.

There's an important point to note here, which is that a new transaction ID value is determined after the request-response phase. In other words, after the Discover-Offer phase, a new transaction ID value is also determined by the client for the Request-ACK phases. Additionally, the packets sent by the client use UDP.

When the client uses the UDP protocol, its packets go from port 68 to the DHCP server's port 67. The DHCP server's packets, in turn, go from port 67 to the client's port 68. The reason DHCP uses the UDP protocol is because of its speed.

**What does the DHCP Protocol provide?**

*IP address

*DNS address

*Gateway address

*SubnetMask address

*IP Address lease period(lease time)

**Which port uses DHCP**

Client Source Port: 68 -----------------------------> DHCP Server Port:67

Client Source Port:68  <----------------------------- DHCP Server Port:67

DHCP uses the UDP protocol because it is fast.

It should not be forgotten that, along with the IP address and the necessary address information for internet access, the DHCP server also provides a lease time. An IP address is never permanently assigned to a computer. Of course, there are other things to know in the background, such as the case of DHCP being on a different subnet or the header fields, but these would require a much more detailed article on DHCP. I have provided the information that should be conveyed in its simplest form when you encounter it in an interview. Perhaps I will write a detailed article on DHCP in the future.










