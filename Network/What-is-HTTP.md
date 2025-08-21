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

### HTTP Request: ###

I mentioned that it's a state of a client requesting information from a server. So how does it determine this request? First, before explaining that, let's say that HTTP request types are divided into two. These are:
<img width="563" height="114" alt="http-3" src="https://github.com/user-attachments/assets/05304ed3-ffd6-40ff-8b6f-0eec63d08fb7" />

**Simple Request:** We can say that a Simple Request consists of a single GET line that names the requested page, without a protocol version. To make this more meaningful, we can look at the Simple Request diagram below.
<img width="604" height="105" alt="http-4" src="https://github.com/user-attachments/assets/7dec3455-ce87-494f-9016-4a9d7eb1ec8d" />


**Full Request:** In a Full Request, the protocol version is also shown in the GET request line. To make this more meaningful, we can look at the Full Request diagram below.

<img width="657" height="108" alt="http-5" src="https://github.com/user-attachments/assets/01661c67-4362-452d-bec3-d166327ef8c9" />

And based on this, to know the answer to the question of what determines the type of an HTTP request, we need to look at the HTTP request message format diagram below.

<img width="121" height="180" alt="http-6" src="https://github.com/user-attachments/assets/ce3b9061-6160-406c-a850-53c81fea9940" />

If we were to look at what each of the headings in the diagram does, one by one, and summarize them as subheadings...

<img width="613" height="124" alt="http-7" src="https://github.com/user-attachments/assets/93542eb0-43f5-41d0-9fb1-85016260a4a4" />

And if we translate these into a language we can understand...

<img width="554" height="74" alt="http-8" src="https://github.com/user-attachments/assets/588f1bf6-f8a0-4876-a5ec-d115a138aded" />

**Http Request Type:** As a client, we specify the type of request we'll make to the other party using HTTP request types. The most commonly used types are GET (to retrieve data) and POST (to send data). If you'd like to look at other HTTP request types, you can find them at this address: https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods.

**Resources:** The URL defines the address we use to access a specific website in the web world. Let's use an example.

<img width="254" height="186" alt="http-9" src="https://github.com/user-attachments/assets/21b74726-333c-411c-ab66-89e05b337c37" />

Of course, because a computer can't read a domain address like this, the relevant server's IP address is determined by DNS, and then a request is made to that address by the HTTP protocol. In such a case, the following diagram appears.

http://facebook.com --------------------------------> http://157.240.196.35/index.html

I want to give a small piece of information here: the reason we don't see the port number in the URL bar is that TCP protocol defaults to port number 80. If I wanted to make the HTTP diagram above a little more explanatory...
**Protocol://Host:Port/Path**

**HTTP Version:** It specifies the HTTP version used. There are differences between HTTP versions, which you can find on my website.

To get a better grasp of the headings explained in the diagram, here is a real-world example of the diagram described below.

<img width="645" height="291" alt="http-10" src="https://github.com/user-attachments/assets/9ee5d221-4d0f-4f42-a6ce-fe3c4604bbe5" />


