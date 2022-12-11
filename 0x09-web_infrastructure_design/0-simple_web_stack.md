This is a basic web server that runs a website that can be accessed by typing www.foobar.com. The network of the server is not secured by SSL certificates or firewalls. The server's resources (CPU, RAM, and SSD) must be shared by each component (database, application server).

Details Regarding This Infrastructure
a server's role.
A server is a piece of hardware or software on a computer that offers services to other computers, often known as clients.

what the domain name does.
to give an IP Address a human-friendly nickname. For instance, it's simpler to recall and recognize www.wikipedia.org than 91.198.174.192. The Domain Name System maps the IP address and domain name alias (DNS)

The DNS record www for www.foobar.com is of the type.
An A record is used by www.foobar.com. You may confirm this by launching dig www.foobar.com.
Note that although this design uses an A record for the infrastructure, the results may vary.
A hostname and its matching IPv4 address are stored in an Address Mapping record (A Record), commonly referred to as a DNS host record.

what the web server does.
The content of the requested resource or an error message is returned by the web server, which is software or hardware that accepts requests over HTTP or secure HTTP (HTTPS).

the application server's function.
for end users, IT services, and enterprises to install, run, and host applications and related services, as well as to facilitate the hosting and delivery of high-end consumer or business applications.



What the database does.
to keep a database of arranged data that can be conveniently accessed, maintained, and updated

the medium through which the server communicates with the client (computer of the user requesting the website).
Through the TCP/IP protocol suite, communication between the client and the server takes place through the internet network.

Concerns Regarding This Infrastructure
This infrastructure contains several SPOFs (single points of failure).
For instance, the entire website would be unavailable if the MySQL database server went down.

downtime during required repairs
The server must be shut down or any component shut down when we need to do maintenance checks on it. There is just one server, thus there would be a downtime on the website.

If incoming traffic is too high, scaling is impossible.
Because all the necessary components are on a single server, scaling this system would be challenging. When the server starts getting a lot of requests, it may quickly run out of resources or begin to slow down.
