Description
With the help of a server that balances the load between the two servers, this distributed web infrastructure tries to reduce the amount of traffic to the primary server by spreading some of the burden to a replica server (primary and replica).

Specifics About This Infrastructure

The load balancer's distribution algorithm configuration and operation.
The Round Robin distribution technique is configured in the HAProxy load balancer. According to their weights, the load balancer behind each server is used in turn by this method. Due to the fact that the servers' processing time is allocated equally, it is also likely the smoothest and most equitable method. Round Robin is a dynamic method that enables real-time modification of server weights.
the load-balancing configuration.

The setup enabled by the load-balancer.
The load balancer's distribution algorithm configuration and operation.
The Round Robin distribution technique is configured in the HAProxy load balancer. According to their weights, the load balancer behind each server is used in turn by this method. Due to the fact that the servers' processing time is allocated equally, it is also likely the smoothest and most equitable method. Round Robin is a dynamic method that enables real-time modification of server weights.
the load-balancing configuration.
Instead of an Active-Active setup, the HAProxy load-balancer is enabling an Active-Passive setup. The load balancer divides workloads among all nodes in an Active-Active configuration to avoid any one node from becoming overburdened. due to the increased number of nodes available to serve.

Additionally, response times and throughput will be significantly improved. On the other hand, not all nodes in an Active-Passive configuration will be active (capable of receiving workloads at all times). When there are two nodes, the second node must be passive or in standby mode, for instance, if the first node is currently operational. If the preceding node is inactive, the second or following passive node may turn active.

How a database Primary-Replica (Master-Slave) cluster works.
One server is set up to function as the primary server in a primary-replica configuration, and the second server serves as a replica of the primary server. However, while the Replica server can only handle read requests, the Primary server can handle both read and write requests. Every time the Primary server performs a write operation, the data between the Primary and Replica servers is updated.


The difference between the Primary node and the Replica node in regard to the application.

The Primary node handles all of the site's write operations, but the Replica node can also handle read operations, which reduces read load to the Primary node.
Concerns Regarding This Infrastructure.

There are numerous SPOFs (Single Point Of Failure).
For instance, the entire site would be unable to make updates if the Primary MySQL database server went down (including adding or removing users). The load balancer server and the application server that connects to the main database server are both SPOFs.
security concerns
Because an SSL certificate isn't used to encrypt the data being carried over the network, hackers can monitor the network. Since no firewall has been deployed on any server, there is no mechanism to prevent illegitimate IP addresses.
No surveillance.
Since each server is not being watched, we have no way of knowing its status.
