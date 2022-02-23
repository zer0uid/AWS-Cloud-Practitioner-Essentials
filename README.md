[Course URL](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/134/aws-cloud-practitioner-essentials?dt=tile&tile=fdt)

---
# Module 1
> What is Cloud Computing: The on-demand delivery of IT resources over the internet with pay-as-you-go pricing.

## Cloud Deployment Models
1. Cloud-Based Deployment
	- Run all parts of the application in the cloud
	- Migrate existing applications into the cloud
	- Design and build new applications in the cloud

2. On-Premisis Deployment
	-   Deploy resources by using virtualization and resource management tools.
	-   Increase resource utilization by using application management and virtualization technologies.

3. Hybrid Deployment
	-   Connect cloud-based resources to on-premises infrastructure.
	-   Integrate cloud-based resources with legacy IT applications.

---
# Module 2 - Compute in the Cloud
Vertically Scaling - Adding more memory & CPU to Virtual Machine

## EC Instance Families (Types) 
[Reference URL](https://aws.amazon.com/ec2/instance-types/)
- **General Purpose** provide a balance of compute, memory, and networking resources. You can use them for a variety of workloads
- **Compute Optimized** are ideal for compute-bound applications that benefit from high-performance processors. Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers.
- **Memory Optimized** are designed to deliver fast performance for workloads that process large datasets in memory. In computing, memory is a temporary storage area. It holds all the data and instructions that a central processing unit (CPU) needs to be able to complete actions. Before a computer program or application is able to run, it is loaded from storage into memory. This preloading process gives the CPU direct access to the computer program.
- **Accelerated computing** use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include floating-point number calculations, graphics processing, and data pattern matching.
- **Storage Optimized** are designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage optimized instances include distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems.

## Amazon EC2 pricing
**On-Demand Instances** are ideal for short-term, irregular workloads that cannot be interrupted. No upfront costs or minimum contracts apply. The instances run continuously until you stop them, and you pay for only the compute time you use.

**Amazon EC2 Savings Plans** enable you to reduce your compute costs by committing to a consistent amount of compute usage for a 1-year or 3-year term. This term commitment results in savings of up to 66% over On-Demand costs.

**Reserved Instances** are a billing discount applied to the use of On-Demand Instances in your account. You can purchase Standard Reserved and Convertible Reserved Instances for a 1-year or 3-year term, and Scheduled Reserved Instances for a 1-year term. You realize greater cost savings with the 3-year option.

**Spot Instances** are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at up to 90% off of On-Demand prices.

**Dedicated Hosts** are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use.

## Scaling Amazon EC2
**Scalability** involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. As a result, you pay for only the resources you use. You don’t have to worry about a lack of computing capacity to meet your customers’ needs.

If you wanted the scaling process to happen automatically, which AWS service would you use? The AWS service that provides this functionality for Amazon EC2 instances is **Amazon EC2 Auto Scaling**.

Within **Amazon EC2 Auto Scaling**, you can use two approaches: dynamic scaling and predictive scaling.

-   _Dynamic scaling_ responds to changing demand. 
-   _Predictive scaling_ automatically schedules the right number of Amazon EC2 instances based on predicted demand.

*(To scale faster, you can use dynamic scaling and predictive scaling together.*)

#### Auto Scaling Group
You set 3 parameters for this group
- Minimum Capacity
- Desired Capacity
- Maximum Capacity

## Elastic Load Balancing (ELB)
Runs at the **region** level rather than the EC2 instance level.  The service is automatically highly available with no additional effort.  ELB is regional, it's a single URL that each front end instance uses. Then the ELB directs traffic to the back end that has the least outstanding requests.

Although Elastic Load Balancing and Amazon EC2 Auto Scaling are separate services, they work together to help ensure that applications running in Amazon EC2 can provide high performance and availability.

**Amazon Simple Queue Service (Amazon SQS)** is a message queuing service. 
- Using Amazon SQS, you can send, store, and receive messages between software components, without losing messages or requiring other services to be available. In Amazon SQS, an application sends messages into a queue. A user or service retrieves a message from the queue, processes it, and then deletes it from the queue.

**Amazon Simple Notification Service (Amazon SNS)** is a publish/subscribe service. 
- Using Amazon SNS topics, a publisher publishes messages to subscribers.  Subscribers can be web servers, email addresses, AWS Lambda functions, or several other options.

## Serverless computing
The term “serverless” means that your code runs on servers, but you do not need to provision or manage these servers.
Another benefit of serverless computing is the flexibility to scale serverless applications automatically. Serverless computing can adjust the applications' capacity by modifying the units of consumptions, such as throughput and memory. 

An AWS service for serverless computing is **AWS Lambda**.

### AWS Lambda
[AWS Lambda](https://aws.amazon.com/lambda) is a service that lets you run code without needing to provision or manage servers.  You only pay for compute time that you consume.  Charges only apply when your code is running.  No administration involved.

- Upload code to Lambda
- Set your code to trigger from an event source, like AWS services, mobile app, or HTTP endpoint.
- Lambda runs your code only when triggered.
- You only pay for what you use

### Containers
[**Amazon Elastic Container Service (Amazon ECS)**](https://aws.amazon.com/ecs/) is a highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS.  Amazon ECS supports _Docker_ containers.

[**Amazon Elastic Kubernetes Service (Amazon EKS)**](https://aws.amazon.com/eks/) is a fully managed service that you can use to run _Kubernetes_ on AWS.
	[Kubernetes](https://kubernetes.io/) is open-source software that enables you to deploy and manage containerized applications at scale.

[**AWS Fargate**](https://aws.amazon.com/fargate/) is a serverless compute engine for containers. It works with both *Amazon ECS* and _Amazon EKS_.  You do not need to provision or manage servers. AWS Fargate manages your server infrastructure for you.


**Additional resources**

To learn more about the concepts that were explored in Module 2, review these resources.

-   [Compute on AWS](https://aws.amazon.com/products/compute)
-   [AWS Compute Blog](https://aws.amazon.com/blogs/compute/)
-   [AWS Compute Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)
-   [Hands-On Tutorials: Compute](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23compute&awsf.getting-started-content-type=content-type%23hands-on)
-   [Category Deep Dive: Serverless](https://aws.amazon.com/getting-started/deep-dive-serverless/)
-   [AWS Customer Stories: Serverless](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23serverless)

---
# Module 3

## AWS global infrastructure
Locations like Paris, Tokyo, Sao Paulo, Dublin, Ohio.  Inside each region is multiple data centers that all have the AWS services.  Each Region can be connected to other Regions through fiber network.  Each region is isolated from every other Region.  Data from that Region will never leave, unless explicit permitted (_Regional data sovereignty_).

*Business Decisions for choosing region*
1. Compliance
2. Proximity
	1. Where is primary customer base?
3. Feature Availability
	1. Not every region has every AWS feature
4. Pricing
	1. Some regions tax structure is more

Availability Zone = A single, or multiple data-centers within a *Region*. (AZed's)

An AWS Region is made up of _multiple_ "Availability Zones".  

***Best practice: Run multiple EC2 isntances in at least two Availability Zones in a Region***

Services listed as **Regionally scoped service** already run across multiple AZed's

### Edge Locations
An **edge location** is a site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.

#### Amazon CloudFront 
Same as CDN (Content Delivery Network)
Also runs DNS (Amazon Route 53)

#### AWS Outposts
Amazon will install on-site in your own building, same services are available.

#### Key Points
- Regions are geographically isolated areas
- Regions contain Availability Zones
- Edge locations run Amazon CloudFront

### How to provision AWS resources

Everything is an *API call* (Application programming interface).  You can interact with AWS services with:
- **AWS Management Console**
	- Web-based interface for accessing and managing AWS services
	- Great for testing, lab environments, non-production use.
- **AWS Command Line Interface (CLI)**
	- Enables you to control multiple AWS services directly from the command line.
	- Make API calls, can be scripted and repeatable; scheduled or triggered.  Automation capable
		- For example, you can use commands to launch an Amazon EC2 instance, connect an Amazon EC2 instance to a specific Auto Scaling group, and more.
- **AWS Software Development Kits (SDKs)**
	- Interact with AWS resources with various programming languages; without using low-level APIs
	- Supported programming languages include C++, Java, .NET, and more.
- **Various other tools**

### AWS Managed Tools
**AWS Elastic Beanstalk**
You provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:
	-   Adjust capacity
	-   Load balancing
	-   Automatic scaling
	-   Application health monitoring

**AWS CloudFormation: Infrastructure as code**
Build an environment by writing lines of code instead of using the AWS Management Console to individually provision resources.

AWS CloudFormation provisions your resources in a safe, repeatable manner, enabling you to frequently build your infrastructure and applications without having to perform manual actions. It determines the right operations to perform when managing your stack and rolls back changes automatically if it detects errors.  

#### Additional resources
-   [Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
-   [Interactive map of the AWS Global Infrastructure](https://www.infrastructure.aws/)
-   [Regions and Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az)
-   [AWS Networking and Content Delivery Blog](https://aws.amazon.com/blogs/networking-and-content-delivery/)
-   [Tools to Build on AWS](https://aws.amazon.com/tools/)
-   [AWS Customer Stories: Content Delivery](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23content-delivery)
---
# Module 4 -  Networking

## Virtual Private Cloud (VPC)
Private IP range, contains Elastic Load Balancer >EC2 Instances & Database(s) .  
- Use **IG** (Internet Gateway) to control public access to resource inside VPC.
	- An internet gateway is a connection between a VPC and the internet.
- Use **VPG** (Virtual Private Gateway) to restrict *only* **Private** traffic to VPC. (*AKA Encrypted VPN Tunnel*).
	- Establish connection between VPC and private network; on-prem data center or internal corporate network.
	- Only allows traffic into VPC if it's from an approved network.
- **AWS Direct Connect **
	- Private dedicated fiber connection from your network to your VPC.

Within a virtual private cloud (VPC), you can organize your resources into subnets. A **subnet** is a section of a VPC that can contain resources such as Amazon EC2 instances.

**Internet Gateway**
![](https://assets.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1645074000/NtwMbSMph3MIi0h6H7HrNw/tincan/31d9c0cca79c54bdceaf3e938fd424e97c98c7e8/assets/Q_HnMl_BAEsDZGxf_NEblbQjD0vn0-pPU.png)
**Virtual Private Gateway**
![](https://assets.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1645074000/NtwMbSMph3MIi0h6H7HrNw/tincan/31d9c0cca79c54bdceaf3e938fd424e97c98c7e8/assets/tthacSS-FyYNWwE3_s8U3lQzEONXm1FMX.png)

**AWS DirectConnect**
![](https://assets.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1645074000/NtwMbSMph3MIi0h6H7HrNw/tincan/31d9c0cca79c54bdceaf3e938fd424e97c98c7e8/assets/p53HDtoqu2euSy0Y_YdzRvczPABE_j-yV.png)

### Subnets and Network Access Control Lists (ACLs)
A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private.
- **Public subnets** contain resources that need to be accessible by the public, such as an online store’s website.
- **Private subnets** contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories.
![](https://assets.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1645074000/NtwMbSMph3MIi0h6H7HrNw/tincan/31d9c0cca79c54bdceaf3e938fd424e97c98c7e8/assets/-HQN-9SqkWc5e-yv_pi4TpfvEYaalWuIu.png)


### Network Access Control Lists (ACLs)
A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.

By default, your account’s default network ACL allows all inbound and outbound traffic, but you can modify it by adding your own rules. For custom network ACLs, all inbound and outbound traffic is denied until you add rules to specify which traffic to allow. Additionally, all network ACLs have an explicit deny rule.

#### Stateless packet filtering
Network ACLs perform **stateless** packet filtering. They remember nothing and check packets that cross the subnet border each way: inbound and outbound.

The VPC component that checks packet permissions for an Amazon EC2 instance is a [**security group**](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html).

#### Security Groups
A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.  By default, a security group denies all inbound traffic and allows all outbound traffic. You can add custom rules to configure which traffic to allow or deny.
#### Stateful packet filtering
Security groups perform **stateful** packet filtering. They remember previous decisions made for incoming packets.

## Amazon Route 53

[**Amazon Route 53**](https://aws.amazon.com/route53) is a DNS web service.  Amazon Route 53 connects user requests to infrastructure running in AWS (such as Amazon EC2 instances and load balancers). It can route users to infrastructure outside of AWS.

**Example: How Amazon Route 53 and Amazon CloudFront deliver content**
![](https://assets.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1645074000/NtwMbSMph3MIi0h6H7HrNw/tincan/31d9c0cca79c54bdceaf3e938fd424e97c98c7e8/assets/mR1nvYoC4OSUVg9a_WE71CA369xcdceJ2.png)

#### Additional Resources
-   [Networking and Content Delivery on AWS](https://aws.amazon.com/products/networking)
-   [AWS Networking & Content Delivery Blog](https://aws.amazon.com/blogs/networking-and-content-delivery/)
-   [Amazon Virtual Private Cloud](https://aws.amazon.com/vpc)
-   [What is Amazon VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
-   [How Amazon VPC works](https://docs.aws.amazon.com/vpc/latest/userguide/how-it-works.html)
---

# Module 5
## Storage and Databases

### Instance stores and Amazon Elastic Block Store (EBS)
 *Block-level storage* volumes behave like **physical hard drive**. Good for Databases, Enterprise software, and file systems. 

#### Instance Stores
An [**instance store**](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) provides temporary block-level storage for an Amazon EC2 instance. An instance store is disk storage that is physically attached to the host computer for an EC2 instance, and therefore has the same lifespan as the instance. When the instance is terminated, you lose any data in the instance store.

 *Instance Store Volumes* are attached to EC2 hosts.  IF you stop or remove the instance, all data will be removed with it.  If you stop an EC2 instance, and start it up, it may start up on a different host; and therefore not have the storage attached.
 - Useful for data where you can lose it (temp files, swap, etc)

### Amazon EBS
[**Amazon Elastic Block Store (Amazon EBS)**](https://aws.amazon.com/ebs) is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. EBS volumes are not tied to your host and can *persist* between stop and starts of the EC2 instance.  Define size, type, and configurations and attache to EC2 instance.  Configure EC2 to use EBS volume.

#### Amazon EBS snapshot
An [**EBS snapshot**](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html) is an *incremental backup*. This means that the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved. 

*Incremental backups* are different from full backups, in which all the data in a storage volume copies each time a backup occurs. The full backup includes data that has not changed since the most recent backup.


### Amazon Simple Storage Service (Amazon S3)
#### Object Storge (Stored in "buckets")
In **object storage**, each object consists of **data, metadata, and a key**.  The data might be an image, video, text document, or any other type of file. Metadata contains information about what the data is, how it is used, the object size, and so on. An object’s key is its unique identifier.

Store data as objects, store objects in buckets, Max Upload size = 5TB, version objects, create multiple buckets. Create permissions to control access.

#### S3 Standard 
- (11 9's durability up to 1 year)
- Good for static website hosting

#### S3 Standard-Infrequent Access (S3 Standard-IA)
-   Ideal for infrequently accessed data
-   Similar to S3 Standard but has a lower storage price and higher retrieval price

#### S3 One Zone-Infrequent Access (S3 One Zone-IA)
-   Stores data in a single Availability Zone
-   Has a lower storage price than S3 Standard-IA
-   You want to save costs on storage.
-   You can easily reproduce your data in the event of an Availability Zone failure.

#### S3 Intelligent-Tiering
-   Ideal for data with unknown or changing access patterns
-   Requires a small monthly monitoring and automation fee per object

#### S3 Glacier
-   Low-cost storage designed for data archiving
-   Able to retrieve objects within a few minutes to hours

#### S3 Glacier Deep Archive
-   Lowest-cost object storage class ideal for archiving
-   Able to retrieve objects within 12 hours

**Lifecycle Policy** are rules set on when to move data between tiers and for how long.

##### Comparing Amazon EBS and Amazon S3
**Amazon Elastic Block Store (EBS)**
- Sizes up to 15 TiB
- Survive termination of EC2 instance
- Solid state by default
- HDD option


### Amazon Simple Storage Service (S3)
- Unlimited storage
- Individual objects up to 5TB
- Write once/read many
- 99.9999999% durability (over 1 year)
- Web enabled
- Regionally distributed
- Cost savings
- Serverless

### Amazon Elastic File System (EFS)
Multiple EC2 instances can access the data in EFS at the same time.  Managed file system, can scale up and down without intervention from the customer.

#### EBS vs EFS
##### Elastic Block Storage (EBS)
- Volumes attach to EC2 instances
- Availability Zone level resource
- Need to be in the same Availability Zone as the attached EC2 instance.
- Volumes **do not automatically scale**
##### Amazon Elastic File System (EFS)
- Multiple instances reading and writing simultaneously
- Linux file system
- Regional resource
- Automatically scales
- On-premises servers can access using AWS Direct Connect

### Amazon Relational Database service (RDS)
In a **relational database**, data is stored in a way that relates it to other pieces of data.  Relational databases use **structured query language (SQL)** to store and query data. This approach allows data to be stored in an easily understandable, consistent, and scalable way.

Customers can *Lift-and-shift* migration to move their workload to Amazon EC2;quick entry to the cloud.

#### Amazon RDS
[**Amazon Relational Database Service (Amazon RDS)**](https://aws.amazon.com/rds/) is a service that enables you to run relational databases in the AWS Cloud.  Amazon RDS is a managed service that automates tasks such as hardware provisioning, database setup, patching, and backups.  Many RDS database engines offer encryption at rest and encryption in transit.

**Amazon RDS offers:**
- Automated patching
- Backups
- Redundancy
- Failover
- Disaster recovery

Amazon RDS is available in 6 DB engines, optimized for memory, performance, or I/O.  Supported DB engines include:
- Amazon Aurora
- PostgreSQL
- MySQL
- MariaDB
- Oracle Database
- Microsoft SQL Server

#### Amazon Aurora
Another option for DB migration.  Supports the following:
- MySQL
- PostgreSQL
- 1/10th of the cost of commercial databases
- Data replication 
- Up to 15 read replicas
- Continuous backups to Amazon S3
- Point-in-time recovery

Aurora is 5x faster than standard MySQL DB's and up to 3x faster than PostgreSQL DB's.  It replicates six copies of your data across 3 Availability Zones and continuously backs up your data to Amazon S3.

#### Amazon DynamoDB
[**Amazon DynamoDB**](https://aws.amazon.com/dynamodb/) is a key-value database service. It delivers single-digit millisecond performance at any scale.

A non-relational serverless database, don't need to manage underlying instances or infrastructure.  DynamoDB manages underlying data and scales it for you.  Data is organized as items, items have attributes. Highly scalable and speed, less than 1ms response time.  It does not use SQL, no relation table structure.  Queries are run against "keys", instead of complex SQL queries.
- Non-relational, NoSQL database
- Purpose built
- Millisecond response time
- Fully managed
- Highly scalable

**Amazon DynamoDB**
- Key-value
- Massive throughput capabilities
- PB size potential
- Granular API access

#### Amazon Redshift
[**Amazon Redshift**](https://aws.amazon.com/redshift) is a data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data. 

#### AWS Database Migration Service (AWS DMS)
[**AWS Database Migration Service (AWS DMS)**](https://aws.amazon.com/dms/) enables you to migrate relational databases, nonrelational databases, and other types of data stores.

- The source database remains fully operation during migration
- Downtime is minimized for applications that rely on that database
- The source and target databases don't have to be of the same type.

*Homogeneous* - Same DB type migration
- Create a task, simple 1-click migration
*Heterogeneous* - Different DB type migration
- 2 step, convert scheme then migrate

[AWS Database Migration Service Resources - Amazon Web Services](https://aws.amazon.com/dms/resources/)

**Use case for AWS DMS**
- Development and test database migration
- Database consolidation
- Continuous replication

##### Additional database services
- Amazon DocumentDB
	- [**Amazon DocumentDB**](https://aws.amazon.com/documentdb) is a document database service that supports MongoDB workloads. (MongoDB is a document database program.)
- Amazon Neptune
	- [**Amazon Neptune**](https://aws.amazon.com/neptune) is a graph database service.
- Amazon Quantum Ledger Database (Amazon QLDB)
	- [**Amazon Quantum Ledger Database (Amazon QLDB)**](https://aws.amazon.com/qldb) is a ledger database service.
- Amazon Managed Blockchain
	- [**Amazon Managed Blockchain**](https://aws.amazon.com/managed-blockchain) is a service that you can use to create and manage blockchain networks with open-source frameworks.
- Amazon ElastiCache
	- [**Amazon ElastiCache**](https://aws.amazon.com/elasticache) is a service that adds caching layers on top of your databases to help improve the read times of common requests.
- Amazon DynamoDB Accelerator
	- [**Amazon DynamoDB Accelerator (DAX)**](https://aws.amazon.com/dynamodb/dax/) is an in-memory cache for DynamoDB.

###### Additional resources
-   [Cloud Storage on AWS](https://aws.amazon.com/products/storage)
-   [AWS Storage Blog](https://aws.amazon.com/blogs/storage/)
-   [Hands-On Tutorials: Storage](https://aws.amazon.com/getting-started/hands-on/?awsf.getting-started-category=category%23storage&awsf.getting-started-content-type=content-type%23hands-on)
-   [AWS Customer Stories: Storage](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23storage)
-   [AWS Database Migration Service](https://aws.amazon.com/dms/)
-   [Databases on AWS](https://aws.amazon.com/products/databases)
-   [Category Deep Dive: Databases](https://aws.amazon.com/getting-started/deep-dive-databases/)
-   [AWS Database Blog](https://aws.amazon.com/blogs/database/)
-   [AWS Customer Stories: Databases](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23databases)

# Module 6
## Security
### AWS Shared Responsibility Module
#### Customers: Security in the cloud
**Customers** are responsible for the security of everything that they create and put _in_ the AWS Cloud.

Customers maintain complete control over content. You are responsible for managing security requirements for your content, including which content you choose to store on AWS, which AWS services you use, and who has access to that content. You also control how access rights are granted, managed, and revoked.

Steps include selecting, configuring, and patching the operating systems that will run on Amazon EC2 instances, configuring security groups, and managing user accounts.

#### AWS: Security of the cloud
**AWS** is responsible for security _of_ the cloud.

AWS manages all layers of infrastructure. The host operating system, the virtualization layer, and the physical security of the data centers . 

AWS  is responsible for global infrastructure; which includes AWS Regions, Availability Zones, and edge locations.

AWS manages the security of the cloud, specifically the physical infrastructure that hosts your resources, which include:

-   Physical security of data centers
-   Hardware and software infrastructure
-   Network infrastructure
-   Virtualization infrastructure

### User permissions and access
[**AWS Identity and Access Management (IAM)**](https://aws.amazon.com/iam/) enables you to manage access to AWS services and resources securely.

IAM Features:
-   IAM users, groups, and roles
-   IAM policies
-   Multi-factor authentication

#### AWS account root user (Enable MFA on this account)
When you first create an AWS account, you begin with an identity known as the [**root user**](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html).

```ad-note
Best practice:

Do **not** use the root user for everyday tasks. 

Instead, use the root user to create your first IAM user and assign it permissions to create other users.

Then, continue to create other IAM users, and access those identities for performing regular tasks throughout AWS. Only use the root user when you need to perform a limited number of tasks that are only available to the root user. Examples of these tasks include changing your root user email address and changing your AWS support plan. 
```
##### IAM user
An **IAM user** is an identity that you create in AWS. It represents the person or application that interacts with AWS services and resources. It consists of a name and credentials.

```ad-note
Best practice:

We recommend that you create individual IAM users for each person who needs to access AWS.  

Even if you have multiple employees who require the same level of access, you should create individual IAM users for each of them. This provides additional security by allowing each IAM user to have a unique set of security credentials.
```

##### IAM policies
An **IAM** **policy** is a document that allows or denies permissions to AWS services and resources.

```ad-note
Best practice:

Follow the security principle of **least privilege** when granting permissions. 

By following this principle, you help to prevent users or roles from having more permissions than needed to perform their tasks. 

For example, if an employee needs access to only a specific bucket, specify the bucket in the IAM policy. Do this instead of granting the employee access to all of the buckets in your AWS account.
```
```
This example IAM policy allows permission to view a list of objects in the Amazon S3 bucket with ID awsdoc-example-bucket, and also access them.
```

##### IAM groups

An IAM group is a collection of IAM users. When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.

##### IAM roles
An IAM role is an identity that you can assume to gain temporary access to permissions.  When someone assumes an IAM role, they abandon all previous permissions that they had under a previous role and assume the permissions of the new role. 
```ad-note
Best practice:

IAM roles are ideal for situations in which access to services or resources needs to be granted temporarily, instead of long-term.
```

##### AWS Organizations
You can use [**AWS Organizations**](https://aws.amazon.com/organizations) to consolidate and manage multiple AWS accounts within a central location.  When you create an organization, AWS Organizations automatically creates a **root**, which is the parent container for all the accounts in your organization.

In AWS Organizations, you can centrally control permissions for the accounts in your organization by using [**service control policies (SCPs)**](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html). SCPs enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.

### Compliance
[**AWS Artifact**](https://aws.amazon.com/artifact) is a service that provides on-demand access to AWS security and compliance reports and select online agreements. AWS Artifact consists of two main sections: **AWS Artifact Agreements** and **AWS Artifact Reports.**

**AWS Artifact Agreements**
- AWS Artifact Agreements, you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations. Different types of agreements are offered to address the needs of customers who are subject to specific regulations, such as the Health Insurance Portability and Accountability Act (HIPAA).

**AWS Artifact Reports**
- AWS Artifact Reports provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations. AWS Artifact Reports remains up to date with the latest reports released. You can provide the AWS audit artifacts to your auditors or regulators as evidence of AWS security controls.

 **Customer Compliance Center**
 The [**Customer Compliance Center**](https://aws.amazon.com/compliance/customer-center/) contains resources to help you learn more about AWS compliance.

 You can also access compliance whitepapers and documentation on topics such as:
- AWS answers to key compliance questions
-   An overview of AWS risk and compliance
-   An auditing security checklist

### Denial-of-service attacks
A **denial-of-service (DoS) attack** is a deliberate attempt to make a website or application unavailable to users.

#### AWS Shield

AWS Shield is a service that protects applications against DDoS attacks. AWS Shield provides two levels of protection: Standard and Advanced.

**AWS Shield Standard** automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frequently occurring types of DDoS attacks. 
- As network traffic comes into your applications, AWS Shield Standard uses a variety of analysis techniques to detect malicious traffic in real time and automatically mitigates it.

**AWS Shield Advanced** is a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. 
- It also integrates with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks.

### Additional Security Services

##### AWS Key Management Services (AWS KMS)
[**AWS Key Management Service (AWS KMS)**](https://aws.amazon.com/kms) enables you to perform encryption operations through the use of **cryptographic keys**. A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data. You can use AWS KMS to create, manage, and use cryptographic keys.

##### AWS Web Application Firewall (WAF)
[**AWS WAF**](https://aws.amazon.com/waf) is a web application firewall that lets you monitor network requests that come into your web applications.  AWS WAF works together with Amazon CloudFront and an Application Load Balancer.

AWS WAF uses a [**web access control list (ACL)**](https://docs.aws.amazon.com/waf/latest/developerguide/web-acl.html) to protect your AWS resources.

##### Amazon Inspector
[**Amazon Inspector**](https://aws.amazon.com/inspector/) helps to improve the security and compliance of applications by running automated security assessments. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to Amazon EC2 instances and installations of vulnerable software versions.

##### Amazon GuardDuty
[**Amazon GuardDuty**](https://aws.amazon.com/guardduty) is a service that provides intelligent threat detection for your AWS infrastructure and resources. It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.  

GuardDuty then continuously analyzes data from multiple AWS sources, including VPC Flow Logs and DNS logs.
	- You can also configure AWS Lambda functions to take remediation steps automatically in response to GuardDuty’s security findings.

###### Additional resources

To learn more about the concepts that were explored in Module 6, review these resources.

-   [Security, Identity, and Compliance on AWS](https://aws.amazon.com/products/security)
-   [Whitepaper: Introduction to AWS Security](https://docs.aws.amazon.com/whitepapers/latest/introduction-aws-security/welcome.html)[](https://docs.aws.amazon.com/whitepapers/latest/aws-security-best-practices/know-the-aws-shared-responsibility-model.html)
-   [Whitepaper: Amazon Web Services - Overview of Security Processes](https://docs.aws.amazon.com/whitepapers/latest/aws-overview-security-processes/aws-overview-security-processes.pdf)
-   [AWS Security Blog](https://aws.amazon.com/blogs/security/)
-   [AWS Compliance](https://aws.amazon.com/compliance)
-   [AWS Customer Stories: Security, Identity, and Compliance](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23security-identity-compliance)

# Module 7
## Monitoring your AWS environment
### Amazon CloudWatch
[**Amazon CloudWatch**](https://aws.amazon.com/cloudwatch/) is a web service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics.

**CloudWatch alarms**
With CloudWatch, you can create [**alarms**](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) that automatically perform actions if the value of your metric has gone above or below a predefined threshold.

The CloudWatch [**dashboard**](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html) feature enables you to access all the metrics for your resources from a single location.

### AWS CloudTrail
[**AWS CloudTrail**](https://aws.amazon.com/cloudtrail/) records API calls for your account. The recorded information includes the identity of the API caller, the time of the API call, the source IP address of the API caller, and more.

**CloudTrail Insights**
Within CloudTrail, you can also enable [**CloudTrail Insights**](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-insights-events-with-cloudtrail.html). This optional feature allows CloudTrail to automatically detect unusual API activities in your AWS account.

**AWS Trusted Advisor**
[**AWS Trusted Advisor**](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) is a web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices.

Trusted Advisor compares its findings to AWS best practices in five categories: 
- cost optimization
- performance
- security
- fault tolerance
- service limits. 

For the checks in each category, Trusted Advisor offers a list of recommended actions and additional resources to learn more about AWS best practices.

##### Additional resources
-   [Management and Governance on AWS](https://aws.amazon.com/products/management-tools)
-   [Monitoring and Observability](https://aws.amazon.com/products/management-tools/use-cases/monitoring-and-observability/)
-   [Configuration, Compliance, and Auditing](https://aws.amazon.com/products/management-tools/use-cases/configuration-compliance-and-auditing/)
-   [AWS Management & Governance Blog](https://aws.amazon.com/blogs/mt/)
-   [Whitepaper: AWS Governance at Scale](https://docs.aws.amazon.com/whitepapers/latest/aws-governance-at-scale/introduction.html)
---
# Module 8
## Pricing & Support
### AWS Free Tier
The [AWS Free Tier](https://aws.amazon.com/free/) enables you to begin using certain services without having to worry about incurring costs for the specified period.

Three types of offers are available: 
-   Always Free
-   12 Months Free
-   Trials

### AWS Pricing Concepts
The [**AWS Pricing Calculator**](https://calculator.aws/#/) lets you explore AWS services and create an estimate for the cost of your use cases on AWS. You can organize your AWS estimates by groups that you define. A group can reflect how your company is organized, such as providing estimates by cost center.

**AWS Lambda**
To learn more about [AWS Lambda pricing](https://aws.amazon.com/lambda/pricing/)

**Amazon EC2**
To learn more about [Amazon EC2 pricing](https://aws.amazon.com/ec2/pricing/)

**Amazon S3**
To learn more about [Amazon S3 pricing](https://aws.amazon.com/s3/pricing/)

### Billing Dashboard
Use the [**AWS Billing & Cost Management dashboard**](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html) to pay your AWS bill, monitor your usage, and analyze and control your costs.
-   Compare your current month-to-date balance with the previous month, and get a forecast of the next month based on current usage.
-   View month-to-date spend by service.
-   View Free Tier usage by service.
-   Access Cost Explorer and create budgets.
-   Purchase and manage Savings Plans.
-   Publish [AWS Cost and Usage Reports](https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html).

**Consolidated billing**
AWS Organizations also provides the option for [**consolidated billing**](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/consolidated-billing.html). 

The consolidated billing feature of AWS Organizations enables you to receive a single bill for all AWS accounts in your organization. By consolidating, you can easily track the combined costs of all the linked accounts in your organization. The default maximum number of accounts allowed for an organization is 4, but you can contact AWS Support to increase your quota, if needed.

**AWS Budgets**
In [**AWS Budgets**](https://aws.amazon.com/aws-cost-management/aws-budgets), you can create budgets to plan your service usage, service costs, and instance reservations.
The information in AWS Budgets updates three times a day.  In AWS Budgets, you can also set custom alerts when your usage exceeds (or is forecasted to exceed) the budgeted amount.

**AWS Cost Explorer**
[**AWS Cost Explorer**](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) is a tool that enables you to visualize, understand, and manage your AWS costs and usage over time.  AWS Cost Explorer includes a default report of the costs and usage for your top five cost-accruing AWS services. You can apply custom filters and groups to analyze your data.

**AWS Support Plans**
AWS offers four different [**Support plans**](https://aws.amazon.com/premiumsupport/plans/) to help you troubleshoot issues, lower costs, and efficiently use AWS services. 

You can choose from the following Support plans to meet your company’s needs: 
-   Basic
-   Developer
-   Business
-   Enterprise

**Technical Account Manager (TAM)**
The Enterprise Support plan includes access to a **Technical Account Manager (TAM)**.

If your company has an Enterprise Support plan, the TAM is your primary point of contact at AWS. They provide guidance, architectural reviews, and ongoing communication with your company as you plan, deploy, and optimize your applications. 

Your TAM provides expertise across the full range of AWS services. They help you design solutions that efficiently use multiple services together through an integrated approach.

**AWS Marketplace**
[**AWS Marketplace**](https://aws.amazon.com/marketplace) is a digital catalog that includes thousands of software listings from independent software vendors. You can use AWS Marketplace to find, test, and buy software that runs on AWS.

AWS Marketplace offers products in several categories, such as Infrastructure Products, Business Applications, Data Products, and DevOps.

##### Additional resources
-   [AWS Pricing](https://aws.amazon.com/pricing)
-   [AWS Free Tier](https://aws.amazon.com/free)
-   [AWS Cost Management](https://aws.amazon.com/aws-cost-management/)
-   [Whitepaper: How AWS Pricing Works](https://docs.aws.amazon.com/whitepapers/latest/how-aws-pricing-works/welcome.html)
-   [Whitepaper: Introduction to AWS Economics](https://d1.awsstatic.com/whitepapers/introduction-to-aws-cloud-economics-final.pdf)
-   [AWS Support](https://aws.amazon.com/premiumsupport)
-   [AWS Knowledge Center](https://aws.amazon.com/premiumsupport/knowledge-center/)
---
# Module 9
## Migration and Innovation
### AWS Cloud Adoption Framework (AWS CAF)
At the highest level, the [**AWS Cloud Adoption Framework (AWS CAF)**](https://d1.awsstatic.com/whitepapers/aws_cloud_adoption_framework.pdf) organizes guidance into six areas of focus, called **Perspectives**. Each Perspective addresses distinct responsibilities.

**Business Perspective**
 The **Business Perspective** ensures that IT aligns with business needs and that IT investments link to key business results.
Common roles in the Business Perspective include: 
-   Business managers
-   Finance managers
-   Budget owners
-   Strategy stakeholders

**People Perspective** 
The **People Perspective** supports development of an organization-wide change management strategy for successful cloud adoption.
Common roles in the People Perspective include: 
-   Human resources
-   Staffing
-   People managers

**Governance Perspective**
The **Governance Perspective** focuses on the skills and processes to align IT strategy with business strategy. This ensures that you maximize the business value and minimize risks.
Common roles in the Governance Perspective include: 
-   Chief Information Officer (CIO)
-   Program managers
-   Enterprise architects
-   Business analysts
-   Portfolio managers

**Platform Perspective**
The **Platform Perspective** includes principles and patterns for implementing new solutions on the cloud, and migrating on-premises workloads to the cloud.
Common roles in the Platform Perspective include: 
-   Chief Technology Officer (CTO)
-   IT managers
-   Solutions architects

**Security Perspective**
The **Security Perspective** ensures that the organization meets security objectives for visibility, auditability, control, and agility.
Common roles in the Security Perspective include: 
-   Chief Information Security Officer (CISO)
-   IT security managers
-   IT security analysts

**Operations Perspective**
The **Operations Perspective** helps you to enable, run, use, operate, and recover IT workloads to the level agreed upon with your business stakeholders.
Common roles in the Operations Perspective include: 
-   IT operations managers
-   IT support managers

### Migration Strategies
Six of the most common [migration strategies](https://aws.amazon.com/blogs/enterprise-strategy/6-strategies-for-migrating-applications-to-the-cloud/) that you can implement are:
-   Rehosting
	- also known as “lift-and-shift” involves moving applications without changes.
-   Replatforming
	- also known as “lift, tinker, and shift,” involves making a few cloud optimizations to realize a tangible benefit
-   Refactoring/re-architecting
	- involves reimagining how an application is architected and developed by using cloud-native features.
-   Repurchasing
	- involves moving from a traditional license to a software-as-a-service model.
-   Retaining
	- consists of keeping applications that are critical for the business in the source environment.
-   Retiring
	- is the process of removing applications that are no longer neede

### AWS Snow Family
The [**AWS Snow Family**](https://aws.amazon.com/snow) is a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS. 

AWS Snow Family is composed of **AWS Snowcone**, **AWS Snowball**, and **AWS Snowmobile**.
[**AWS Snowcone**](https://aws.amazon.com/snowcone) 
- Small, rugged, and secure edge computing and data transfer device.  It features 2 CPUs, 4 GB of memory, and 8 TB of usable storage.

[**AWS Snowball**](https://aws.amazon.com/snowball/)
- *Snowball Edge Storage Optimized* devices are for large scale migrations and reoccurring data transfers.
	 -   Storage: 80 TB of hard disk drive (HDD) capacity for block volumes and Amazon S3 compatible object storage, and 1 TB of SATA solid state drive (SSD) for block volumes. 
	-   Compute: 40 vCPUs, and 80 GiB of memory to support Amazon EC2 sbe1 instances (equivalent to C5).
- *Snowball Edge Compute Optimized* provides powerful computing resources for machine learning, full motion video analysis, analytics, etc.
	- Storage: 42-TB usable HDD capacity for Amazon S3 compatible object storage or Amazon EBS compatible block volumes and 7.68 TB of usable NVMe SSD capacity for Amazon EBS compatible block volumes. 
	- Compute: 52 vCPUs, 208 GiB of memory, and an optional NVIDIA Tesla V100 GPU. Devices run Amazon EC2 sbe-c and sbe-g instances, which are equivalent to C5, M5a, G3, and P3 instances.

### Innovations with AWS
**Serverless applications**
- With AWS, **serverless** refers to applications that don’t require you to provision, maintain, or administer servers. You don’t need to worry about fault tolerance or availability.

**Artificial intelligence**
-   Convert speech to text with Amazon Transcribe.
-   Discover patterns in text with Amazon Comprehend.
-   Identify potentially fraudulent online activities with Amazon Fraud Detector.
-   Build voice and text chatbots with Amazon Lex.

**Machine learning (ML)**
- AWS offers *Amazon SageMaker* to remove the difficult work from the process and empower you to build, train, and deploy ML models quickly.  You can use ML to analyze data, solve complex problems, and predict outcomes before they happen.

###### Additional Resources
-   [Migration & Transfer on AWS](https://aws.amazon.com/products/migration-and-transfer)
-   [A Process for Mass Migrations to the Cloud](https://aws.amazon.com/blogs/enterprise-strategy/214-2/)
-   [6 Strategies for Migrating Applications to the Cloud](https://aws.amazon.com/blogs/enterprise-strategy/6-strategies-for-migrating-applications-to-the-cloud/)
-   [AWS Cloud Adoption Framework](https://aws.amazon.com/professional-services/CAF/)
-   [AWS Fundamentals: Core Concepts](https://aws.amazon.com/getting-started/fundamentals-core-concepts/)
-   [AWS Cloud Enterprise Strategy Blog](https://aws.amazon.com/blogs/enterprise-strategy/)
-   [Modernizing with AWS Blog](https://aws.amazon.com/blogs/modernizing-with-aws/)
-   [AWS Customer Stories: Data Center Migration](https://aws.amazon.com/solutions/case-studies/?customer-references-cards.sort-by=item.additionalFields.publishedDate&customer-references-cards.sort-order=desc&awsf.customer-references-location=*all&awsf.customer-references-segment=*all&awsf.customer-references-product=product%23vpc%7Cproduct%23api-gateway%7Cproduct%23cloudfront%7Cproduct%23route53%7Cproduct%23directconnect%7Cproduct%23elb&awsf.customer-references-category=category%23datacenter-migration)
---
# Module 10
## The Cloud Journey

### AWS Well-Architected Framework
The [**AWS Well-Architected Framework**](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf) helps you understand how to design and operate reliable, secure, efficient, and cost-effective systems in the AWS Cloud.

**5 Pillars of Well-Architected Framework**
-   Operational excellence
	- the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures.
-   Security
	- The ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.
-   Reliability
	- Includes testing recovery procedures, scaling horizontally to increase aggregate system availability, and automatically recovering from failure.
-   Performance efficiency
	- The ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.
-   Cost optimization
	- The ability to run systems to deliver business value at the lowest price point.

### Benefits of AWS Cloud

Six advantages of cloud computing:
-   Trade upfront expense for variable expense.
	- include data centers, physical servers, and other resources that you would need to invest in before using computing resources.
-   Benefit from massive economies of scale.
	- Because usage from hundreds of thousands of customers aggregates in the cloud, providers such as AWS can achieve higher economies of scale.
-   Stop guessing capacity.
	- You don’t have to predict how much infrastructure capacity you will need before deploying an application.
-   Increase speed and agility.
	- Makes it easier for you to develop and deploy applications. More time for dev teams to experiment and innovate.
-   Stop spending money running and maintaining data centers.
	- data centers often requires you to spend more money and time managing infrastructure and servers.  Focus less on these and more on applications and customers.
-   Go global in minutes.
	- AWS Cloud global footprint enables you to quickly deploy applications to customers around the world, while providing them with low latency.

###### Additional resources
-   [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)
-   [Whitepaper: AWS Well-Architected Framework](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf)
-   [AWS Architecture Center](https://aws.amazon.com/architecture)
-   [Six Advantages of Cloud Computing](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html)
-   [AWS Architecture Blog](https://aws.amazon.com/blogs/architecture)
--- 

# Module 11
## AWS Certified Cloud Practitioner Basics
### Exam domains

The AWS Certified Cloud Practitioner exam includes four domains:

- 1 - Cloud Concepts
    
-  2 - Security and Compliance
    
-  3 - Technology
    
-   4 - Billing and Pricing
    

The areas covered describe each domain in the [Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf) for the AWS Certified Cloud Practitioner certification. For a description of each domain, review the [AWS Certified Cloud Practitioner website](https://aws.amazon.com/certification/certified-cloud-practitioner/). [](https://aws.amazon.com/certification/certified-cloud-practitioner)You are encouraged to read the information in the Exam Guide as part of your preparation for the exam.

Each domain in the exam is weighted. The weight represents the percentage of questions in the exam that correspond to that particular domain. These are approximations, so the questions on your exam may not match these percentages exactly. The exam does not indicate the domain associated with a question. In fact, some questions can potentially fall under multiple domains.

| Domain                          | Percentage of exam |
| ------------------------------- | ------------------ |
| Domain 1: Cloud Concepts        | 26%                |
| Domain 2: Security & Compliance | 25%                |
| Domain 3: Technology            | 33%                |
| Domain 4: Billing & Pricing     | 16%                |
| Total                           | 100%               |



You are encouraged to use these benchmarks to help you determine how to allocate your time studying for the exam.

**Recommended experience**

Candidates for the AWS Certified Cloud Practitioner exam should have a basic understanding of IT services and their uses in the AWS Cloud platform. 

We recommend that you have at least six months of experience with the AWS Cloud in any role, including project managers, IT managers, sales managers, decision makers, and marketers. These roles are in addition to those working in finance, procurement, and legal departments.

**Exam details**

The AWS Certified Cloud Practitioner exam consists of **65 questions** to be completed in **90 minutes**. The minimum passing score is **70%**.

Two types of questions are included on the exam: multiple choice and multiple response.

-   A **multiple-choice** question has one correct response and three incorrect responses, or distractors.
-   A **multiple-response** question has two or more correct responses out of five or more options.

On the exam, there is no penalty for guessing. Any questions that you do not answer are scored as incorrect. If you are not sure of what the correct answer is, it’s always best for you to guess instead of leaving any questions unanswered.

The exam enables you to flag any questions that you’d like to review before submitting the exam. This helps you to use your time during the exam efficiently, knowing that you can always go back and review any questions that you were initially unsure of.

**Whitepapers and resources**

As part of your preparation for the AWS Certified Cloud Practitioner exam, we recommend that you review the following whitepapers and resources:

-   [Overview of Amazon Web Services](https://d1.awsstatic.com/whitepapers/aws-overview.pdf)
-   [How AWS Pricing Works](http://d1.awsstatic.com/whitepapers/aws_pricing_overview.pdf)
-   [Compare AWS Support Plans](https://aws.amazon.com/premiumsupport/plans/)

### Exam Strategies

**Read the full question**
- First, make sure that you read each question in full. Key words or phrases in the question that, if left unread, could result in you selecting an incorrect response option.

**Predict the answer before reviewing the response options**
- Next, try to predict the correct answer before looking at any of the response options.   This strategy helps you to draw directly from your knowledge and skills without distraction from incorrect response options. If your prediction turns out to be one of the response options, this can be helpful for knowing whether you’re on the right track. However, make sure that you review all the other response options for that question.

**Eliminate incorrect response options**
- Before selecting your response to a question, eliminate any options that you believe to be incorrect.  This strategy helps you to focus on the correct option (or options, for multiple-response questions) and ensure that you have fulfilled all the requirements of the question.

### Sample questions

The following two questions help you become familiar with the differences between multiple-choice and multiple-response questions.

AWS Certified Cloud Practitioner exam results are reported as a score from 100–1,000. What is the minimum passing score?
- [ ] 650
- [x] 700
- [ ] 850
- [ ] 900

Which domains are included on the AWS Certified Cloud Practitioner exam? (Select TWO.)
_**Strategy:** Think back to the exam domains that were reviewed earlier in this module. Based on the domains that you recall learning about, which response options do you think that you can eliminate as incorrect?_
- [ ] Security and Compliance
- [ ] Automation and Optimization
- [ ] Monitoring and Reporting
- [ ] Billing and Pricing
- [ ] Deployment and Provisioning

**Additional sample questions in the PDF link:**
[https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Sample-Questions.pdf](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Sample-Questions.pdf)

### Final Assessment
**Which statement best describes Amazon GuardDuty?**
- [x] A service that provides intelligent threat detection for your AWS infrastructure and resources
- [ ] A service that lets you monitor network requests that come into your web applications
- [ ] A service that checks applications for security vulnerabilities and deviations from security best practices
- [ ] A service that helps protect your applications against distributed denial-of-service (DDoS) attacks

**You want to store data in a key-value database. Which service should you use?**
- [ ] Amazon DocumentDB
- [x] Amazon DynamoDB
- [ ] Amazon RDS
- [ ] Amazon Aurora

**Which tool enables you to visualize, understand, and manage your AWS costs and usage over time?**
- [ ] AWS Artifact
- [ ] AWS Budgets
- [x] AWS Cost Explorer
- [ ] AWS Pricing Calculator

**Which action can you perform in Amazon CloudFront?**
- [ ] Run infrastructure in a hybrid cloud approach.
- [x] Deliver content to customers through a global network of edge locations.
- [ ] Provision resources by using programming languages or a text file.
- [ ] Provision an isolated section of the AWS Cloud to launch resources in a virtual network that you define.

**Which service is used to transfer up to 100 PB of data to AWS?**
- [x] AWS Snowmobile
- [ ] AWS DeepRacer
- [ ] Amazon Neptune
- [ ] Amazon CloudFront

**Which service enables you to review details for user activities and API calls that have occurred within your AWS environment?**
- [x] AWS CloudTrail
- [ ] Amazon Inspector
- [ ] Amazon CloudWatch
- [ ] AWS Trusted Advisor

**Which statement best describes Elastic Load Balancing?**
- [ ] A service that monitors your applications and automatically adds or removes capacity from your resource groups in response to changing demand
- [ ] A service that provides data that you can use to monitor your applications, optimize resource utilization, and respond to system-wide performance changes
- [x] A service that enables you to set up, manage, and scale a distributed in-memory or cache environment in the cloud

**Which service enables you to consolidate and manage multiple AWS accounts from a central location?**
- [ ] AWS Key Management Service (AWS KMS)
- [ ] AWS Identity and Access Management (IAM)
- [x] AWS Organizations
- [ ] AWS Artifact

**Which migration strategy involves changing how an application is architected and developed, typically by using cloud-native features?**
- [x] Refactoring
- [ ] Rehosting
- [ ] Replatforming
- [ ] Repurchasing

**Which AWS Trusted Advisor category includes checks for your service limits and overutilized instances?**
- [ ] Fault Tolerance
- [ ] Security
- [x] Performance
- [ ] Cost Optimization

**Which virtual private cloud (VPC) component controls inbound and outbound traffic for Amazon EC2 instances?**
- [ ] Subnet
- [x] Security group
- [ ] Internet gateway
- [ ] Network access control list
> A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.  [Control traffic to resources using security groups - Amazon Virtual Private Cloud](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)

**Which pillar of the AWS Well-Architected Framework focuses on using computing resources in ways that meet system requirements?**
- [x] Performance Efficiency
- [ ] Operational Excellence
- [ ] Reliability
- [ ] Security
> The Performance Efficiency pillar focuses on using computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.  [https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf)

**Which statement best describes AWS Marketplace?**
- [x] A digital catalog that includes thousands of software listings from independent software vendors
- [ ] A resource that provides guidance, architectural reviews, and ongoing communication with your company as you plan, deploy, and optimize your applications
- [ ] A resource that can answer questions about best practices and assist with troubleshooting issues
- [ ] An online tool that inspects your AWS environment and provides real-time guidance in accordance with AWS best practices
> You can use AWS Marketplace to find, test, and buy software that runs on AWS.
> [AWS Marketplace: Homepage](https://aws.amazon.com/marketplace) 

14. **Which Support plans include access to all AWS Trusted Advisor checks? (Select TWO.)**
- [ ] Basic
- [ ] AWS Free Tier
- [x] Business
- [x] Enterprise
- [ ] Developer
> [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

15. **You are running an Amazon EC2 instance and want to store data in an attached resource. Your data is temporary and will not be kept long term. Which resource should you use?**
- [ ] Amazon Elastic Block Store (Amazon EBS) volume
- [ ] Amazon S3 bucket
- [ ] Instance store
- [ ] Subnet
>**Learn more: [Amazon EC2 instance store - Amazon Elastic Compute Cloud](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)

16. **Which component or service enables you to establish a dedicated private connection between your data center and virtual private cloud (VPC)?**
- [ ] Internet gateway
- [ ] Amazon CloudFront
- [ ] Virtual private gateway
- [x] AWS Direct Connect
> **Learn more:**   [AWS Direct Connect](https://aws.amazon.com/directconnect)

17. **Which statement is TRUE for AWS Lambda?**
- [ ] Before using AWS Lambda, you must prepay for your estimated compute time.
- [ ] The first step in using AWS Lambda is provisioning a server.
- [x] You pay only for compute time while your code is running.
- [ ] To use AWS Lambda, you must configure the servers that run your code.
> **Learn more:** [AWS Lambda](https://aws.amazon.com/lambda)

18. **Which actions can you perform in Amazon Route 53? (Select TWO.)**
- [ ] Access AWS security and compliance reports and select online agreements.
- [ ] Connect user requests to infrastructure in AWS and outside of AWS.
- [ ] Automate the deployment of workloads into your AWS environment.
- [ ]  Monitor your applications and respond to system-wide performance changes.
- [ ] Manage DNS records for domain names.
> **Learn more:** [Amazon Route 53](https://aws.amazon.com/route53)

19. **Which compute option reduces costs when you commit to a consistent amount of compute usage for a 1-year or 3-year term?**
- [x] Savings Plans
- [ ] Reserved Instances
- [ ] Spot Instances
- [ ] Dedicated Hosts
> **Learn more:** [Savings Plans](https://aws.amazon.com/savingsplans/)

20. **You want to store data in a volume that is attached to an Amazon EC2 instance. Which service should you use?**
- [ ] AWS Lambda
- [ ] Amazon Simple Storage Service (Amazon S3)
- [x] Amazon Elastic Block Store (Amazon EBS)
- [ ] Amazon ElastiCache
> **Learn more:**  [Amazon EBS](https://aws.amazon.com/ebs)

21. **Which service is used to run containerized applications on AWS?**
- [ ] Amazon Redshift
- [x] Amazon Elastic Kubernetes Service (Amazon EKS)
- [ ] Amazon SageMaker
- [ ] Amazon Aurora
> **Learn more:**  [Amazon EKS](https://aws.amazon.com/eks)

22. **Which Perspective of the AWS Cloud Adoption Framework focuses on recovering IT workloads to meet the requirements of your business stakeholders?**
- [ ] Business Perspective
- [ ] Governance Perspective
- [x] Operations Perspective
- [ ] People Perspective
> **Learn more:**  [Whitepaper: An Overview of the AWS Cloud Adoption Framework](https://d1.awsstatic.com/whitepapers/aws_cloud_adoption_framework.pdf)

23. **Which service is used to quickly deploy and scale applications on AWS?**
- [ ] AWS Snowball
- [x] AWS Elastic Beanstalk
- [ ] Amazon CloudFront
- [ ] AWS Outposts
> **Learn more:**  [AWS Quick Starts](https://aws.amazon.com/quickstart)

24. **Which tool is used to automate actions for AWS services and applications through scripts?**
- [ ] AWS Snowball
- [ ] Amazon Redshift
- [ ] Amazon QLDB
- [x] AWS Command Line Interface
> **Learn more:**  [AWS Command Line Interface](https://aws.amazon.com/cli/)

25. **Which statement best describes an Availability Zone?**
- [ ] The server from which Amazon CloudFront gets your files
- [ ] A site that Amazon CloudFront uses to cache copies of content for faster delivery to users at any location
- [ ] A separate geographical location with multiple locations that are isolated from each other
- [x] A fully isolated portion of the AWS global infrastructure
> **Learn more:**  [AWS global infrastructure](https://aws.amazon.com/about-aws/global-infrastructure)  [Regions and Availability Zones](https://aws.amazon.com/about-aws/global-infrastructure/regions_az/)

26. **Which tasks are the responsibilities of AWS? (Select TWO.)**
- [ ] Training company employees on how to use AWS services
- [ ] Configuring security groups on Amazon EC2 instances
- [x] Configuring AWS infrastructure devices
- [x] Maintaining virtualization infrastructure
- [ ] Creating IAM users and groups
> **Learn more:**  [AWS shared responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/)

27. **You want to send and receive messages between distributed application components. Which service should you use?**
- [ ] AWS Snowball
- [ ] Amazon Route 53
- [x] Amazon Simple Queue Service (Amazon SQS)
- [ ] Amazon ElastiCache
> **Learn more:**  [Amazon SQS](https://aws.amazon.com/sqs)

28. **You want Amazon S3 to monitor your objects’ access patterns. Which storage class should you use?**
- [ ] S3 One Zone-IA
- [x] S3 Intelligent-Tiering
- [ ] S3 Standard-IA
- [ ] S3 Glacier
> **Learn more:**  [Amazon S3 storage classes](https://aws.amazon.com/s3/storage-classes/)

29. **In the S3 Intelligent-Tiering storage class, Amazon S3 moves objects between a frequent access tier and an infrequent access tier. Which storage classes are used for these tiers? (Select TWO.)**
- [ ] S3 Glacier
- [x] S3 Standard-IA
- [x] S3 Standard
- [ ] S3 Glacier Deep Archive
- [ ] S3 One Zone-IA
> **Learn more:**  [Amazon S3 storage classes](https://aws.amazon.com/s3/storage-classes/)

30. **Which service enables you to build the workflows that are required for human review of machine learning predictions?**
- [ ] Amazon Textract
- [x] Amazon Augmented AI
- [ ] Amazon Aurora
- [ ] Amazon Lex
> **Learn more:**  [Amazon Augmented AI](https://aws.amazon.com/augmented-ai)
