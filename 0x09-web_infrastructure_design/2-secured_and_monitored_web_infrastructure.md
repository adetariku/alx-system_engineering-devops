Description

This is a 3-server web infrastructure that provides secure, monitored and encrypted traffic.

Specifics About This Infrastructure

Firewall is used to: 

To acts as an intermediary between an internal network and an external network, protecting a network (a web server anyway) from unwanted or unauthorized users by blocking incoming traffic that meets the above criteria. Designed to

The purpose of monitoring clients.

Monitoring clients are used to monitor servers and external networks. Analyze server performance and operations, measure overall health, and notify administrators when servers are not performing as expected. Monitoring tools monitor servers and provide administrators with key indicators about server behavior. It automatically tests server availability, measures response times, and alerts you to errors such as corrupted/missing files, security gaps/damage, and many other issues.

Issues With This Infrastructure

Terminating SSL at the load balancer level leaves the traffic between the load balancer and the web server unencrypted.
A single MySQL server is problematic because it is not scalable and can act as a single point of failure for your web infrastructure.
When servers contain identical components, the components on the server compete for resources such as CPU, memory, and I/O, which can slow performance and make it difficult to identify the source of problems. . Such a setup is not easily extensible.
