<a href="https://zupimages.net/viewer.php?id=23/44/nwul.jpeg"><img src="https://zupimages.net/up/23/44/nwul.jpeg" alt="" /></a>

1. Load Balancer (HAProxy) :

Why: The load balancer (HAProxy) is added to distribute the load of incoming traffic between web servers, improving website availability and responsiveness. This ensures that traffic is balanced between servers.
Distribution algorithm: The HAProxy is configured with the "Round Robin" load distribution algorithm. This means that requests are distributed sequentially between the active servers.
Active-Active vs Active-Passive: The infrastructure is configured in Active-Active mode. This means that both web servers are active and serving traffic at the same time. Active-Passive would have meant that one server would have been on standby, ready to take over if the active server failed.

-------------------------------------------------------------------------------------------------------

2. For each additional element, why you add it :
The redundant server and load balancer are added to guarantee high availability and distribute traffic efficiently.

-------------------------------------------------------------------------------------------------------

3. What distribution algorithm is your load balancer configured with and how does it work?
The load balancer is configured with a Round Robin distribution algorithm. It works by sequentially distributing incoming traffic to the two servers in a circular fashion, ensuring that the load is evenly distributed.

-------------------------------------------------------------------------------------------------------

4. Does your load balancer allow an Active-Active or Active-Passive configuration?
The load balancer is configured with an Active-Active configuration, allowing both servers to actively manage incoming requests simultaneously. In an Active-Passive configuration, one server remains idle until the active server fails, whereas an Active-Active configuration allows both servers to actively share the traffic load.

-------------------------------------------------------------------------------------------------------

5. How a master replica (master-slave) database cluster works:
In a master replica (master-slave) cluster, the master/master database node manages read and write operations, while the replica/slave nodes respond to data from the master node to ensure data consistency across the cluster.
*A cluster is a set of several computers (or servers) interconnected and configured to work together as if they were a single system. The main purpose of a cluster is to improve the performance, availability and reliability of IT applications and services. Clusters are used in various areas of IT, including servers, databases, distributed computing, storage and high availability.

-------------------------------------------------------------------------------------------------------

6. What is the difference between the main node and the replica node as far as the application is concerned?
The master node handles read and write operations, making it the main point of interaction for the application. Replica nodes, on the other hand, are used for read operations, providing read scalability and failover support while offloading read traffic from the primary node.

-------------------------------------------------------------------------------------------------------

Infrastructure issues :

1. Single point of failure (SPOF):
The load balancer remains a single point of failure, potentially disrupting the entire system in the event of a malfunction or downtime. The MySQL database can also become an SPOF in the absence of redundancy. A high-availability load balancer and a MySQL cluster are recommended to remedy these SPOFs.

-------------------------------------------------------------------------------------------------------

2. Security issues:
The lack of a firewall exposes the system to unauthorised access. It is imperative to add a firewall to reinforce security. In addition, the absence of HTTPS makes communications vulnerable to interception. SSL/TLS is required to secure data in transit.

-------------------------------------------------------------------------------------------------------

3. No monitoring :
The absence of monitoring solutions means that the infrastructure is not monitored in terms of performance, availability and errors. A monitoring system is essential to detect and resolve problems quickly, ensuring a smooth user experience.
