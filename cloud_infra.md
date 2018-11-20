# Cloud Architecture Documentation: Docker Enterprise Edition on AWS Cloud

## Interface
3
Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes (removes the need to directly manage) server hardware, containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

<img width="616" alt="container_interfaces" src="https://user-images.githubusercontent.com/37644969/48748166-de385d80-ec43-11e8-8fc9-a8ea3e5d432f.png">

Docker Enterprise Edition (EE) is an integrated solution that includes open source and commercial software, the integrations between them, full Docker API support, validated configurations, and commercial support for your Docker EE environment. A pluggable architecture allows flexibility in the computer, networking, and storage providers that are used in your containers as a service (CaaS) infrastructure. The open APIs allow Docker EE to easily integrate into your existing systems, such as LDAP/AD, monitoring, logging, and more.

Docker Enterprise Edition has two main components: Docker Universal Control Plane (UCP) and Docker Trusted Registry (DTR).

**UCP** is an enterprise-grade cluster management solution from Docker that helps you manage your whole cluster from a single place. UCP includes the UCP controllers and UCP nodes.

**DTR** is the enterprise-grade image storage solution from Docker that helps you securely store and manage the Docker images you use in your applications. DTR is deployed in a three-node configuration that includes one DTR master and two DTR replicas.

## Architecture

<img width="704" alt="screen shot 2018-11-18 at 12 47 23 pm" src="https://user-images.githubusercontent.com/37644969/48748674-9e727580-ec45-11e8-8768-d79305ea076d.png">
**Quick overview of Docker EE environment on AWS**

This overview represents the following:

1.	A virtual private cloud (VPC) that spans three Availability Zones and includes three public subnets.
2.	Three Swarm controller nodes that run the DTR and UCP services.
3.	A cluster of Swarm nodes in an Auto Scaling group, so the cluster can grow dynamically as the load on the instances increases.
4.	Three Elastic Load Balancing (ELB) load balancers in the public subnets. Two of these load balancers provide inbound access to the management consoles for UCP and DTR, and the third provides inbound access to customer applications running on the Swarm nodes. 
5.	Amazon Simple Storage Service (Amazon S3) for backing up the root certificate authorities (CAs).
