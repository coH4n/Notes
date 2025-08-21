## What is Traceroute and how does it work? ##

First, let's say that to understand how the traceroute program works, I think we need to have a basic understanding of how the internet works. Of course, I won't explain that here; you can find that article on my website. However, to make the topic more understandable, I should briefly mention this: when we, as a client, send a packet to the other side, these packets reach their destination via routers. These routers have IP addresses that define them. Thanks to these IP addresses, routers exchange packets with each other.

The purpose of the traceroute program is to learn the IP addresses of these routers. It does this by leveraging the Time To Live (TTL) header found in IP packets. So what is the Time To Live header? It's an IP packet header used to drop unnecessary packets in the network world. To give a more illustrative example, when you make a request to a certain IP address, if that IP address is not active, the packet you sent is dumped thanks to the Time To Live header.

In a scenario without Time To Live, that packet would create traffic and consume bandwidth everywhere it passes, which would be a disaster, considering that time is very valuable in the network world. This is exactly why the traceroute program uses the Time To Live header to learn the IP addresses of the routers. To explain the working principle of the Time To Live header using the diagram I drew below, the TTL duration is decreased by one at every router it passes through. The default TTL duration is 64.

<img width="607" height="87" alt="traceroute-1" src="https://github.com/user-attachments/assets/495c36b4-b001-470d-8b2c-7ae601bf82f3" />


If the Time to Live duration equals 0 before the packet reaches its destination, a feedback message is sent to the recipient's IP address from the router where the packet was dumped. This is what Traceroute leverages: in a scenario where it sets the Time to Live header of the packet it sends to the destination to 1, when the packet arrives at the first router, the packet is dumped, and Traceroute determines the router's IP address from the router's feedback packet. It then repeats this process until it reaches the destination.

<img width="658" height="156" alt="traceoute-2" src="https://github.com/user-attachments/assets/4c3cd7b3-84e9-4a18-ab45-802901b1dfbf" />

And of course, sometimes when the traceroute program is running, you might see a "*" character or it might get stuck at a certain point. We can think of this as the router not responding to ICMP protocol requests or being blocked by a Firewall. Although the traceroute program may seem very simple, it's a very cleverly designed program.
