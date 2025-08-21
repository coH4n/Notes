## VIRTUALIZATION

Today, I will try to explain what you need to know about virtualization in the simplest way possible.

**What is Virtualization:** 

To put it simply, it is the distribution of the functional power of a physical machine's hardware components across multiple virtual machines. I would also like to note here that you may hear the terms Cloud and Virtualization being used interchangeably, but they are absolutely not the same. Virtualization is a component of the Cloud, while the Cloud is a much larger structure than Virtualization.

The structure that makes it possible to virtualize the hardware components on this physical machine is called a hypervisor.

**What is Hypervisor:**

We can say it's a software that runs on a physical server or host computer, or a very lightweight operating system. To elaborate on this definition, the hypervisor running on the server side is referred to as a very simple operating system, whereas the hypervisor that runs on a normal user's side can be referred to as a software. I also adopt this definition because the hypervisor is divided into two categories. If we look at these through the diagram below:

<img width="512" height="136" alt="1" src="https://github.com/user-attachments/assets/ecdc26b8-f70e-4ee1-a2e2-7bf8ec7b2074" />

### TYPE 1(native or bare-metal hypervisors): ###

Bare-metal hypervisors are a type of hypervisor that is the operating system itself, rather than being built on top of a computer's operating system. I believe that if we look at the image below, we will get a better grasp of the situation.

<img width="519" height="264" alt="2" src="https://github.com/user-attachments/assets/b53f5319-1154-4da6-b1f5-67f486785342" />

We can say that Type 1 hypervisors are the most widely used type in the industry and are also the type of hypervisor used to virtualize servers today. Because this operating system, installed on the physical machine, has a very simple structure, we perform the new virtual machine configuration process through a management console.

I should note here that many people are under the impression that hypervisors are free. While it's true you can install the hypervisor on ten servers for free, you'll need a management console to configure them, and you will have to pay for a licensed one. In a very simple way, this is how I would explain a Type 1 hypervisor.

**TYPE 1 Advantages**

**It is generally faster than Type 2.** The reason for this is that Type 1 hypervisors have direct access to the underlying physical host's resources, such as the CPU, RAM, storage, and network interfaces. Therefore, the latency of Type 1 hypervisors is lower compared to Type 2.

**More resource-rich.** The Type 1 hypervisor does not need to share its core resources with a host operating system. This allows it to access a greater amount of CPU, RAM, storage, and network bandwidth. This feature also contributes to the performance of the Type 1 hypervisor.

**More secure.** Because there is no host operating system in a Type 1 hypervisor deployment, the attack surface of this deployment is much smaller than that of Type 2. This also means there will be significantly fewer security vulnerabilities that threat actors can exploit.

**More stable.** The absence of a host operating system also eliminates problems related to the host operating system that could affect the performance and availability of the virtual machines running on the hypervisor.

**TYPE 1 Disadvantages:**

**Installation and management are more difficult.** With a Type 1 hypervisor, you have to start from scratch because you are dealing with a bare-metal server. Even though you still need to install a host operating system in a Type 2 deployment, IT administrators (even junior administrators) are more familiar with operating system installation and configuration. For this reason, they may find managing Type 1 more difficult.

**It relies on an external management interface.** Typically, Type 1 hypervisors are managed through an external management interface. This means that to set up a Type 1 hypervisor, you'll need a separate system or computer.

### TYPE 2(hosted hypervisor): ###

Unlike a Type 1 hypervisor, a Type 2 hypervisor can be described as software built on top of the operating system layer. Although it may seem less prominent than the other hypervisor type in today's world, it is the hypervisor type adopted by typical users. Many of us accessing our virtual machines via VirtualBox is an example of a hosted hypervisor. To get a better grasp of the situation, we should look at the image below.

<img width="376" height="300" alt="thiss" src="https://github.com/user-attachments/assets/7ae8c1b6-9da2-4324-ad0e-11713eafe4c5" />

As you can see in the image above, the hypervisor acts as a bridge between virtualization and the operating system on the computer itself. If we were to look at the advantages and disadvantages of a TYPE 2 hypervisor...

**TYPE 2 Advantages:**

**More affordable.** The superior features of Type 1 hypervisors in terms of reliability, security, and efficiency come at a price. They are naturally more expensive. Conversely, Type 2 hypervisors are more cost-effective. Thus, although they can theoretically be used in enterprise use cases, the target market for Type 2 hypervisors is normally end-users.

**Easier to use.** Affordability is not the only reason Type 2 hypervisors are more suitable for end-users. Type 2 hypervisors are also generally easier to use. Therefore, they are more suitable for an audience with less technical knowledge.

**TYPE 2 Disadvantages:**

**Slower than Type 1.** Having a layer (the host operating system) between the Type 2 hypervisor and the underlying physical host increases latency. Therefore, Type 2 hypervisors are generally slower than their Type 1 counterparts.

**Not available as a host resource.** Since the Type 2 hypervisor shares the CPU, RAM, storage, and network bandwidth from the underlying physical infrastructure with the host operating system, the amount of resources the Type 2 hypervisor can access is limited compared to that of a Type 1.

**Less secure.** The presence of a host operating system increases the attack surface of the entire system. This means there are more vulnerabilities for threat actors to exploit.

**Less stable.** Any performance and availability issues in the host operating system will definitely affect the Type 2 hypervisor and its VMs running on it.





 


