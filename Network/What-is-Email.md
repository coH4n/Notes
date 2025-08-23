## EMAİL ##
In this article, I will try to explain email, which has been a part of our lives since the very beginning of the internet. I believe it's important to understand how this system, which we use so frequently today, works, even in its simplest form.

**What is Email:**
We can define email as a communication method used to convey information over the internet. To make this definition a bit clearer, let's use a real-world example. In the old days, when a person wanted to send a letter, it was delivered by a mailman and placed in the recipient's mailbox. The recipient would then access the letter when they checked their mailbox. The email communication method is essentially an adaptation of that old system for the digital world. Here, the servers act as our digital mailmen. To get started, let's define what these servers are.

**IMAP and POP:** The protocol used to receive emails from the other party.

**SMTP:** The protocol used to send an email to the other party.

**What is POP3? (I would like to inform you that I copied the definition here from the internet, because it was explained exactly as I wanted):**

It is a protocol used by local email clients such as Outlook, Thunderbird, Windows Mail, and Mac Mail to communicate with a remote email server and download emails. These email clients usually have an option to keep or not keep a copy of the downloaded emails on the server. If you are connecting to the same email account from multiple devices, it is recommended that you keep a copy of the emails on the server. Otherwise, after one device downloads the email, it will delete that email from the remote server, and the other devices will not be able to access it.

**What are the advantages and disadvantages of the POP3 protocol?**

**advantages:**

-Since the email is downloaded to your device, you can view it even if you don't have an internet connection.

-It saves storage space on the mail server because emails are deleted after being downloaded to a device, provided that the configuration is set this way.

**Disadvantages:**

-In any situation that might happen to your computer, undesirable situations can arise (such as viruses, data loss, or crashes).

-The lack of synchronization. To elaborate on this point: although POP3 can be configured on multiple clients, the first client that accesses the POP3 server will get the email, and the other clients will not be able to. I have to say that if you are managing emails from multiple clients, I cannot say that the POP3 protocol is a very suitable protocol for this type of use.

### IMAP ###

We can say this is the protocol we use to access an email server through web applications (Gmail, Outlook, Yahoo), rather than through email applications running on our computer. The difference between this protocol and the POP3 protocol is that it works in a synchronized manner. This means emails are available for access by any client. This is, of course, because the emails are kept on the server.

**What are the advantages and disadvantages of the IMAP protocol?**

-It is possible to access emails from any desired client application.

-It operates in a synchronized manner. To explain this point with an example, an email deleted on one client will also be in a deleted state on other client applications.

**What are the differences between POP3 and IMAP protocols?**

Technically, the POP3 and IMAP protocols operate with the same underlying logic. Both protocols can be used depending on user preference. To state the most significant difference between these protocols in a few sentences: With the POP3 protocol, you can only view your emails from the device you set it up on, whereas IMAP allows you to access your emails from different devices, such as a computer, mobile phone, and tablet, not just from a single place.

### SMTP(Simple Mail Transfer Protocol) ###

The protocol used to communicate with a remote server to send an email from a client application or web application to the recipient's email server.

I've tried to explain what email servers are in their simplest form. Now, I will try to explain how this email communication works using a diagram.

<img width="951" height="313" alt="email-1" src="https://github.com/user-attachments/assets/c4a3ace9-df83-4557-8633-e21c75e25ebd" />

1.An email addressed to xyz@hotmail.com was sent to the other party by an email client named abc@gmail.com

2.First, the email uses the SMTP protocol to communicate and reach the sender's SMTP server.

3.The SMTP server receives the recipient's address (xyz@hotmail.com) and divides it into two parts: the recipient name xyz and the domain name hotmail.com. Since this recipient address is from a different domain, it needs to know the IP address of the recipient's SMTP server. To do this, it asks the DNS for this IP address.

4.DNS smtp.hotmail.com adresini soruyor

5.The DNS returns the IP address.

6.An email is being sent to the smtp.hotmail.com address over the TCP/IP protocol.

7.smtp.hotmail.com separates the incoming mail into two parts: the recipient name xyz and the domain name hotmail.com. The SMTP server then recognizes this email by using the domain name.

8.The email goes to the relevant mail server using the TCP/IP protocol on the smtp.hotmail.com side.

9.The mail.hotmail.com puts the incoming mail into the relevant user's mailbox.

10.The recipient indicates their desire to access their emails using either the IMAP or POP3 protocols via any client application.

11.mail.hotmail.com sunucusu ise ilgili kişinin posta kutusundai mailleri döndürüyor.

Of course, there are many other scenarios in the background, such as being blocked by a firewall, email spoofing, or spam. Email is a vast topic on its own; it's clear that understanding the information in the email codes, as well as the header and body sections, is a very important subject. However, my goal here was to convey the simplest information. Perhaps in the future, I may prepare a more detailed document on how email works.





