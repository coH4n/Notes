## DNS ##

In this article, I will explain one of the most important protocols of today's internet world: DNS (Domain Name System). If you ask me, it might be the most important one, because if it weren't for the Domain Name System, we would probably only be able to access 15 or 20 websites in total. I think if I explain this sentence by going through ancient times, you will grasp the subject better.

Throughout history, humans have communicated with each other using letters, and the reason for this is based on a scientific fact: letters take up much less space in memory than numbers. When someone asks you your name, is it easier to say a word made up of letters or a number made up of digits? You would answer this yourself with a collection of words made up of letters.

Unlike humans, computers communicate with each other using numbers. When you want to go to a website today, you are actually going to the address that is the numerical equivalent of that website, which is the IP address we know. The system that performs this operation is the Domain Name System, which we can define as the system that translates a domain name into an IP address.

In a world without DNS, imagine a scenario where we constantly type an IP address into the URL bar. What would that be like? Most likely, we would have a notepad on our computer and keep a list of IP addresses. This was actually a method used in the days when landline phones were common. Next to the home phone, there was always a phone number and a name that defined that phone number.

Based on this example and moving away from the definition in the computer world, if we were to define DNS, we could say it's a system that translates the language people understand into the language a computer understands.

### How does DNS work? ### 

You stated that DNS is the system that translates a domain name into an IP address. So, how does it work? If you've searched for "how DNS works" before this article, you've probably seen a diagram similar to the one below, with Root Servers, TLD Servers, and Name Servers.

Yes, it's easy to understand from a diagram or visual, but one of the first questions I had was, "What are these determined by?" The answer to this question lies in knowing about FQDN (Fully Qualified Domain Name). The Turkish translation is "Tamamen nitelikli alan adı." If I were to go over the FQDN example below...

<img width="1210" height="231" alt="dns-1" src="https://github.com/user-attachments/assets/b5f60b26-ba83-4077-b4ef-e1329f768d8a" />

DNS servers use the FQDN (Fully Qualified Domain Name) address we saw above to parse incoming DNS requests within their authorized scope and find the corresponding IP address. This process works from the rightmost dot to the leftmost Second-Level Domain.

To truly understand the FQDN structure, you need to examine the DNS tree structure, but I won't go into that here because I want to explain DNS to you in the simplest and most understandable way possible. However, in the diagram below, which explains a DNS request from start to finish, I believe you'll be able to visualize how it all works.

<img width="1016" height="600" alt="dns-2" src="https://github.com/user-attachments/assets/cb3f2cfe-5b3d-4a88-8997-ad02d20dcad6" />

**1-** A request is made for hedef.com by the client.
**2-** The Internet Service Provider (ISP) checks its own cache.
**3-** The IP address that is not in the cache is sent to the DNS resolver (name server).
**4-** The DNS resolver asks the Root server.
**5-** The root server, upon seeing the .com extension, redirects to the IP address of the TLD server that knows the records related to .com.
**6-** The DNS Resolver asks the relevant TLD server for the IP address of the hedef.com domain.
**7-** The TLD server, after seeing the .com. extension, redirects to the IP address of the NS (Name Server) that holds the records for hedef.com.
**8-** The DNS resolver asks the relevant Name Server for the IP address of the hedef.com domain.
**9-** The Name Server sends the A record of the hedef.com domain to the DNS resolver.
**10-** The DNS Resolver sends the IP address to the ISP.
**11-** The ISP caches the relevant IP address.
**12-** The ISP sends the relevant IP address to the client.
**13-** Client,ilgili IP adresini ön belleğine kaydediyor.

The situation described above can be called a diagram and bullet point definition of how DNS works. So, what are the roles of these DNS servers within themselves? To explain them in very short headings...

**Root Server:**

It sits at the top of the DNS system and is the first address where the process of converting a domain name to an IP address begins. There are a total of 13 Root Servers in the world.

**Top-Level Domain (TLD) Server:**

The server that holds the address of the relevant Name Server for the IP address to be learned. TLD servers are also divided into branches such as commerce (.com), education (.edu), and so on.

**Name Server:**

The server where the DNS records of the desired IP address are stored. This server returns the relevant server's IP address to the client, declaring that the DNS process has been successfully completed.

A DNS process occurs under three conditions. I explained the first condition using the diagram above. To explain the other two conditions using a diagram as well...

1.If an IP address is found in the client's cache.

<img width="983" height="98" alt="dns-33" src="https://github.com/user-attachments/assets/fb028aa4-197d-4af1-83df-0a4eb68fddbe" />

2.If an unknown IP address is in the client's cache but is in the ISP service provider's cache.

<img width="750" height="145" alt="dns-4" src="https://github.com/user-attachments/assets/3b33cb75-864e-4ece-bbd2-86f1202313eb" />

By caching well-known IP addresses, DNS resolver servers are prevented from being overloaded. And even more importantly, we save time. In the network world, time is always very important.

In this article, I tried to explain the working principle of DNS in the most understandable way possible. Of course, there are questions that need to be asked, like what the role of SSL/TLS is in the background, or how the Shared Hosting situation works, but if a question like this comes up in an interview, I believe you can answer it very easily using this diagram.












