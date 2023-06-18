# Learning-AWS-practitioner-essentials

<img width="1190" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/14e7103b-fc64-4a6f-b0a8-f9b6946541d5">

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
  * Cloud architect: Is the subject matter expert for the team. Is the tipical lateral move for an IT solution Architect
  * 🟣 AWS System Operation(SysOps):  It oversees the server, network and desktop teams
  * System Administrator: Must be proficient with configuration management and changes.
  * Security administrator
  * 🔵 Devops administrator: Build and operate fast and scalable workflows, implementing continous build, integration, deployment and infrastructure code. Must be proficient with programming scripting languages and also oversee database and developer teams.

## AWS cloud practitioner essentials

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

The AWS service provides access to virtual servers. It's highly flexible, cost-effective, and quick (secure, compute rezible capacity). AWS builds and secure the datacenters, puchase and install sesrvers, and the servers are online and ready to use
* Multitenancy: sharing underlying hardware between virtual machines. is manage by AWS


### Amazon EC2 configuration:

**<div align="center">(🚀 Launch  🖥️  Conect  📧 Use )</div>**

🚀 Operating system: you can choose eaither Windows or Linux </br>
🚀 Aplication(s) server: Software running on the instance Internal buisiness apps, web apps, Data bases, thir-part applications...</br>
🚀 Instance type</br>
* Vertical Scaling: EC2 instances are also resizable. You might start with a small instance, realize the application you are running is starting to max out that server, and then you can give that instance more memory and more CPU.</br>
🚀Control over the Networking: Type of requests</br>

### Amazon EC2 types:
Each Amazon EC2 instance type is grouped under an instance family and optimized for certain types of tasks. Instance types offer varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications.
* **General purpose instances:** Provide a balance of compute, memory, and networking resources (Application, gaming and backend services and small and medium databases)
* **Compute optimized instances:** Ideal for compute-bound applications that benefit from high-performance processors for instances processing workloads that require processing many transactions in a single group.
* **Memory optimized instances:** are designed to deliver fast performance for workloads that process large datasets in memory for instance workload that requires large amounts of data to be preloaded before running aplications (Ideal for high-performance databases)
* **Accelerated computing instances:** use hardware accelerator or coprocessors, to perform some functions more efficiently than possible in software running on CPUs for instance floating-point number calculations, graphic processing and data pattern matching (ideal for streaming)
* **Storage optimized instances:**  are designed for workloads that require high, sequential read and write access to large datasets on local storage. (Suitable for data warehousing applications)

### Purchase options:
+ **On-Demand:** Ideal for short-term, irregular workloads that cannot be interrupted. No upfront cost or minimum contract applies.
+ **Savings plans:** Reduce your compute costs by committing to a consistent amount of compute usage for a 1- or 3-year term. This term commitment results in savings of up to 72% over ON-Demand costs
+ **Reserved instances:** are ideal for workloads with flexible start and end times, or that can withstand interruptions.
+ **Spot instances:** workloads that can be interrupted
+ **Dedicated host:** are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use.

### Scalability and Elasticity:
**Scalability** involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. 
* **Amazon EC2 Auto Scaling:** Is service provide for Amazon EC2 instaces that alllows you to scaling process to happen automatically. Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand.
  * **Dynamic scaling** responds to changing demand.
  * **Predictive scaling** automatically schedules the right number of Amazon EC2 instances based on predicted demand.
  * When configuring the size of an auto scaling group, you can set ***minimum capacity***, ***Desired capacity*** and ***Maximum capacity***

### Elastic Load Balancing:
Is the AWS service that automatically distributes incoming application traffic across multiple resources, such as Amazon EC2 instances. For example, if you have multiple Amazon EC2 instances, Elastic Load Balancing distributes the workload across the multiple instances so that no single instance has to carry the bulk of it. 
Properly distribute traffic; high performance, cost-efficient, highly available, automatically scalable 

<div class="row" align="center">
    <img width="450" alt="image" src="https://github.com/CarolinaChavezDavid/learning-AWS-practitioner-essentials/assets/77591347/ee9834e8-4235-4c9e-87c0-3aa2ce7159f2">
</div>









