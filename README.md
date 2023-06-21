# Learning-AWS-practitioner-essentials

Here are my notes of the AWS Cloud practitioner essentials course.

<img width="1190" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/14e7103b-fc64-4a6f-b0a8-f9b6946541d5">

# Content <!-- omit in toc -->

*   [AWS global infrastructure and releability](#AWS-global-infrastructure-and-releability)
    *   [Hiding individual stats](#hiding-individual-stats)
*   [Networking](#Networking)
   

#### Traditional on-premises model:
highly manual
expensive equipment 
less than full capacity
  ##### Roles
  * IT solution Architect
  * 🟠 System Administrator: keeps servers operational, it handles the on-site hardware and infrastructure, Install, superto and mantain computer system and servers
  * 🟣 Network administrator: Desing, install, configura, and maintain LAN and WAN
  * 🟣 Desktop administrator: Desploy, configure, secure, manage, and monitor devices and applications.
  * 🔵 Application administrator: Keep the organization´s applicaction up and running.
  * 🟠 Database administrator: Direct or perform installation and maintenance of databases in the IT enviroment.

> **_NOTE:_**  Many of the activities of the roles marked with 🟠 falls under AWS's responsability when a organization moves to the cloud. The roles marked with 🟣 🔵 might move into the AWS system operations and DevOps administrator roles respectively.
    
#### AWS Cloud Environment:
Increased development **speed**
Provide near-limitless **scale**
**Innovation** to shared responsabilities model, innovate with technologies such as advanced analytics, IoT and automation at scale
**Productivity** infrastructure, and security, automate compliance *AWS is responsible for security of the cloud and the customer is responsible for security in the cloud*
  ##### Roles
  * cloud architect: is the subject matter expert for the team. Is the tipical lateral move for an IT solution Architect
  * 🟣 AWS System Operation(SysOps):  It oversees the server, network and desktop teams
  * System Administrator: Must be proficient with configuration management and changes.
  * Security administrator
  * 🔵 Devops administrator: Build and operate fast and scalable workflows, implementing continous build, integration, deployment and infrastructure code. Must be proficient with programming scripting languages and also oversee database and developer teams.

## AWS cloud practitioner essentials

### Cloud computing
**The on-demand delivery of IT resources over the internet with pay-as-you-go pricing**


#### AWS servicing offer:
* Compute
* Storage
* Network Security
* Block chain
* Machine learning
* Artifitial intelligence

<div align="center">
<img width="300" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/929b35aa-0b4d-4152-9a1a-76d48137d718">
</div


* **Client**: Can be a web browser or desktop application that a person interacts with to make requests to computer servers.
* **Server**: Can be services such as Amazon Elastic Compute Cloud (Amazon EC2), a type of virtual server.
* **Cloud Computing**:is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing.

#### Cloud deployment models:
* **Cloud-Based deployment**: Run all parts of the application in the cloud, migrate existing applications to the cloud, design and build new applications in the cloud.
* **On-Premises deployment** (private cloud deployment): Deploy resources by using virtualization and resource management tools, Increase resource utilization by using application management and virtualization technologies.
* **Hybrid deployment**: Connect cloud-based resources to on-premises infrastructure, integrate cloud-based resources with legacy IT applications.



<div align="center">
  <img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/9b8758c7-f536-48fe-94f7-93da01b4aeda">
</div>

 ***<div align="center">Amazon elastic compute cloud (EC2)</div>***
 ***<div align="center">📙 Host traditional applications, full access to the OS</div>***
The AWS service provides access to virtual servers. It's highly flexible, cost-effective, and quick (secure, compute rezible capacity). AWS builds and secure the datacenters, puchase and install sesrvers, and the servers are online and ready to use.
With EC2 instances you are responsable for patching your instances when new software packages come out, setting up the scaling of those instances as well as ensuring that you've architected your solutions to be hosted in a highly available manner. 
* Multitenancy: sharing underlying hardware between virtual machines. is manage by AWS


### Amazon EC2 configuration:

**<div align="center">(🚀 Launch  🖥️  Conect  📧 Use )</div>**

🚀 Operating system: you can choose eaither Windows or Linux </br>
🚀 Aplication(s) server: Software running on the instance Internal buisiness apps, web apps, Data bases, thir-part applications...</br>
🚀 Instance type</br>
* Vertical Scaling: EC2 instances are also resizable. You might start with a small instance, realize the application you are running is starting to max out that server, and then you can give that instance more memory and more CPU.</br>
🚀Control over the Networking: Type of requests</br>

### Amazon EC2 types (families):
Each Amazon EC2 instance type is grouped under an instance family and optimized for certain types of tasks. Instance types offer varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications.
* **General purpose instances:** Provide a balance of compute, memory, and networking resources (Application, gaming and backend services and small and medium databases)
* **Compute optimized instances:** Ideal for compute-bound applications that benefit from high-performance processors for instances processing workloads that require processing many transactions in a single group, batch procesing.
* **Memory optimized instances:** are designed to deliver fast performance for workloads that process large datasets in memory for instance workload that requires large amounts of data to be preloaded before running aplications (Ideal for high-performance databases)
* **Accelerated computing instances:** use hardware accelerator or coprocessors, to perform some functions more efficiently than possible in software running on CPUs for instance floating-point number calculations, graphic processing and data pattern matching (ideal for streaming)
* **Storage optimized instances:**  are designed for workloads that require high, sequential read and write access to large datasets on local storage. (Suitable for data warehousing applications)

### Purchase options:
+ **On-Demand:** Ideal for short-term, irregular workloads that cannot be interrupted. No upfront cost or minimum contract applies.
+ **Savings plans:** Reduce your compute costs by committing to a consistent amount of compute usage for a 1- or 3-year term. This term commitment results in savings of up to 72% over ON-Demand costs
+ **Reserved instances:** are ideal for workloads with flexible start and end times, or that can withstand interruptions. Contract lenght of 1 and 3 years.
+ **Spot instances:** workloads that can be interrupted
+ **Dedicated host:** are physical servers with Amazon EC2 instance capacity that are fully dedicated to your use.

### Scalability and Elasticity:
**Scalability** involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. 
* **Amazon EC2 Auto Scaling:** This is a service provided for Amazon EC2 instances that allows the scaling process to happen automatically. Auto-scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand.
  * **Dynamic scaling** responds to changing demand.
  * **Predictive scaling** automatically schedules the right number of Amazon EC2 instances based on predicted demand.
  * When configuring the size of an auto scaling group, you can set ***minimum capacity***, ***Desired capacity*** and ***Maximum capacity***

### Elastic Load Balancing:
Is the AWS service that automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances. For example, if you have multiple Amazon EC2 instances, elastic load balancing distributes the workload across the multiple instances so that no single instance has to carry the bulk of it. 
Properly distribute traffic; high performance, cost-efficient, highly available, automatically scalable 

<div class="row" align="center">
    <img width="450" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/ee9834e8-4235-4c9e-87c0-3aa2ce7159f2">
</div>

### Messaging and queuing
* **Monolitic application** Tughtly coupled components. Applications are made of multiple components. The components communicate with each other to transmit data, fulfill requests, and keep the application running.
* **Microservices** Loosly coupled 

When designing applications on AWS, you can take a microservices approach with services and components that fulfill different functions. Two services facilitate application integration: Amazon Simple Notification Service (Amazon SNS) and Amazon Simple Queue Service (Amazon SQS).

* **Amazon SQS (Simple Queue Service)** is a message queuing service you can send, store and receive messages between software components at any volume
  * **Payload** Data contain within a message.
* **Amazon SNS (Simple Notification Service)**  is a publish/subscribe service. Using Amazon SNS topics, a publisher publishes messages to subscribers. 


<div align="center">
  <img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/904edb1c-1aee-4129-8db6-2bfe40ec9bac">
</div>

 ***<div align="center">Amazon elastic compute cloud (EC2)</div>***
  ***<div align="center">📙 Host short running functions, Service-oriented applications, event driven applications, no provisioning or managing servers</div>***

 AWS Lambda is one serverless compute option. Lambda's a service that allows you to upload your code into what's called a Lambda function. Configure a trigger and from there, the service waits for the trigger. When the trigger is detected, the code is automatically run in a managed environment, an environment you do not need to worry too much about because it is automatically scalable, highly available and all of the maintenance in the environment itself is done by AWS.
 
* **Serverless** You cannot see or access the underlying infrastructure that are hosting your application, means that your code runs on servers, but you do not need to provision or manage these servers

> 💡 If you are looking to run Docker container-based workloads on AWS ( A ***container*** is standard way of package your code), you first need to choose your orchestration tool either **ECS** or **EKS**. Then you need to chose your platform. Do you want to run your containers on EC2 instances that you manage or in a serverless environment like AWS Fargate that is managed for you? 

<div align="center">
  <img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/1abf31d8-7157-4192-ad53-5bc728665eee">
</div>

 ***<div align="center">Amazon elastic Container Service (Amazon ECS)</div>***
 Is a highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS. 



<div align="center">
 <img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/d44dfbe1-bd43-49e5-8dba-65cc854ed048">
</div>

 ***<div align="center">Amazon Elastic Kubernates Service (Amazon EKS)</div>***
 Is a fully managed service that you can use to run Kubernetes on AWS. 

 <div align="center">
 <img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/e40ecf15-b8b5-48bf-9213-bf3fa149e7b5">
</div>

 ***<div align="center">Amazon Fargate</div>***
 is a serverless compute engine for containers. It works with both Amazon ECS and Amazon EKS. 

 # AWS global infrastructure and releability

Throughout the globe, AWS builds **Regions** ( are geographical isolated areaa that contains AWS resources) to be closest to where the business traffic demands. Locations like Paris, Tokyo, Sao Paulo, Dublin, Ohio. Inside each Region, we have multiple data centers that have all the compute, storage, and other services you need to run your applications
There's four business factors that go into choosing a region. 

   1. Compliance with data governance and legal requirements
   2. Proximity to the customer: Must avoid latency (The time it takes for data to be sent and received)
   3. Feature availability
   4. Pricing
      
#### Availavility zones
An Availability Zone is a single data center or a group of data centers within a Region. Availability Zones are located tens of miles apart from each other. This is close enough to have low latency (the time between when content requested and received) between availability zones. However, if a disaster occurs in one part of the Region, they are distant enough to reduce the chance that multiple Availability Zones are affected.

> ⭐ Planning for failure and deploying applications across multiple Availability Zones is an important part of building a resilient and highly available architecture.

<div align="center">
  <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/9c9b2f5d-1289-41f7-92c8-33be0451598f">
</div>


#### Edge location
AWS Edge locations run **Amazon Cloudfront** (is a service that helps deliver data, video, applications, and APIs to customers around the world with low latency and high transfer speeds.) to help get content closer to your customers, no matter where they are in the world. An edge location is a site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery. Amazon CloudFront is a CDN (Content delivery network)

>**How do I interact with these services** In AWS, everything is an API (Application Programing Interface) call.

#### Interacting with AWS servies - provisioning resources
* **AWS Management console:** web-based interface for accessing and managing AWS services, includes wizards and workflows that you can use to complete tasks in AWS services.
   * Test envieroments
   * View AWS bills
   * View monitoring
   * work with non-technical resources 
* **AWS Command Line interface (CLI):** Make API calls using the terminal on your machinne, is used to automate actions for AWS services and applications through scripts.
* **AWS Software Development Kits (SDKs):** Interact with AWS resources through varoius programming languages, enable you to develop AWS applications in supported programming languages.

* **AWS outspot:**  Extend AWS infrastructure and services to your on-premises data center.


other manage tools you can manage your AWS environment


<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/06f49308-f227-4bd8-9268-320117cc0d5b">
   
**AWS Elastic Beanstalk**
is a service that helps you provision Amazon EC2-based environments. Instead of clicking around the console or writing multiple commands to build out your network, EC2 instances, scaling and Elastic Load Balancers, you can instead provide your application code and desired configurations to the AWS Elastic Beanstalk service, which then takes that information and builds out your environment for you.
Helps you to focus on your business application, not the infrastructure.
* Adjust capacity
* Load balancing
* Automatic scaling
* Application health monitoring

<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/01ee8c6e-33f1-4805-90d8-85f3404c2324">
   
**AWS Cloud formation**
Infrastructure as code tool used to define. awide variety of AWS resources. Supoort storage, database, analytics, machine learning 



# Networking

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/9c3cc8c3-8b17-4bb6-90b4-523948c2f00e">
</div>

 ***<div align="center">Amazon Virtual Private Cloud (Amazon VPC)</div>***
is essentially your own private network in AWS. A VPC allows you to define your private IP range for your AWS resources, and you place things like EC2 instances and ELBs inside of your VPC. You place your resources into different **Subnets**; Subnets are chunks of IP addresses in your VPC that allow you to group resources together. Control if resources are either privately or publicly available. In a VPC, subnets can communicate with each other. For example, you might have an application that involves Amazon EC2 instances in a public subnet communicating with databases that are located in a private subnet.

*  **Subnets** A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private. 
   * **Public subnets** contain resources that need to be accessible by the public, such as an online store’s website.
   * **Private subnets** contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories. 
* 🚪 **Internet Gateway** allow public traffic from the internet to access your VPC.
<div align="center">
  <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/5a7aa22c-b80d-4fac-9452-82f663b5ceeb">
</div>

* 🔒 **Virutal Private Gateway** allows protected internet traffic to enter into the VPC. A virtual private gateway enables you to establish a virtual private network (VPN) connection between your VPC and a private network, such as an on-premises data center or internal corporate network. A virtual private gateway allows traffic into the VPC only if it is coming from an approved network.

<div align="center">
  <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/f462a9d7-50f6-4ca0-951b-f562869c4ea2">
</div>

* <img width="20" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/18b534b4-70d9-45f1-befb-47cf6bbda098"> **AWS direct connect** llows you to establish a completely private, dedicated fiber connection from your data center to AWS. You work with a Direct Connect partner in your area to establish this connection, AWS Direct Connect provides a physical line that connects your network to your AWS VPC

<div align="center">
  <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/d18a040c-ad29-439c-9aef-05b8888e0f8c">
</div>

#### Network traffic in a VPC
When a customer requests data from an application hosted in the AWS Cloud, this request is sent as a **packet**. A packet is a unit of data sent over the internet or a network. It enters into a VPC through an internet gateway. Before a packet can enter into a subnet or exit from a subnet, it checks for permissions. These permissions indicate who sent the packet and how the packet is trying to communicate with the resources in a subnet.
The VPC component that checks packet permissions for subnets is a **network access control list (ACL).**

**Network access control lists (ACLs)**: A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.

<img width="430" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/6c68c6a1-89d4-49ce-b772-373e03cc633f">










