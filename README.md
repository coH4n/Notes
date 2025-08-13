## Asymmetric encryption(Public Key Encryption)
In this article, I will explain asymmetric encryption, which is the backbone of cryptography. Before delving into asymmetric encryption, we need to understand how symmetric encryption works because asymmetric encryption and symmetric encryption are related and work together. You can find my article on this topic on my website. Asymmetric encryption, which was founded in 1970, was developed to address the security vulnerability brought by symmetric encryption. To briefly summarize the working principle of symmetric encryption, it involves the use of one key for both encryption and decryption. This is where the vulnerability of symmetric encryption arises. The recipient must also have the Secret Key that will be used for encryption. In an insecure world like the internet, direct access to this key is a vulnerability for us. And because of this, asymmetric encryption, also known as public-key cryptography, entered our lives. In asymmetric encryption, we have two types of keys: the Public Key and the Private Key.

### Public Key:
You can freely share this key everywhere, whether it is secure or not. When a person wants to send data to you, they use this key.
### Private Key: 
The key that should not be shared with anyone except the relevant person is the key that we can use to decrypt the data sent to us with our Public Key.

To explain the working principle, when a person wants to send data to us, they encrypt the data with our publicly available Public Key and send it to us. We can then decrypt the Public Key's encryption using our Private Key. If we want to send data to a person, we repeat the same process. I believe you will have a better grasp of the situation if you combine this working principle I have explained with the image below.

<img width="500" height="277" alt="1" src="https://github.com/user-attachments/assets/e7d372d8-492e-429a-8565-757c27dfdaae" />

If you have read an article about the working principle of asymmetric encryption before this one, I assume you have seen a text like this.
When we want to send data, we encrypt it with our Private Key and send it to the destination, and the destination decrypts the encryption with our Public Key.

Yes, this working principle is correct. The reason is that Private Key and Public Key can decrypt each other. However, since the Public Key is held by everyone, this creates a security problem. When you read forums like Stack Overflow or Quora, a lot of people discuss this issue. I think it would be useful to know this because, in interviews, some of our instructors may ask you to explain this situation in addition to the question, "What is asymmetric encryption and how does it work?" But generally, the answer to this question is the working principle I explained above.

The biggest problem with asymmetric encryption is speed. I state this in every one of my articles. In the computer world, speed is very important. Think about it, when we want to send data, are we going to constantly encrypt it with a Public Key and send it to the other party? Of course not. This is where the situation arises where asymmetric encryption and symmetric encryption work together. In symmetric encryption, we know that the key used for encryption must be the same as the key used for decryption. So how will the recipient securely get this secret key? We solve this problem with asymmetric encryption. We deliver the secret key we want to send to the other party by encrypting it with the other party's Public Key. I believe you will have a better grasp of this situation with the example below.

<img width="1299" height="326" alt="2" src="https://github.com/user-attachments/assets/c1fe8610-ec39-4d31-9d5b-026b5edcdae6" />



