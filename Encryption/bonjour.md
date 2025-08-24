
## Symmetric Encryption:
In this article, I will explain symmetric encryption, a form of encryption that dates back thousands of years. I will try to present its working principle in the simplest way possible, without going into the mathematical basis. Symmetric encryption is a form of encryption that we use very often in today's world. Think about it: when you leave your house and lock the door, if someone else has a copy of your key (a sibling, a parent, etc.), they can open the door. Based on this example, in the world of the internet, when we want to send data with a password, the key used to encrypt the data is also used for decryption. To explain this with an example:

<img width="513" height="248" alt="1" src="https://github.com/user-attachments/assets/8a8316f9-56ec-4bfe-992f-b6872c3bad35" />

I believe this is the simplest explanation of the working principle of symmetric encryption, which we hear so often every day. Symmetric encryption is a type of encryption that we use very frequently in data transfer in today's world. The reason for this is that it is many times faster than other forms of encryption. When I first learned this, I asked myself, "How does the key I use to encrypt get to the other party?" This is where the vulnerability of symmetric encryption arises. When we want to send data, we need to agree with the other party on which secret key to use. If there is someone sniffing the network during that agreement and they get a hold of the secret key, they can decrypt all the encrypted messages and compromise the privacy. I believe you will have a better grasp of the situation with the example below.

<img width="770" height="132" alt="2" src="https://github.com/user-attachments/assets/0cde0a1f-675d-47aa-a288-df4efb3dc349" />

This was the biggest problem that symmetric encryption brought, and because of this problem, asymmetric encryption entered our lives. I won't explain it here, but for a very brief piece of information, I can say that we deliver our secret key value to the other party using asymmetric encryption.

In order to get a better grasp of this topic, I recommend you look at my articles on Asymmetric Encryption and SSL/TLS on my github adress. Of course, it is also necessary to discuss symmetric encryption types, especially AES, DES, and bit concepts, but for now, knowing this will be beneficial for you.
