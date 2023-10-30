<img/>https://ibb.co/Lv9NfbW<img>
What is a server ?
A server is a computer specially configured to provide services, data or resources to other computers, usually called clients, via a network.
---------------------------------------------------------------------------------------
What is the role of the domain name ?
The domain name (in this case, "foobar.com") is a human-readable address that maps the server's IP address to a user-friendly name. This means that when users access www.foobar.com, the browser knows where to find the associated server using the DNS record.
---------------------------------------------------------------------------------------
What type of DNS record www is in www.foobar.com ?
The "www" DNS record is a sub-domain that points to the IP address of the server. This allows users to access the website using the URL "www.foobar.com".
---------------------------------------------------------------------------------------
What is the role of the web server ?
The web server, in this case Nginx, is responsible for receiving requests from clients (users' web browsers) and returning the appropriate web pages from the site. It manages the processing of HTTP requests, file retrieval, communication with the application server, and returns responses to the client.
---------------------------------------------------------------------------------------
What is the role of the application server ?
The application server is responsible for processing the business logic of the web application. It interacts with the web server to generate dynamic web pages from the application code, generally written in a programming language such as PHP, Python, Ruby, etc.
---------------------------------------------------------------------------------------
What is the role of the database ?
The database, in this case MySQL, stores and manages the data required for the website. This includes user information, site content and other relevant data. The application server communicates with the database to retrieve or store data according to the needs of the application.
---------------------------------------------------------------------------------------
What is the server using to communicate with the computer of the user requesting the website ?
The server uses the HTTP (Hypertext Transfer Protocol) to communicate with the user's computer. When a user enters the URL in the browser, an HTTP request is sent to the server, and the server responds with the requested web page or resources.
---------------------------------------------------------------------------------------
You must be able to explain what the issues are with this infrastructure:
SPOF ?
Single Point of Failure (SPOF): If the single server fails, the entire website becomes inaccessible, leading to downtime and potential loss of business.
---------------------------------------------------------------------------------------
Downtime when maintenance needed (like deploying new code web server needs to be restarted) ?
Deploying new code or restarting the web server could lead to temporary downtime, impacting user experience and accessibility.
---------------------------------------------------------------------------------------
Cannot scale if too much incoming traffic ?
A single server may not handle a significant increase in traffic efficiently, leading to slow response times or potential crashes during traffic spikes.
---------------------------------------------------------------------------------------
To address these challenges, a more robust infrastructure setup would involve implementing load balancing, redundancy, and possibly a cloud-based solution to scale resources dynamically based on traffic demands. Additionally, employing techniques like zero-downtime deployment and high availability setups can minimize disruptions during maintenance.