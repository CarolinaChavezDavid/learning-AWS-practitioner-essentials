# Learning-AWS-practitioner-essentials

Here are my notes from the AWS Cloud Practitioner Essentials course.

<img width="1190" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/14e7103b-fc64-4a6f-b0a8-f9b6946541d5">

# Cloud roles

<details>
#### Traditional on-premises model:
highly manual
expensive equipment 
less than full capacity



  ##### Roles
  * IT solution Architect
  * 🟠 System Administrator: keeps servers operational, it handles the on-site hardware and infrastructure, Install, superto and mantain computer system and servers
  * 🟣 Network administrator: Desing, install, configurate, and maintain LAN and WAN
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

</details>



# AWS cloud practitioner essentials



<hr />

# Cloud computing
 <details>
**The on-demand delivery of IT resources over the internet with pay-as-you-go pricing**


#### AWS servicing offer:
* Compute
* Storage
* Network Security
* Block chain
* Machine learning
* Artificial intelligence

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

 ***<div align="center">Amazon Lambda</div>***
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
 
 </details>


     
 # AWS global infrastructure and releability

   <details>

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

 </details>

# Networking

<details>
   
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

* <img width="20" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/18b534b4-70d9-45f1-befb-47cf6bbda098"> **AWS direct connect** Allows you to establish a completely private, dedicated fiber connection from your data center to AWS. You work with a Direct Connect partner in your area to establish this connection, AWS Direct Connect provides a physical line that connects your network to your AWS VPC

<div align="center">
  <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/d18a040c-ad29-439c-9aef-05b8888e0f8c">
</div>

| **Security group**                                          | **Network ACL**                                                      |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| Stateful                                                    | Stateless                                                            |
| Intance level                                               | VPC level (getaway)                                                  |
| Default: denies all inbound traffic and allows all outbound | Default: It is stateless and allows all inbound and outbound traffic |
| exp:  door attendant building                               | exp: airport migration                                               |

#### Network traffic in a VPC
When a customer requests data from an application hosted in the AWS Cloud, this request is sent as a **packet**. A packet is a unit of data sent over the internet or a network. It enters into a VPC through an internet gateway. Before a packet can enter into a subnet or exit from a subnet, it checks for permissions. These permissions indicate who sent the packet and how the packet is trying to communicate with the resources in a subnet.
The VPC component that checks packet permissions for subnets is a **network access control list (ACL).**

**Network access control lists (ACLs)**: A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/6c68c6a1-89d4-49ce-b772-373e03cc633f">
</div>

 ***<div align="center">Amazon Route 53</div>***
 is a DNS web service. It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS. Another feature of Route 53 is the ability to manage the DNS records for domain names. You can register new domain names directly in Route 53. You can also transfer DNS records for existing domain names managed by other domain registrars. This enables you to manage all of your domain names within a single location.
 * **DNS (Domain Name System):** You can think of DNS as being the phone book of the internet. DNS resolution is the process of translating a domain name to an IP address.
<div align="center">
   <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/57d0bf3d-98bf-44eb-82af-39af246cbecf">
</div>



**Routing policies**
* Latency-based routing
* Geolocation DNS
* Geoproximity routing
* Weighted round robin

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/1a72d0e4-7b66-42e7-bac9-86b5a569d21e">
</div>

 ***<div align="center">Amazon Cloud front</div>***

is a content delivery service. It uses a network of edge locations to cache content and deliver it to customers all over the world.


 <div align="center">
 <img width="800" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/b5e9ea92-7b09-4fbf-b20f-3d6c135647f2">
</div>

</details>

# Storage and databases
<details>
   
* 🗃️ **Instance Store** is a block level storage volumes that behave like a physical drives, provides temporary storage for an Amazon EC2 instance, is physically attached to the host computer for an EC2 instance, therefore has the same lifespan ***When the instance is terminated, you lose any data in the instance store.***

> Amazon EC2 instances are virtual servers. If you start an instance from a stopped state, the instance might start on another host, where the previously used instance store volume does not exist.

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/53ac9370-f6fb-4e8e-853d-1a73301dd4a6">
</div>

 ***<div align="center">Amazon Elastic Block Store (Amazon EBS)</div>***
  **<div align="center">Block storage</div>**

is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available.
you define configuration as volume size and type

> An Amazon EBS volume stores data in a single Availability Zone.

   * **Amazon EBS snapshots** Help you to take ***incremental backups*** of EBS volumes of data that needs to perssits. Incremetal means that only make backups of the block of data that has change since the last snapshot

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/d21a420d-4c8b-41d2-938f-e09bfb5d3488">
</div>

 ***<div align="center">Amazon Simple Storage Service (Amazon S3)</div>***
  **<div align="center">Object storage</div>**

 is a service that provides object-level storage. Amazon S3 stores data as objects in buckets. Amazon S3 offers unlimited storage space. The maximum file size for an object in Amazon S3 is 5 TB. You can also use the Amazon S3 versioning feature to track changes to your objects over time.
 
In **object storage**, each object consists of data (image, video, text document, or any other type of file), metadata (information about what the data is, how it is used, the object size, and so on), and a key (unique identifier).

 > ⚠️ When a file in object storage is modified, the entire object is updated.

* **Amazon S3 storage classes** you can select an Amazon S3 storage class considering How often you plan to retrieve your data, How available you need your data to be.


| Amazon S3 class | Characteristics |  Applicability considerations |
|:---:|:---:|:---:|
| Amazon S3 Standard | * Designed for frequently accessed data<br>* Stores data in a minimum of three Availability Zones<br>▪️ has a higher cost than other storage classes intended for <br>infrequently accessed data and archival storage. | ▪️ websites, content distribution, and data analytics |
| Amazon S3 <br>Standard-Infrequent Access (S3 Standard-IA) | ▪️ Ideal for infrequently accessed data<br>* Similar to Amazon S3 Standard but has a lower storage price <br>and higher retrieval price | ▪️ it automatically moves it to the infrequent or frequent access tier, <br>according to the access days |
| Amazon S3 <br>One zone-infrequent Access (S3 one Zone IA) | ▪️ Stores data in a single Availability Zone<br>* Has a lower storage price than Amazon S3 Standard-IA | *You want to save costs on storage.<br>*You can easily reproduce your data in the event of an <br>Availability Zone failure. |
| Amazon S3 <br>Intelligent-Tiering | ▪️ Ideal for data with unknown or changing access patterns<br>▪️ Requires a small monthly monitoring and automation fee per object |  |
| Amazon S3 <br>Glacier Instant Retrieval | ▪️  Works well for archived data that requires immediate access<br>▪️ Can retrieve objects within a few milliseconds |  |
| Amazon S3 <br>Glacier Flexible Retrieval | ▪️  Low-cost storage designed for data archiving<br>▪️ Able to retrieve objects within a few minutes to hours | ▪️ storage class to store archived customer records or older <br>photos and video files. |
| Amazon S3 <br>Glacier Deep Archive | ▪️ Lowest-cost object storage class ideal for archiving<br>▪️ Able to retrieve objects within 12 to 48 hours |  |
| Amazon S3 <br>Outposts | ▪️ Creates S3 buckets on Amazon S3 Outposts<br>* Makes it easier to retrieve, store, and access data on AWS Outposts | ▪️ delivers object storage to your on-premises AWS Outposts environment.<br>▪️ It works well for workloads with local data residency requirements <br>that must satisfy demanding performance needs by keeping data close to <br>on-premises applications. |


<div align="center">
<img width="1000" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/079d47ba-c50a-4e6f-b458-3b6b7fea5c32">
</div>

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/3ff8318c-7955-42fb-ac6c-4e9152b1be53">
</div>

 ***<div align="center">Amazon Elastic File System (Amazon EFS)</div>***
 **<div align="center">File storage</div>**

Is a scalable file system used with AWS Cloud services and on-premises resources. As you add and remove files, Amazon EFS grows and shrinks automatically. It can scale on demand to petabytes without disrupting applications.

 In **file storage**, multiple clients (such as users, applications, servers, and so on) can access data that is stored in shared file folders. is ideal for use cases in which a large number of services and resources need to access the same data at the same time.

 > Amazon EFS is a regional service. It stores data in and across multiple Availability Zones.

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/e43e0c1f-9072-499c-b950-93108b1bcbaf">
</div>

 ***<div align="center">Amazon Relational Database Service (Amazon RDS)</div>***

 Is a service that enables you to run relational databases in the AWS Cloud. Amazon RDS is a managed service that automates tasks such as hardware provisioning, database setup, patching, and backups.

 * **Amazon RDS database engines**
   * PostgreSQL
   * MySQL
   * MariaDB
   * Oracle Database
   * Microsoft SQL Server
   * <img width="20" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/fde6a3dc-451b-413c-90e0-ac7a2ad94923"> **Amazon Aurora** is an enterprise-class relational database. It is compatible with MySQL and PostgreSQL relational databases. It is up to five times faster than standard MySQL databases and up to three times faster than standard PostgreSQL databases. Amazon Aurora helps to reduce your database costs by reducing unnecessary input/output (I/O) operations, while ensuring that your database resources remain reliable and available.  Consider Amazon Aurora if your workloads require high availability. It replicates six copies of your data across three Availability Zones and continuously backs up your data to Amazon S3.

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/192b3f6c-cd76-486b-b393-92bb71032901">
</div>
 
***<div align="center">Amazon DynamoDB</div>***
Is a key-value database service. It delivers single-digit millisecond performance at any scale. is serverless, which means that you do not have to provision, patch, or manage servers. You also do not have to install, maintain, or operate software. As the size of your database shrinks or grows, DynamoDB automatically scales to adjust for changes in capacity while maintaining consistent performance. This makes it a suitable choice for use cases that require high performance while scaling.

<div align="center">
<img width="1000" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/50512248-ef38-49ec-bd6d-facfac31d7f3">
</div>

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/55c93cc8-916e-4b20-b454-b33e96cf5718">
</div>

 ***<div align="center">Amazon Redshift</div>***
  **<div align="center">Data Warehouse</div>**
is a data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data.

<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/382dc1de-f512-44bf-baba-c5eff58725c0">
</div>

 ***<div align="center">AWS Database Migration Service (AWS DMS)</div>***

enables you to migrate relational databases, nonrelational databases, and other types of data stores. With AWS DMS, you move data between a source database and a target database. The source and target databases can be of the same type or different types. During the migration, your source database remains operational, reducing downtime for any applications that rely on the database. There could be homogeneos or hetereogeneous migration. Other use cases:
   * Development and test database migrations
   * Database consolidation:  Combining several databases into a single database
   * Continuous replication

### Other services
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/e194eede-5655-4ab9-a82e-ed7a82f1b485"> **Amazon DocumentDB**  is a document database service that supports MongoDB workloads. (MongoDB is a document database program.)
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/fa097690-5649-4056-b4d8-93de15aeede1"> **Amazon Neptune**  is a graph database service to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection, and knowledge graphs
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/b3048b47-7ce1-449b-a05b-b7d6cb8d3ee1"> **Amazon Quantum Ledger Database (Amazon QLDB)**  is a ledger database service to review a complete history of all the changes that have been made to your application data.
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/718efab0-8f7e-491e-b19c-e84fac227e66"> **Amazon Managed Blockchain** is a service that you can use to create and manage blockchain networks with open-source frameworks. Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority.
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/3083bb74-3978-46af-a25f-4863560abd6d"> **Amazon ElastiCache** is a service that adds caching layers on top of your databases to help improve the read times of common requests. It supports two types of data stores: Redis and Memcached.
* <img width="30" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/4e682c4d-6d97-4e54-992a-8bedaeb9decc"> **Amazon DynamoDB Accelerator (DAX)** is an in-memory cache for DynamoDB. It helps improve response times from single-digit milliseconds to microseconds.

</details>

# Security

<details>

### Share respoonsability model
* **Costumer responsability**: "security in the cloud”, Customers are responsible for the security of everything that they create and put in the AWS Cloud.
* **AWS responsability**: "security of the cloud”, AWS operates, manages, and controls the components at all layers of infrastructure. This includes areas such as the host operating system, the virtualization layer, and even the physical security of the data centers from which services operate. 

<div align="center">
<img width="1000" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/bfea094c-bb09-465a-9fab-0c0043d815fd">
</div>


<div align="center">
<img width="50" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/034303f6-4da1-4b5c-8b83-234e03efaa03">
</div>

 ***<div align="center">AWS Identity and Access Management</div>***

 IAM enables you to manage access to AWS services and resources securely.

* **IAM users, groups, and roles**
    * **AWS account root user**

<div align="center">
<img width="700" alt="image"src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/6e6a4dcb-e07c-4bba-8a2a-1b64952d689a">
</div>

***Do not use the root user for everyday tasks.*** 
   * **IAM users** it's an identity that you create in AWS. It represents the person or application that interacts with AWS services and resources. It consists of a name and credentials. By default, when you create a new IAM user in AWS, it has no permissions associated with it. you must grant the IAM user the necessary permissions.
     
* **IAM policies** it's a document that allows or denies permissions to AWS services and resources.

<div align="center">
  <img width="300" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/5ece4b17-2930-4129-95e6-0dded6267a5e">

</div>

* **IAM groups**  it's a collection of IAM users. When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.
* **IAM groups** it's an identity that you can assume to gain temporary access to permissions. Before an IAM user, application, or service can assume an IAM role, they must be granted permissions to switch to the role. When someone assumes an IAM role, they abandon all previous permissions that they had under a previous role and assume the permissions of the new role.  
* **Multi-factor authentication** extra layer of security

### AWS Organizations
You can use AWS Organizations to consolidate and manage multiple AWS accounts within a central location.When you create an organization, AWS Organizations automatically creates a root, which is the parent container for all the accounts in your organization. In AWS Organizations, you can centrally control permissions for the accounts in your organization by using service control policies (SCPs). **SCPs** enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.
The default maximum number of accounts allowed for an organization is 4, but you can contact AWS Support to increase your quota, if needed.

* **Organizational units** In AWS Organizations, you can group accounts into organizational units (OUs) to make it easier to manage accounts with similar business or security requirements you can apply service control policies (SCPs) to the organization root, an individual member account, or an OU. 

### compliance

* **AWS Artifact** it's a service that provides on-demand access to AWS security and compliance reports and select online agreements.
  * **AWS Artifact Agreements** you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations. Different types of agreements are offered to address the needs of customers who are subject to specific regulations, such as the Health Insurance Portability and Accountability Act (HIPAA).
  * **AWS Artifact Reports** provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations. AWS Artifact Reports remains up to date with the latest reports released.

  ### Denial-of-service attacks

it'ss a deliberate attempt to make a website or application unavailable to users.
* **Distributed denial-of-service attacks** In a distributed denial-of-service (DDoS) attack, multiple sources are used to start an attack that aims to make a website or application unavailable. This can come from a group of attackers, or even a single attacker. The single attacker can use multiple infected computers (also known as “bots”) to send excessive traffic to a website or application.

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/e8f8b676-5054-4a18-ac2f-696bd1d2b62d">
</div>

 ***<div align="center">AWS Shield</div>***
 
* **AWS Shield Standard** automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frequently occurring types of DDoS attacks. uses a variety of analysis techniques to detect malicious traffic in real time and automatically mitigates it. 
* **AWS Artifact Reports** is a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. It also integrates with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks.

  <div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/60fc59f9-2900-4b8a-9eab-082043614615">
</div>

 ***<div align="center">AWS Key Management Service (AWS KMS)</div>***
it enables you to perform encryption operations through the use of cryptographic keys. A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data. You can use AWS KMS to create, manage, and use cryptographic keys. You can also control the use of keys across a wide range of services and in your applications.

 <div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/09acd862-dd08-478f-8680-3fa6f5fd83ba">
</div>

 ***<div align="center">AWS WAF</div>***
 it's a web application firewall that lets you monitor network requests that come into your web applications. 

AWS WAF works together with Amazon CloudFront and an Application Load Balancer. Recall the network access control lists that you learned about in an earlier module. AWS WAF works in a similar way to block or allow traffic. However, it does this by using a web access control list (ACL) to protect your AWS resources. 


 <div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/e1373d65-4de1-4506-bcce-85ccdb843f5c">
</div>

 ***<div align="center">Amazon inspector</div>***
 Amazon Inspector helps to improve the security and compliance of applications by running automated security assessments. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to Amazon EC2 instances and installations of vulnerable software versions.

 
 <div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/3591f914-ad18-4c7b-bfe0-31b947b571c1">
</div>

 ***<div align="center">Amazon GuardDuty</div>***
 is a service that provides intelligent threat detection for your AWS infrastructure and resources. It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.
 
 </details>

 # Monitoring and analytics

  <details>

  <div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/751f4a27-1e34-48bb-9487-58841944ad10">
</div>


 ***<div align="center">Amazon CloudWatch</div>***

  it's a web service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics. CloudWatch uses metrics to represent the data points for your resources. AWS services send metrics to CloudWatch. CloudWatch then uses these metrics to create graphs automatically that show how performance has changed over time

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/a3ed7e94-2a97-47e6-9ec3-f3c8606b0be5">
</div>

 ***<div align="center">AWS CloudTrail</div>***
 records API calls for your account. The recorded information includes the identity of the API caller, the time of the API call, the source IP address of the API caller, and more. You can think of CloudTrail as a “trail” of breadcrumbs (or a log of actions) that someone has left behind them.
 * **CloudTrail Insights** his optional feature allows CloudTrail to automatically detect unusual API activities in your AWS account.

<div align="center">
<img width="50" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/91416f85-b2c9-456b-a9c4-d4e20b83c930">
</div>

***<div align="center">AWS Trusted advisor</div>***
 is a web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices. he inspection includes security checks, such as Amazon S3 buckets with open access permissions.

 <div align="center">
 <img width="1000" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/ee16672a-6cc4-4899-84cb-e15f4e0d18e5">
</div>

 </details>

  # Pricing and support

<details>

### Free tier
   Enables you to begin using certain services without having to worry about incurring costs for the specified period. 
   * **Always free** These offers do not expire and are available to all AWS customers. For example, AWS Lambda allows 1 million free requests and up to 3.2 million seconds of compute time per month. Amazon DynamoDB allows 25 GB of free storage per month.
   * **12 months free** These offers are free for 12 months following your initial sign-up date to AWS. Examples include specific amounts of Amazon S3 Standard Storage, thresholds for monthly hours of Amazon EC2 compute time, and amounts of Amazon CloudFront data transfer out.
   * **Trials** Short-term free trial offers start from the date you activate a particular service. The length of each trial might vary by number of days or the amount of usage in the service.
For example, Amazon Inspector offers a 90-day free trial. Amazon Lightsail (a service that enables you to run virtual private servers) offers 750 free hours of usage over a 30-day period.

### AWS pricing
   * **Pay for what you use** For each service, you pay for exactly the amount of resources that you actually use, without requiring long-term contracts or complex licensing. .
   * **Pay less when you reserve** Some services offer reservation options that provide a significant discount compared to On-Demand Instance pricing.
For example, suppose that your company is using Amazon EC2 instances for a workload that needs to run continuously. You might choose to run this workload on Amazon EC2 Instance Savings Plans, because the plan allows you to save up to 72% over the equivalent On-Demand Instance capacity. A Compute Savings Plan offers lower compute costs in exchange for committing to a consistent amount of usage over a 1-year or 3-year term. 
   * **Pay less with volume-based discounts when you use more** Some services offer tiered pricing, so the per-unit cost is incrementally lower with increased usage.
For example, the more Amazon S3 storage space you use, the less you pay for it per GB.

### AWS pricing
You can create budgets to plan your service usage, service costs, and instance reservations. The information in AWS Budgets updates three times a day. This helps you to accurately determine how close your usage is to your budgeted amounts or to the AWS Free Tier limits. In AWS Budgets, you can also set custom alerts when your usage exceeds (or is forecasted to exceed) the budgeted amount.

### AWS cost explorer
is a tool that enables you to visualize, understand, and manage your AWS costs and usage over time. AWS Cost Explorer includes a default report of the costs and usage for your top five cost-accruing AWS services. You can apply custom filters and groups to analyze your data. For example, you can view resource usage at the hourly level.

### AWS Support

AWS offers four different Support plans to help you troubleshoot issues, lower costs, and efficiently use AWS services.. 
   * **Basic Support** is free for all AWS customers. It includes access to whitepapers, documentation, and support communities. With Basic Support, you can also contact AWS for billing questions and service limit increases. With Basic Support, you have access to a limited selection of AWS Trusted Advisor checks. Additionally, you can use the AWS Personal Health Dashboard, a tool that provides alerts and remediation guidance when AWS is experiencing events that may affect you. 
   * **Developer support**
      * Best practice guidance
      * Client-side diagnostic tools
      * Building-block architecture support, which consists of guidance for how to use AWS offerings, features, and services together
   * **Business Support**
      * Use-case guidance to identify AWS offerings, features, and services that can best support your specific needs
      * All AWS Trusted Advisor checks
      * Limited support for third-party software, such as common operating systems and application stack components
   * **Enterprise On-Ramp Support**
      * A pool of Technical Account Managers to provide proactive guidance and coordinate access to programs and AWS experts
        * Consultative review and architecture guidance (one per year)
        * Infrastructure Event Management support (one per year)
        * Support automation workflows
        * 30 minutes or less response time for business-critical issues
      * A Cost Optimization workshop (one per year)
      * A Concierge support team for billing and account assistance
      * Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard
   * **Enterprise Support**
      * A designated Technical Account Manager to provide proactive guidance and coordinate access to programs and AWS experts
        * Consultative review and architecture guidance 
        * Infrastructure Event Management support
        * Cost Optimization Workshop and tools
        * Support automation workflows
        * 15 minutes or less response time for business-critical issues
      * A Concierge support team for billing and account assistance
      * Training and Game Days to drive innovatio
      * Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard
    
**Technical Account Manager (TAM)**
The TAM is your primary point of contact at AWS. If your company subscribes to Enterprise Support or Enterprise On-Ramp, your TAM educates, empowers, and evolves your cloud journey across the full range of AWS services. TAMs provide expert engineering guidance, help you design solutions that efficiently integrate AWS services, assist with cost-effective and resilient architectures, and provide direct access to AWS programs and a broad community of experts

### AWS Marketplace
is a digital catalog that includes thousands of software listings from independent software vendors. You can use AWS Marketplace to find, test, and buy software that runs on AWS. 

<div align="center">
<img width="812" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/bf0ac97b-057e-4199-bd14-c65335b14c34">
</div>

</details>


# Migration and innovation

<details>

   ###  AWS Cloud Adoption Framework (AWS CAF)
organizes guidance into six areas of focus, called Perspectives. Each Perspective addresses distinct responsibilities. The planning process helps the right people across the organization prepare for the changes ahead.

* **Business Perspective** ensures that IT aligns with business needs and that IT investments link to key business results. helps you to move from a model that separates business and IT strategies into a business model that integrates IT strategy. commons roles:
   * Business managers
   * Finance managers
   * Budget owners
   * Strategy stakeholders
* **People Perspective** supports development of an organization-wide change management strategy for successful cloud adoption.
   * Human resources
   * Staffing
   * People managers
* **Governance Perspective** focuses on the skills and processes to align IT strategy with business strategy. This ensures that you maximize the business value and minimize risks. helps to understand how to update the staff skills and processes necessary to ensure business governance in the cloud. Manage and measure cloud investments to evaluate business outcomes.
   * Chief Information Officer (CIO)
   * Program managers
   * Enterprise architects
   * Business analysts
   * Portfolio managers
* **Platform Perspective**  includes principles and patterns for implementing new solutions on the cloud, and migrating on-premises workloads to the cloud.
   * Chief Technology Officer (CTO)
   * IT managers
   * Solutions architects
* **Security Perspective** ensures that the organization meets security objectives for visibility, auditability, control, and agility. helps you structure the selection and implementation of permission
   * Chief Information Security Officer (CISO)
   * IT security managers
   * IT security analysts
* **Operations Perspective**  helps you to enable, run, use, operate, and recover IT workloads to the level agreed upon with your business stakeholders. Define how day-to-day, quarter-to-quarter, and year-to-year business is conducted. Align with and support the operations of the business. The AWS CAF helps these stakeholders define current operating procedures and identify the process changes and training needed to implement successful cloud adoption.
   * IT operations managers
   * IT support managers
 
### Strategies for migration

| **Rehosting** | also known as “lift-and-shift” involves moving applications without changes |
|:---:|:---:|
| **Replatforming** | also known as “lift, tinker, and shift,” involves making a few cloud optimizations to realize a tangible benefit. <br>Optimization is achieved without changing the core architecture of the application |
| **Refactoring** | also known as re-architecting, involves reimagining how an application is architected and developed by using cloud-native features |
| **Repurchasing** | involves moving from a traditional license to a software-as-a-service model. |
| **Retaining** | consists of keeping applications that are critical for the business in the source environment |
| **Retiring** | is the process of removing applications that are no longer needed |

### AWS snow family
It's a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS. 
<div align="center">
<img width="500" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/ddc2dc4f-9f86-4a70-8ef5-befeeef93c60">
</div>

* **AWS Snowcone** is a small, rugged, and secure edge computing and data transfer device. It features 2 CPUs, 4 GB of memory, and 8 TB of usable storage.
* **AWS Snowball**
   * **Snowball Edge Storage Optimized** devices are well suited for large-scale data migrations and recurring transfer workflows, in addition to local computing with higher capacity needs. 
      * Storage: 80 TB of hard disk drive (HDD) capacity for block volumes and Amazon S3 compatible object storage, and 1 TB of SATA solid state drive (SSD) for block volumes. 
      * Compute: 40 vCPUs, and 80 GiB of memory to support Amazon EC2 sbe1 instances (equivalent to C5).
   * **Snowball Edge Compute Optimized** provides powerful computing resources for use cases such as machine learning, full motion video analysis, analytics, and local computing stacks. 
      * Storage: 42-TB usable HDD capacity for Amazon S3 compatible object storage or Amazon EBS compatible block volumes and 7.68 TB of usable NVMe SSD capacity for Amazon EBS compatible block volumes. 
      * Compute: 52 vCPUs, 208 GiB of memory, and an optional NVIDIA Tesla V100 GPU. Devices run Amazon EC2 sbe-c and sbe-g instances, which are equivalent to C5, M5a, G3, and P3 instances.
* **AWS Snowmobile** is an exabyte-scale data transfer service used to move large amounts of data to AWS. You can transfer up to 100 petabytes of data per Snowmobile, a 45-foot long ruggedized shipping container, pulled by a semi trailer truck.

* **Amazon SageMaker**, you can quickly and easily begin working on machine learning projects. You do not need to follow the traditional process of manually bringing together separate tools and workflows.
* **Amazon Textract** is a machine learning service that automatically extracts text and data from scanned documents.
* **Amazon Lex** is a service that enables you to build conversational interfaces using voice and text.
* **AWS DeepRacer** is an autonomous 1/18 scale race car that you can use to test reinforcement learning models.
* **Argumented AI** Amazon Augmented AI (Amazon A2I) provides built-in human review workflows for common machine learning use cases, such as content moderation and text extraction from documents. With Amazon A2I, you can also create your own workflows for machine learning models built on Amazon SageMaker or any other tools.



</details>


# The cloud journey

<details>

   ### The AWS well-architected framework

   helps you understand how to design and operate reliable, secure, efficient, and cost-effective systems in the AWS Cloud.

<div align="center">
<img width="500" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/c8bae68b-36a3-473e-bc52-c905185f67c2">
</div>

The Well-Architected Framework is based on six pillars: 

* **Operational excellence** is the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures (operations as code, annotating documentation, anticipating failure, and frequently making small, reversible changes. The ability to run workloads effectively and gain insights into their operations
* **Security**  is the ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies. 
When considering the security of your architecture, apply these best practices:
   * Automate security best practices when possible.
   * Apply security at all layers.
   * Protect data in transit and at rest.
* **Reliability** the ability of a workload to consistently and correctly perform its intended functions
   * Recover from infrastructure or service disruptions
   * Dynamically acquire computing resources to meet demand
   * Mitigate disruptions such as misconfigurations or transient network issues
Reliability includes testing recovery procedures, scaling horizontally to increase aggregate system availability, and automatically recovering from failure.
* **Performance efficiency** is the ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve. (Evaluating the performance efficiency of your architecture includes experimenting more often, using serverless architectures, and designing systems to be able to go global in minutes.
* **Cost optimization** is the ability to run systems to deliver business value at the lowest price point. Cost optimization includes adopting a consumption model, analyzing and attributing expenditure, and using managed services to reduce the cost of ownership.
* **Sustainability** is the ability to continually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing the total resources required.
To facilitate good design for sustainability:
   * Understand your impact
   * Establish sustainability goals
   * Maximize utilization
   * Anticipate and adopt new, more efficient hardware and software offerings
   * Use managed services
   * Reduce the downstream impact of your cloud workloads

  ### Advantage of cloud computing
* **Trade upfront expense for variable expense**
Upfront expenses include data centers, physical servers, and other resources that you would need to invest in before using computing resources. 
Instead of investing heavily in data centers and servers before you know how you’re going to use them, you can pay only when you consume computing resources.
* **Benefit from massive economies of scale**
By using cloud computing, you can achieve a lower variable cost than you can get on your own. 
Because usage from hundreds of thousands of customers aggregates in the cloud, providers such as AWS can achieve higher economies of scale. Economies of scale translate into lower pay-as-you-go prices.
* **Stop guessing capacity.**
With cloud computing, you don’t have to predict how much infrastructure capacity you will need before deploying an application. 
For example, you can launch Amazon Elastic Compute Cloud (Amazon EC2) instances when needed and pay only for the compute time you use. Instead of paying for resources that are unused or dealing with limited capacity, you can access only the capacity that you need, and scale in or out in response to demand. 
* **Increase speed and agility.**
The flexibility of cloud computing makes it easier for you to develop and deploy applications.
This flexibility also provides your development teams with more time to experiment and innovate.
* **Stop spending money running and maintaining data center**
Cloud computing in data centers often requires you to spend more money and time managing infrastructure and servers. 
A benefit of cloud computing is the ability to focus less on these tasks and more on your applications and customers.
* **Go global in minutes.**
The AWS Cloud global footprint enables you to quickly deploy applications to customers around the world, while providing them with low latency.
   
</details>
