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















