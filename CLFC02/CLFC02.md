Question Set: https://www.examtopics.com/exams/amazon/aws-certified-cloud-practitioner/view/6/

++++

##### Amazon Machine Images (AMIs)

An AMI is a pre-configured virtual machine image that contains the operating system, application software, and any other required components needed to launch an instance. AMIs can be used to create new instances in the same or a different region, which can be useful for disaster recovery purposes.

##### AWS Data Pipeline

a web service that helps you reliably process and move data between different AWS compute and storage services

##### AWS Service Catalog

allows organizations to create and manage catalogs of IT services that are approved for use on AWS.

##### AWS  PrivateLink

provides direct secure connections **from VPCs to other AWS services.**

##### Amazon Macie

A data security service that **uses machine learning** (ML) and pattern matching to discover and help protect your sensitive data.

##### AWS IAM Access Analyzer

helps you identify the resources in your organization and accounts, such as Amazon S3 buckets or IAM roles, shared with an **external entity**. To **identify unintended access** to your resources and data, which is a security risk.. 

##### AWS Transit Gateway

Connect VPCs and on-promises networks through a central hub. 

##### QuickSight

supports the creation of visual reports from AWS Cost and Usage Report data

##### AWS Infrastructure Event Management (IEM)

 offers architecture and scaling guidance and operational support during the preparation and execution of planned events

##### Amazon S3 Lifecycle rules

a set of rules that you can create to automate the transition of objects between different storage classes or deletion when objects are no longer needed. This can help you to save money on storage costs and to manage your data more effectively.

##### S3 Versioning

keeping multiple variants of an object in the same bucket, can be used to preserve, retrieve, and restore every version. 

##### AppStream 2.0

a fully managed application streaming service that **provides users instant access to their desktop applications** from anywhere. (e.g. A company wants to use the AWS Cloud to provide secure access to desktop applications that are running in a fully managed environment.)

##### AWS Global Accelerator

uses **edge locations** to improve the availability and performance of applications by routing traffic through the AWS global network infrastructure to the nearest edge location. This helps reduce latency and improve application responsiveness for users around the world. 



















# Difference

##### AWS Infrastructure Event Management (IEM) v.s. The designated AWS technical account manager (TAM)

##### CloudWatch v.s. CloudTrail







+++++

# ???

![image-20231117003732307](CLFC02.assets/image-20231117003732307.png)

![image-20231117110939698](CLFC02.assets/image-20231117110939698.png)

+++

# Compute in the Cloud

### **Amazon Elastic Compute Cloud (Amazon EC2)**

[EC2]: https://aws.amazon.com/ec2/

Secure and resizable compute capacity for virtually any workload

### Amazon EC2 Instance Types

- **General purpose instances**
  -  a balance of compute, memory, and networking resources
- **Compute optimized instances**
  -  for compute-bound applications that benefit from high-performance **processors**
  - e.g. web, application, and gaming servers
- **Memory optimized instances**
  - fast performance for workloads that process large datasets in memory
- **Accelerated computing instances**
  - use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs
- **Storage optimized instances**
  - for workloads that require high, sequential read and write access to large datasets on local storage
  - e.g. distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems

### EC2 Pricing

|                                  |                                                              |
| -------------------------------- | ------------------------------------------------------------ |
| On-Demand                        | - No upfront costs or minimum contracts apply. - For short-term, irregular workloads that cannot be interrupted. - **Less than 1 year** |
| **Reserved Instances**           | a billing discount applied to the use of On-Demand Instances. - a commitment of either **1 year or 3 years** |
| - Standard Reserved Instances    | - If knowing the choice of instance type & size & AWS Region |
| - Convertible Reserved Instances | - If runs in different Zones / instance types                |
| EC2 Instance Saving Plans        | - when you make an hourly spend commitment to an instance family and Region for a **1-year or 3-year term**. -  if you need flexibility in your Amazon EC2 usage over the duration of the commitment term - save of up to 72% over On-Demand costs |
| Spot Instance                    | - ideal for workloads with **flexible start and end times**, or can **withstand interruptions**. - processing job that can start and stop as needed without affecting overall operations |
| Dedicated Hosts                  | -  physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. |



### Scalability

beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in

#### Amazon EC2 Auto Scaling

automatically add or remove Amazon EC2 instances

- Approaches: dynamic scaling, predictive scaling



### Elastic Load Balancing



### Messaging and Queuing

#### **monolithic application**

made of multiple components which communicate with each other.  If a single component fails, other components fail. 

#### Microservices approacd

application components are loosely coupled, prevents the entire application from failing. 

if a single component fails, the other components continue to work. 

#### **Amazon Simple Notification Service (Amazon SNS)**

 a publish/subscribe service, subscribers can be web servers, email addresses, AWS Lambda functions, or several other options

#### **Amazon Simple Queue Service (Amazon SQS)**

a message queuing service, Fully managed message queuing for microservices, distributed systems, and serverless applications

send, store, and receive messages between software components **at any volume**

##### SQS v.s. Pipeline

**SQS**:  between software components **at any volume**

**Pipeline**: reliably process and move data between different AWS compute and storage services



### Additional Compute Services

#### **Serverless computing**

do not need to provision or manage these servers

##### **AWS Lambda**

is a service for serverless computing. 

Automatically respond to code execution requests at any scale.  

Run code without provisioning or managing infrastructure

(So: maximizes operational efficiency and minimizes the cost of running the application)

#### **Containers**

a standard way to package your application's code and dependencies into a single object

#### **Amazon Elastic Container Service (Amazon ECS)**

a highly scalable, high-performance **container management system** that enables you to **run and scale** containerized applications on AWS

supports Docker containers

#### **Amazon Elastic Kubernetes Service (Amazon EKS)**

a fully managed service that you can use to run Kubernetes on AWS

enables you to deploy and manage containerized applications at scale

#### **AWS Fargate**

a **serverless compute engine** for containers







# Global Infrastructure and Reliability

### Global Infrastructure

#### Region

A separate geographical location with multiple locations that are isolated from each other.

##### Select a region

- Compliance with data governance and legal requirements
- Proximity to your customers
- Available services within a region
- Pricing

#### Availability Zone

is a single data center or a group of data centers within a **Region**

is made up of one or more discrete data centers that have redundant power, networking, and connectivity

##### Region v.s. Zone

A Region consists of three or more Availability Zones.

#### VPC | Zone | Region 

- a VPC belongs to a region, a region can have multiple VPCs 
- a VPC spans all availability zones

#### Amazon CloudFront

A **content delivery network (CDN) service** built for high performance, security, and developer convenience.



### Edge Locations

is a site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.

### Provision AWS services

##### **AWS Management Console**

a web-based interface for accessing and managing AWS services

##### **AWS Command Line Interface (AWS CLI)**

control multiple AWS services directly from the command line within one tool

##### Software Development Kits (SDKs)

make it easier for you to use AWS services through an API designed for your programming language or platform, enable you to use AWS services with your existing applications or create entirely new applications that will run on AWS.

#### **AWS Elastic Beanstalk**

Deploying the resources according to the configuration settings provided by users, to perform: 

- Adjust capacity
- Load balancing
- Automatic scaling
- Application health monitoring

#### **AWS CloudFormation**

Treat your **infrastructure as code**. 

To build an environment by writing lines of code instead of using the AWS Management Console to individually provision resources.

It provisions your resources in a safe, repeatable manner, enabling you to frequently build your infrastructure and applications

#### AWS Outposts

Extend AWS infrastructure and services to different locations, including your on-premises data center.











# Networking

### **Amazon Virtual Private Cloud (Amazon VPC)**

A networking service for establishing boundaries around your AWS resources

enables you to provision an isolated section of the AWS Cloud, where resources can be launched in a virtual network you defined, or organize resources into subnets

#### Internet gateway

being attached to the VPC, is a connection **between a VPC and the internet**. 

#### Virtual private gateway

establish a **virtual private network (VPN) connection** **between your VPC and a private network**,

#### AWS Direct Connect

establish a **dedicated private** connection **between your data center and a VPC**.  / between on premise and AWS

##### AWS Direct Connect v.s. AWS PrivateLink

- Direct connect is for private dedicated connection **between on premise and AWS**, <u>***not** between **workloads** (applications and services)*</u>

- PrivateLink provides direct secure connections **from VPCs to other AWS services**.

##### Workloads

an application, service, capability, or a specified amount of work that consumes cloud-based resources

##### Customer gateway

is the customer side of a VPN connection, is one of the components of an AWS Site-to-Site VPN connection

##### VPC Peering

A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them



### Subnets

is **a section of VPC** that can contain resources that being grouped 

#### Network Access Control list (ACL)

a **virtual firewall** that controls inbound and outbound traffic **at the subnet level**.

is a **Stateless packet filtering**, which remember nothing 

They process rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic.

#### Security Group

a **virtual firewall** that controls inbound and outbound traffic **for an Amazon EC2 instance**.

By default, a security group denies all inbound traffic and allows all outbound traffic.  

is a **Stateful packet filtering**, remember previous decisions made for incoming packets



### Global Network

#### Domain Name System (DNS)

Translating a domain name to an IP address

#### **Amazon Route 53**

is **a DNS web service**, route end users to internet applications hosted in AWS, can route users to infrastructure outside of AWS.







# Security

### AWS Shared Responsibility Model

![sharedResponsibilityModel](CLFC02.assets/sharedResponsibilityModel.png)

Customers are responsible for the security of everything that they create and put *in* the AWS Cloud.

AWS is responsible for security *of* the cloud. AWS operates, manages, and controls the components at all layers of infrastructure. 

##### Shared controls: 

- Patch Management - in the infrastructure; in guest OS and applications
- Configuration Management - infrastructure devices; guest OS, database, applications
- Awareness & Training - each one's employee



### AWS IAM

**AWS Identity and Access Management (IAM)**

- enables you to **manage** access to AWS services and resources securely
- You can apply IAM policies to IAM users, groups, or roles. You cannot apply an IAM policy to the AWS account root user.

#### **AWS account root user**

has complete access to all the AWS services and resources in the account

- Follow the security principle of **least privilege** when granting permissions: prevent users or roles from having more permissions than needed to perform their tasks.

#### **IAM users**

consists of a name and credentials

#### **IAM policies**

a document that allows or denies permissions to AWS services and resources

#### **IAM groups**

a collection of IAM users, all users in the group are granted permissions specified by the policy.

#### **IAM roles**

An IAM role is an identity that you can assume to gain temporary access to permissions.  

#### **Multi-factor authentication**

provides an extra layer of security for your AWS account



### **AWS Organizations**

consolidate and manage multiple AWS accounts within a central location, centrally control permissions for the accounts in your organization by using **SCPs (service control policies)**

- centrally manage and govern its AWS Cloud environment
- automate the creation of AWS accounts
- simplify billing processes, consolidated billing capabilities

#### SCPs

Can be applied to control policies (SCPs) to the organization root, an individual member account, or an OU. 

Can **restrict the use of specific AWS services** or to impose additional conditions or requirements on the use of those services. / enable you to **place restrictions on the AWS services**

#### **Organizational units**

group accounts into organizational units (OUs) to make it easier to manage accounts with similar business or security requirements



### Compliance

#### **AWS Artifact**

is a service that provides on-demand access to AWS security and compliance reports and select online agreements

- consists of two main sections: AWS Artifact Agreements and AWS Artifact Reports
- provide document: AWS ISO certifications

#### **Customer Compliance Center**

 read customer compliance stories



### Denial-of-Service Attacks

is a deliberate attempt to make a website or application unavailable to users.

#### **AWS Shield**

a service that automatically detect and mitigate **sophisticated** **network-level** **distributed** DDoS events

- provides two levels of protection: Standard and Advanced
  - automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frequently occurring types of DDoS attacks. 
  - a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. 



### Additional Security Services

#### **AWS Key Management Service (AWS KMS)**

enables you to perform **encryption** operations through the use of **cryptographic keys**

#### **AWS WAF**

**Web Application Firewall** that lets you **monitor network requests** that come into your **web applications**. 

works in a similar way to block or allow traffic. However, it does this **by using a web access control list (ACL)**

#### **Amazon Inspector**

helps to improve the security and compliance of applications by running automated security assessments

It checks applications for **security vulnerabilities** and deviations from security best practices

#### **Amazon GuardDuty**

a service that provides **intelligent threat detection** for your AWS infrastructure and resources. 

It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.











# Monitoring and Analytics

### Amazon CloudWatch

Observe and monitor resources and applications on AWS, on premises, and on other clouds.

Includes performance changes, **resource use**, operational health. 

enables you to monitor and manage various **metrics** and **configure alarm** actions based on data from those metrics

#### metrics

represent the data points for your resources. 

AWS services send metrics to CloudWatch -> CloudWatch uses these metrics to **create graphs automatically** that show how performance has changed over time.

#### **CloudWatch alarms**

automatically perform actions if the value of your metric has gone above or below a predefined threshold

#### **CloudWatch dashboard**

access all the metrics for your resources from a single location



### AWS CloudTrail

Track **user activity** and **API usage**, records API calls for your account, includes the identity of the API caller, the time of the API call, the source IP address of the API caller, and more, like a log of actions. 

can determine whether a change was made to the security groups of an EC2 instance in the last month

#### CloudTrail Insights

automatically detect unusual API activities in your AWS account.



### AWS Trusted Advisor

a web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices

in five categories: cost optimization, performance, security (like Amazon S3 buckets), fault tolerance, and service limits

For each category: Green check - no problems; Orange triangle - investigations; Red circle - recommended actions. 



# Pricing and Support

### AWS Free Tier

A program allow customers to use AWS services without costs. using certain services without having to worry about incurring costs for the specified period

- Always Free: like AWS Lambda requests, Amazon DynamoDB strorage
- 12 Months Free: offered to new AWS customers
- Trials: from the date you activate a particular service, like Amazon Inspector

#### **How AWS pricing works**

#### AWS Pricing Calculator

explore AWS services and **create an estimate** for the cost of your use cases on AWS

### Billing Dashboard

to pay your AWS bill, monitor your usage, and analyze and control your costs.

### Consolidated Billing

is a feature of AWS Organizations

enables you to receive a single bill for all AWS accounts in your organization, with reviewing itemized charges incurred by each account. 

share bulk discount pricing, Savings Plans, and Reserved Instances across the accounts in your organization

### AWS Budgets  

create budgets to plan your service usage, service costs, and instance reservations. 

set custom **alerts** when your usage exceeds (or is forecasted to exceed) the budgeted amount.

### **AWS Cost Explorer**

is a tool that lets you **visualize**, understand, and manage your AWS costs and usage over time.

includes a default report of the costs and usage for your top five cost-accruing AWS services



### **AWS Support**

Basic Support: free for all, includes access to whitepapers, documentation, and support communities

The followings include all the benefits of Basic Support: 

|                       |                                                              |
| --------------------- | ------------------------------------------------------------ |
| **Developer Support** | Best practice guidance; Client-side diagnostic tools;Building-block architecture support (guidance for how to use AWS offerings, features, and services together) |
| **Business Support**  | Use-case guidance to identify AWS offerings, features, and services; All **AWS Trusted Advisor checks**; Limited support for third-party software, such as common operating systems and application stack components |

**AWS Enterprise On-Ramp Support**: includes all features above, and:

- A pool of **TAM** to provide proactive guidance and coordinate access to programs and AWS experts
- A Cost Optimization workshop (one per year)
- A Concierge support team for billing and account assistance
- Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard

**Enterprise Support**: includes all features above, and:

- A designated **TAM** to provide proactive guidance and coordinate access
- A Concierge support team for billing and account assistance
- Operations Reviews and tools to monitor health
- Training and Game Days to drive innovation
- Tools to monitor costs and performance through Trusted Advisor and Health API/Dashboard

also provides full access to proactive services

#### **Technical Account Manager (TAM)**

primary point of contact at AWS. TAM educates, empowers, and evolves your cloud journey across the full range of AWS **services**. 

![image-20231117190422495](CLFC02.assets/image-20231117190422495.png)



### Marketplace

a digital catalog that includes thousands of software listings from independent software vendors, allows you to find, test, and buy software that runs on AWS. 

has several categories, such as Infrastructure Software, DevOps, Data Products, Professional Services, Business Applications, Machine Learning, Industries, and Internet of Things (IoT).







# Migration and Innovation

### AWS CAF

#### **Six core perspectives of the Cloud Adoption Framework** - **Perspectives**

- business capabilities: **Business**, **People**, and **Governance**
- technical capabilities: **Platform**, **Security**, and **Operations**



### Migration Strategies

- Rehosting - “lift-and-shift”, moving applications without changes
- Replatforming - “lift, tinker, and shift,”, making a few cloud optimizations to realize a tangible benefit, without changing the core architecture
- Refactoring/re-architecting - reimagining how an application is architected and developed by using cloud-native featurez
- Repurchasing - moving from a traditional license to a software-as-a-service model
- Retaining -  keeping applications that are critical for the business in the source environment
- Retiring - removing applications that are no longer needed.



### AWS Snow Family

a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS

Composed of:

- **AWS Snowcone** - 14TB, small, rugged, and secure edge computing and data transfer device
- **AWS Snowball** - 80TB
  - **Snowball Edge Storage Optimized** - large-scale data migrations and recurring transfer workflows
  - **Snowball Edge Compute Optimized** - provides powerful computing resources 
- **AWS Snowmobile**. - 100 petabytes, an exabyte-scale data transfer service used to move large amounts of data to AWS



### Innovation

- **Serverless applications**
  - AWS Lambda
- **Artificial intelligence**
- **Machine learning**
  - Amazon SageMaker

#### **Amazon Lex**

can quickly build, test, and deploy conversational chatbots to use in your applications.





# The Cloud Journey

### **The AWS Well-Architected Framework**

helps you understand how to design and operate reliable, secure, efficient, and cost-effective systems in the AWS Cloud, provides a way for you to consistently measure your architecture

- **Operational excellence**: he ability to **support development and run** workloads effectively
- **Security**: 
- **Reliability**: Recover, dynamically acquire resources, mitigate disruptions
- **Performance efficiency**: **use computing resources** efficiently
- **Cost optimization**: adopting a consumption model, analyzing and attributing expenditure, and using managed services
- **Sustainability**: by reducing energy consumption and increasing efficiency

### **Advantages of cloud computing**

- Trade upfront expense for variable expense: pay only when you consume computing resources.
- Benefit from massive economies of scale: achieve a lower variable cost than you can get on your own
- Stop guessing capacity.
- Increase speed and agility.
- Stop spending money running and maintaining data centers.
- Go global in minutes.























