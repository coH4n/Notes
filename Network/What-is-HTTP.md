## HTTP ##

In this article, I will try to explain one of the oldest internet protocols, the HTTP protocol. In my opinion, the HTTP protocol is one of the worst protocols I know, and the reason for this is that it's a stateless protocol. In other words, it doesn't remember anything about the previous HTTP request-response lifecycle. Of course, it's also important to remember that the HTTP protocol was originally created for the purpose of document transfer, given the year it was developed.

With the development of the internet and the introduction of World Wide Web technology, technologies that could work with the HTTP protocol evolved. Examples of these include cookies, tokens, and so on. However, in this article, I will try to present the process that the HTTP protocol goes through when making a request to a website—the well-known request-response state.

First, let's list the features of the HTTP protocol in headings.

**-Standart Web Transfer Protocol:** A protocol used to access any file on the web.

**-HTTP Port Number is 80:** This means that all HTTP-related traffic is sent to and received from port 80.

**-Transfer Hypermedia Document:** It enables the transfer of files such as text, images, audio, video, and other multimedia files over the web via the HTTP protocol.

### How Does work HTTP: ###
The working principle of HTTP is based on request-response behavior. To understand this behavior, we can look at the image below.

<img width="640" height="99" alt="http-1" src="https://github.com/user-attachments/assets/af4eecf0-87f7-450c-87e0-5c6fa127a445" />

The image you see above is a type of visual that everyone sees very frequently on the internet, but to get a better grasp of the situation, I will proceed using the image below.

<img width="687" height="96" alt="http-2" src="https://github.com/user-attachments/assets/57e839e2-4258-44d6-be83-c989cca89e71" />

**Connection:** To understand what's under this heading, we need to know basic networking, because the events that take place here are things like DNS and the three-way handshake. I won't explain them here, but you can find them on my website.

**Request:** This is the state of a client requesting information from a server.

**Response:** This is the state of the server returning information to the client.

**Close:** This is the state where one or both parties terminate the transaction.

I will explain the Request and Response headings here, but the Connection part should definitely be known as well.

### HTTP REQUEST: ###



