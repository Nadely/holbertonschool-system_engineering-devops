<a href="https://zupimages.net/viewer.php?id=23/44/pcat.jpg"><img src="https://zupimages.net/up/23/44/pcat.jpg" alt="" /></a>
1. For each additional element, why do you add it:

The three firewalls are added to filter incoming and outgoing network traffic, enhancing security.
The SSL certificate is added to enable a secure and encrypted HTTPS connection between users and the server, ensuring data confidentiality.
The three monitoring clients are added to monitor system performance, availability, and security.
What are firewalls for?
Firewalls are used to filter network traffic, controlling which data packets are allowed to enter or exit a machine or network. They enhance security by preventing unauthorized access.

-------------------------------------------------------------------------------------------------------

2. Why is traffic routed through HTTPS?

Traffic is routed through HTTPS to ensure the security of data in transit. HTTPS encrypts communications, making data unreadable to anyone intercepting the traffic, thereby enhancing confidentiality.

-------------------------------------------------------------------------------------------------------

3. What is the purpose of monitoring?

Monitoring is used to check system performance, availability, and security. It helps detect issues, bottlenecks, potential failures, and enables a quick response to maintain optimal operation.

-------------------------------------------------------------------------------------------------------

4. How does the monitoring tool collect data?

The monitoring tool collects data using clients that gather information from various components of the system (servers, firewalls, load balancer, etc.) and send it to the monitoring system. These data are then analyzed and used to generate alerts in case of issues.

-------------------------------------------------------------------------------------------------------

5. Explain what to do if you want to monitor your web server QPS (Queries Per Second):

To monitor the web server in terms of Queries Per Second (QPS), you need to configure the monitoring tool to collect data on incoming and outgoing traffic to the web server. You'll need to set up thresholds or rules in the monitoring tool to trigger an alert if the QPS exceeds a certain level, indicating excessive load or a potential issue.

-------------------------------------------------------------------------------------------------------

6. Why is SSL termination at the load balancer level problematic?

SSL termination at the load balancer level means that traffic between the load balancer and web servers is not encrypted. This can be problematic because it exposes data in transit between the load balancer and web servers to the risk of interception. Ideally, SSL traffic should be encrypted end-to-end, including between the load balancer and web servers.

-------------------------------------------------------------------------------------------------------

7. Why is having only one MySQL server capable of accepting writes a problem?

Having a single MySQL server capable of accepting writes is a problem because in the event of a server failure, the application won't be able to write to the database. This creates a Single Point of Failure (SPOF) for write operations, potentially causing a major service interruption.

-------------------------------------------------------------------------------------------------------

8. Why can having servers with the same components (database, web server, and application server) be a problem:

Having servers with the same components (database, web server, and application server) can be a problem because their resource consumption and needs are likely to differ. For example, more database servers may be needed to handle a heavy workload. Additionally, when maintenance is performed on a server for a specific component, it can affect other components on the same server, potentially impacting availability and resource management.

-------------------------------------------------------------------------------------------------------

Lastly, it's important to note that the load balancer remains a Single Point of Failure (SPOF), which means it can become a single point of failure in the infrastructure. To ensure high availability, it's recommended to deploy a high-availability load balancer with a failover configuration.
