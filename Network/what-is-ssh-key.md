## What is SSH Key
In this article, I will talk about the SSH protocol, which we use very frequently in today's world and is known by everyone. To define SSH very briefly, we can say it's a method used to securely send commands to a computer over an insecure network. However, in this article, rather than explaining how the SSH protocol works, I will try to explain how we open a session with a remote computer—that is, the id_rsa and id_rsa.pub keys that everyone sees in CTFs.

Even though I create passwords with different combinations, I sometimes have my doubts about their security. I can't even imagine what simple password combinations people create, because the passwords they create might be the same as the ones in data breaches that occur all over the world. These passwords from data breaches can be accessed very easily through websites. For this reason, there is a much better and more secure alternative than using passwords in the SSH Protocol: SSH-KEY.

### How does ssh key work?:
The working principle of an SSH Key is based on the private key and public key that everyone hears so much about. To summarize what they are, we can break them down into the following sections:

**Private Key:** This is a type of key that's declared specifically for the individual and should never be shared with anyone. If someone else gets ahold of this key, they could impersonate the person and lead to undesirable situations.


**Public Key:** As its name implies, we can say this is a key that's perfectly fine for everyone to know.

Think of a scenario where we want to connect to our web server using the SSH protocol. For the other side to identify us, we need to have the Public Key, which we share publicly, on the relevant web server. I believe that if I explain this working principle step-by-step through a diagram, you will have a better grasp of the situation. (To better understand the events, it is necessary to know about asymmetric encryption, which is available on my website.)
