### How does work NAT/PAT ###
Hello everyone, when I was a kid and would go to internet cafes after school, to look cool, I'd open the command prompt and type 'ipconfig'. The IPv4 address I saw there was 192.168.1.10, but when I went online and checked my IPv4 address, something else would appear. At the time, I thought this was impossible. Back then, I used to wonder how that happened. Today, I will explain the working principle of NAT, the concept that makes this possible. First, if we were to start with the definition of NAT, on Wikipedia it is described as...

### Network Address Translation (NAT) ### 
It is the process by which a computer on a TCP/IP network changes the network address information in an IP packet header, by re-mapping its address space IP when exiting to another network via a routing device.

In simpler terms, we can define it as the structure that translates a Private IPv4 address into a Public IPv4 address. One of the main reasons NAT came into our lives is undoubtedly the trouble caused by IPv4 addresses. I won't go into IPv4 in detail, as that's a separate topic, but to put it simply, we have a limited number of IPv4 addresses—4,294,967,296 in total—which is insufficient for today's world. This is because the internet has become more popular over the years, and many things in today's world can connect to the internet. If a device is going to connect to the internet, an IPv4 address is necessary. To solve these problems, the concepts of Private IP, Public IP, and Network Address Translation came into our lives.

**Private IPv4: We can say that Private IPv4 addresses are the IPv4 addresses assigned by a DHCP server within a Local Area Network.** To put it in a way that everyone can understand for Private IPv4: Imagine we have a home network with 5 people connected to it. This means there are 5 Private IPv4 addresses. The presence of these 5 Private IPv4 addresses together represents a Local Area Network.

**Public IPv4: We can say that it is the IPv4 address found under the name of Wide Area Network, which identifies us on the Internet. This IPv4 address is given to us by our Internet Service Provider.** To put it in a way that everyone can understand regarding a Public IPv4 address: You can think of it as the modem in your home. The modem that our Internet Service Provider gives us has an IPv4 address, and this IPv4 address is the Public IPv4 address that identifies us on the internet.

### Network Address Translation ### 
A mechanism that works via a router to translate between a Private IPv4 address and a Public IPv4 address.

NAT, on the other hand, is divided into three types:

**▪Static NAT**

**▪Dynamic NAT**

**▪NAT Overloading or NAT/PAT(Port Address Translation)**

NAT/PAT is the one we use most today, but I will also briefly explain the features of Static and Dynamic NAT.

**Static Nat:** Static NAT is not the type of NAT we use today. Its working principle is to assign a unique Public IPv4 address to each Private IPv4 address. I will try to explain this using the diagram I have drawn.

<img width="513" height="169" alt="resim-1" src="https://github.com/user-attachments/assets/73c69d0d-ef11-40ee-98df-6424b81d07b1" />

Here, we have a pool of Private IPv4 addresses and a pool of Public IPv4 addresses. We need to get as many Public IPv4 addresses from our Internet Service Provider as we have users on the Local Area Network.

<img width="580" height="350" alt="resim-2" src="https://github.com/user-attachments/assets/36f49110-e30c-40d0-ad33-05d379532ec2" />

Looking at the Static NAT working diagram, when data leaving PC1 reaches the router, a conversion from the Private IPv4 address to the Public IPv4 address happens with NAT running on the router. As I mentioned, Static NAT is not a NAT process we see in today's world. This is because of its one-to-one and manual operation, and the fact that the IPv4 address pool is configured manually.

**Dynamic NAT:** We can say that its working principle is similar to Static NAT, with the only difference being that it operates under a one-to-one/automatic rule. We have a pool of Public IPv4 addresses, but the key difference is that we don't need to specify a particular Private IPv4 address pool. The logic is 'first come, first served' for the Public IPv4 address, and these processes happen automatically.

**NAT Overloading veya NAT/PAT:** This is the situation of using a single Public IPv4 address for multiple Private IPv4 addresses. This process is made possible by using port numbers. To explain this with a diagram...

First, we have a pool of Private IPv4 addresses.

<img width="580" height="450" alt="resim-3" src="https://github.com/user-attachments/assets/0cadaccf-2418-4e3a-9d60-2d7b557cc052" />

When PC1 with the IP address 192.168.1.10 wants to send data to the internet through port 3000, the NAT/PAT mechanism first writes the Private IPv4 address and port number to the NAT table in their original form. Then, it converts the Private IPv4 address to a Public IPv4 address, and if necessary, it also translates the port number. Afterwards, it finds its place in the table corresponding to the original address. Now, the data is sent to its destination.

Actually, it has a very simple working mechanism. To provide a clearer summary of the working principle of NAT/PAT in this part of the article: Network Address Translation does nothing more than convert a Private IPv4 address into a Public IPv4 address. The mechanism that enables multiple Private IPv4 addresses to use a single Public IPv4 address is Port Address Translation. By using port numbers, we create a list and allow everyone on the Local Area Network to access the internet.

It's also important to remember that on most NAT devices, the NAT session limit is restricted by the available memory. Each NAT translation takes up about 160 bytes of memory on the device. More NAT processes mean more load on the CPU, which can lead to undesirable results, such as packet loss and ping delays.

Of course, there are many questions to be asked about what default gateway, TCP, and UDP do in the background of this process, but this is the working principle of NAT in short.












