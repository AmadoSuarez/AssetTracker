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

## Advantages

**Return on Investment and Cost Savings:**

The greatest driver of most administration choices when choosing a new item is the return on investment. The more an answer can drive down expenses while increasing benefits, the better solution it is, particularly for substantial, set up organizations, which need to generate a steady flow of revenue for the long term. In this sense, Docker can help facilitate this type of savings by dramatically reducing infrastructure resources.

**Standardization and Productivity:**

Docker EE compartments guarantee consistency over various improvement and discharge cycles, standardizing your condition. One of the greatest points of interest to a Docker-based design is really institutionalization. Docker gives repeatable improvement, manufacture, test, and production environments. Standardizing service infrastructure across the entire pipeline allows every team member to work in a production parity environment. 

**Compatibility and Maintainability:**

Phase out the “it works on my machine” issue once and for all. One of the advantages that the whole group will acknowledge is equality. Equality, regarding Docker, implies that your images run the same regardless of which server or whose PC they are running on. For your developers, this means less time spent setting up environments, debugging environment-specific, and a more compact and simple to-set-up codebase. Equality also means your production infrastructure will be more reliable and easier to maintain.

**Multi-Cloud Platforms:**

One of Docker’s greatest benefits is portability. Over last few years, all major cloud computing providers, including Amazon Web Services (AWS) and Google Cloud Platform (GCP), have embraced Docker’s availability and added individual support. Docker containers can be run inside an Amazon EC2 instance, Google Compute Engine instance, Rackspace server, or VirtualBox, provided that the host OS supports Docker. If this is the case, a container running on an Amazon EC2 instance can easily be ported between environments, for example to VirtualBox, achieving similar consistency and functionality. 

**Security:**

Docker ensures that applications that are running on containers are completely segregated and isolated from each other, granting you complete control over traffic flow and management. No Docker container can look into processes running inside another container. From an architectural point of view, each container gets its own set of resources ranging from processing to network stacks. 