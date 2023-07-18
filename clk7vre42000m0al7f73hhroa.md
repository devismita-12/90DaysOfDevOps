---
title: "Introduction to EC2:"
datePublished: Tue Jul 18 2023 05:55:02 GMT+0000 (Coordinated Universal Time)
cuid: clk7vre42000m0al7f73hhroa
slug: introduction-to-ec2

---

Amazon Elastic Compute Cloud (Amazon EC2) provides on-demand, scalable computing capacity in the Amazon Web Services (AWS) Cloud. Using Amazon EC2 reduces hardware costs so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. You can add capacity (scale up) to handle compute-heavy tasks, such as monthly or yearly processes, or spikes in website traffic.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1689658715822/99e2a6ef-7d54-4ef8-9125-19e14dc6e702.png align="center")

* Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud.
    
* Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.
    
* Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.
    
* Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.
    

Deliver secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs. Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively. Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing. Deliver the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects

## <mark>EC2 Instance Types</mark>

### General Purpose instances

General Purpose instances are designed to deliver a balance of compute, memory, and network resources. They are suitable for a wide range of applications, including web servers, small databases, development and test environments, and more.

### Compute-optimized

Compute Optimized instances provide a higher ratio of compute power to memory. They excel in workloads that require high-performance processing such as batch processing, scientific modeling, gaming servers, and high-performance web servers.

### Memory-optimized

Memory Optimized instances are designed to handle memory-intensive workloads. They are suitable for applications that require large amounts of memory, such as in-memory databases, real-time big data analytics, and high-performance computing.

### Storage optimized

Storage Optimized instances are optimized for applications that require high, sequential read and write access to large datasets. They are ideal for tasks like data warehousing, log processing, and distributed file systems.

### Accelerated computing

Accelerated Computing Instances typically come with one or more types of accelerators, such as Graphics Processing Units (GPUs), Field Programmable Gate Arrays (FPGAs), or custom Application Specific Integrated Circuits (ASICs). These accelerators offload computationally intensive tasks from the main CPU, enabling faster and more efficient processing for specific workloads.

## **Features of Amazon EC2**

Amazon EC2 provides the following high-level features:

**Instances**

Virtual servers.

**Amazon Machine Images (AMIs)**

Preconfigured templates for your instances that package the components you need for your server (including the operating system and additional software).

**Instance types**

Various configurations of CPU, memory, storage, networking capacity, and graphics hardware for your instances.

**Key pairs**

Secure login information for your instances. AWS stores the public key and you store the private key in a secure place.

**Instance store volumes**

Storage volumes for temporary data that is deleted when you stop, hibernate, or terminate your instance.

**Amazon EBS volumes**

Persistent storage volumes for your data using Amazon Elastic Block Store (Amazon EBS).

**Regions, Availability Zones, Local Zones, AWS Outposts, and Wavelength Zones**

Multiple physical locations for your resources, such as instances and Amazon EBS volumes.

**Security groups**

A virtual firewall that allows you to specify the protocols, ports, and source IP ranges that can reach your instances and the destination IP ranges to which your instances can connect.

**Elastic IP addresses**

Static IPv4 addresses for dynamic cloud computing.

**Tags**

Metadata that you can create and assign to your Amazon EC2 resources.

**Virtual private clouds (VPCs)**

Virtual networks you can create that are logically isolated from the rest of the AWS Cloud. You can optionally connect these virtual networks to your own network.