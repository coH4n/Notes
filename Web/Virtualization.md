## VIRTUALIZATION

Today, I will try to explain what you need to know about virtualization in the simplest way possible.

**What is Virtualization:** 

To put it simply, it is the distribution of the functional power of a physical machine's hardware components across multiple virtual machines. I would also like to note here that you may hear the terms Cloud and Virtualization being used interchangeably, but they are absolutely not the same. Virtualization is a component of the Cloud, while the Cloud is a much larger structure than Virtualization.

The structure that makes it possible to virtualize the hardware components on this physical machine is called a hypervisor.

**What is Hypervisor:**

We can say it's a software that runs on a physical server or host computer, or a very lightweight operating system. To elaborate on this definition, the hypervisor running on the server side is referred to as a very simple operating system, whereas the hypervisor that runs on a normal user's side can be referred to as a software. I also adopt this definition because the hypervisor is divided into two categories. If we look at these through the diagram below:

<img width="512" height="136" alt="1" src="https://github.com/user-attachments/assets/ecdc26b8-f70e-4ee1-a2e2-7bf8ec7b2074" />

**TYPE 1(native or bare-metal hypervisors):**

Bare-metal hypervisors are a type of hypervisor that is the operating system itself, rather than being built on top of a computer's operating system. I believe that if we look at the image below, we will get a better grasp of the situation.

<img width="519" height="264" alt="2" src="https://github.com/user-attachments/assets/b53f5319-1154-4da6-b1f5-67f486785342" />

We can say that Type 1 hypervisors are the most widely used type in the industry and are also the type of hypervisor used to virtualize servers today. Because this operating system, installed on the physical machine, has a very simple structure, we perform the new virtual machine configuration process through a management console.

I should note here that many people are under the impression that hypervisors are free. While it's true you can install the hypervisor on ten servers for free, you'll need a management console to configure them, and you will have to pay for a licensed one. In a very simple way, this is how I would explain a Type 1 hypervisor.
