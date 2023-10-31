<a href="https://zupimages.net/viewer.php?id=23/44/azjd.jpeg"><img src="https://zupimages.net/up/23/44/azjd.jpeg" alt="" /></a>



1. What is a server?

A server is generally located in a data centre.
It can be physical or virtual.
It runs an operating system.

-------------------------------------------------------------------------------------------------------

2. What is the role of a domain name?

The role of a domain name is to translate the domain name registration into an IP address.

-------------------------------------------------------------------------------------------------------

3. What type of DNS record is www in www.foobar.com?

The www DNS record in www.foobar.com is an A record, because it resolves to an IP address.

-------------------------------------------------------------------------------------------------------

3. What is the role of the web server?

The role of a web server is to serve web pages, i.e. static content.

-------------------------------------------------------------------------------------------------------

4. What is the role of an application server?

The role of an application server is to calculate dynamic content.

-------------------------------------------------------------------------------------------------------

5. What is the role of the database?

The role of the database is to store the application data.

-------------------------------------------------------------------------------------------------------

6. What does the server use to communicate with the computer of the user requesting the website?

The server uses the network, in particular the TCP/IP protocol, to communicate with the computer of the user requesting the website.
*TCP is a reliable, connection-oriented communications protocol. It divides data into packets, sends them across the network and reassembles them in the correct order at their destination. It also ensures that data is transmitted error-free and in the correct order.

-------------------------------------------------------------------------------------------------------

Regarding infrastructure problems :

SPOF (Single Points of Failure):

1. The HAProxy server is a SPOF because it is not redundant. In addition, the lack of redundancy in the MySQL database makes it another single point of failure.
Maintenance downtime:

2. The website would be temporarily down when new code is deployed and the web server needs to be restarted. This could lead to interruptions for users.
Inability to scale to handle heavy traffic:

3. This infrastructure is not scalable and cannot handle large amounts of incoming traffic, which is a potential problem when the site experiences a sudden increase in traffic.
