 ## CERTIFICATION AUTHORITY
Hello everyone. In this article, I will try to explain how Certificate Authorities (CAs), or as everyone knows them, SSL/TLS, work. I also want to state that in this article, I'll be using the term Certificate Authorities. It's also beneficial to note that before reading this, it would be useful to have some knowledge about asymmetric encryption and the HTTPS handshake process. You can find information on these topics on my GitHub page.

**Sertifika Otoriteleri Nedir:** 

When we want to communicate securely with a web server, we perform an action to send a secret key to the server using the public key that the server has declared. The server then decrypts this with its own private key, and a secure connection is established.

While this may not seem to have a problem, a malicious person on the network can perform a Man-in-the-Middle (MITM) attack and replace the server's public key with their own. In this case, the confidential data you want to send to the server will actually go to the attacker.

To get a better grasp of these points, you can look at the image below.
