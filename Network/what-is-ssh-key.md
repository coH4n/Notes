## What is SSH Key
In this article, I will talk about the SSH protocol, which we use very frequently in today's world and is known by everyone. To define SSH very briefly, we can say it's a method used to securely send commands to a computer over an insecure network. However, in this article, rather than explaining how the SSH protocol works, I will try to explain how we open a session with a remote computer—that is, the id_rsa and id_rsa.pub keys that everyone sees in CTFs.

Even though I create passwords with different combinations, I sometimes have my doubts about their security. I can't even imagine what simple password combinations people create, because the passwords they create might be the same as the ones in data breaches that occur all over the world. These passwords from data breaches can be accessed very easily through websites. For this reason, there is a much better and more secure alternative than using passwords in the SSH Protocol: SSH-KEY.

### How does ssh key work?:
The working principle of an SSH Key is based on the private key and public key that everyone hears so much about. To summarize what they are, we can break them down into the following sections:

**Private Key:** This is a type of key that's declared specifically for the individual and should never be shared with anyone. If someone else gets ahold of this key, they could impersonate the person and lead to undesirable situations.


**Public Key:** As its name implies, we can say this is a key that's perfectly fine for everyone to know.

Think of a scenario where we want to connect to our web server using the SSH protocol. For the other side to identify us, we need to have the Public Key, which we share publicly, on the relevant web server. I believe that if I explain this working principle step-by-step through a diagram, you will have a better grasp of the situation. (To better understand the events, it is necessary to know about asymmetric encryption, which is available on my website.)

<img width="900" height="220" alt="last-ssh" src="https://github.com/user-attachments/assets/7e3240b2-eb55-4930-ac99-e70d53e4832e" />

To summarize the situation above in bullet points, we can say:

**1:** We declare our intention to connect to the relevant server via the SSH protocol by using our Public Key.

**2:** The relevant server then compares the public key we've provided with the public key list it has and approves it.

**3.** To establish the connection, the server generates a random string, encrypts it with the public key to verify the other party's identity, and sends it to the other party.

**4:** The client then decrypts the public key using its private key.

**5:** The client sends this value to the server.
 
**6:** The SSH connection is established.

We can say this is why the commonly seen id_rsa and id_rsa.pub keys are found in the same directory. It is also worth noting that the values I provided for the Public and Private Keys are not real. In the real world, an example of these values is available in the image I provided below.

<img width="530" height="556" alt="last-ssh-2" src="https://github.com/user-attachments/assets/e3c4c609-649a-402a-aa89-836410c24cc3" />

Of course, if you want to connect using the SSH protocol, there is specific software available for your operating system. If you're using macOS or Linux, you can access this software through the terminal, while for Windows, the most commonly used application is PuTTY. It's important to note that you must be very careful about the applications you download on Windows, as there are many fake applications on the market. This could cause your private key to fall into the wrong hands or lead to a virus on your computer.




