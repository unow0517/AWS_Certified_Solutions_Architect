# AWS_Certified_Solutions_Architect - Associate

## What To Do Here
- preparing AWS Solutions Architect Certification.
- Take note important concepts.

## Prior Experience
- I built an app and ran it on AWS when I was studying in 42 Heilbronn.
- Short experience with EC2, route53, S3
- I took [Udemy Course](https://www.udemy.com/share/106WtA3@PZipmHbtGDd8yMYGf167glVsvIQmBIpirjpuo_ByMCr8DYGtfkcrzeIpy59J85DpWQ==/), but couldn't reach the end.

## How To Start
- Start with dump question to learn neccessary concepts

## Website 
https://www.examtopics.com/ : website which offers dump question for the certification.  

## Key Concepts
**S3 Transfer Acceleration**
  1. This feature utilizes Amazon CloudFront's globally distributed edge locations to speed up uploads to S3.
  2. It significantly reduces the time it takes to upload large volumes of data from geographic locations.
<br>

**CloudFront**
  1. Amazon CloudFront is a globally distributed Content Delivery Network (CDN) service that accelerates the delivery of data, videos, applications, and APIs to users. It works by caching copies of content at edge locations around the world, allowing users to access data from the nearest geographical location, thereby reducing latency.
<br>

**S3 Cross-Region Replication**
  1. feature that automatically replicates data stored in one Amazon S3 bucket to another S3 bucket in a different AWS region. This replication helps enhance data durability, availability, and compliance by ensuring that data is stored across multiple geographic locations.
<br>

**AWS Snowball Edge Storage Optimized**
  1. a highly versatile, portable storage and compute device used for transferring large amounts of data in and out of AWS. Designed to handle petabyte-scale data transfers.
  2. Provides up to 80 TB of usable storage capacity.
<br>

**Amazon Elastic Block Store (EBS)**
  1. a high-performance block storage service designed for use with Amazon EC2 (Elastic Compute Cloud).
  2. It provides scalable storage volumes that can be attached to EC2 instances, enabling low-latency access to data for applications such as databases, file systems, and enterprise applications.
<br>

**AWS Edge Locations**
  1. data centers located in various geographical regions around the world, primarily used for delivering content via Amazon CloudFront, AWS's Content Delivery Network (CDN).
  2. These locations are strategically placed to provide low-latency access to applications, ensuring faster data transfer and improved user experience.
<br>

**On Demand**
  1. only when user needs
  2. paying what you use
<br>

**Amazon Red Shift**
  1. a fully managed, petabyte-scale data warehouse service in the cloud.
  2. It allows users to run complex queries and analyze large amounts of data quickly.
  3. Redshift is optimized for high-performance analysis of structured and semi-structured data, making it a key component for data analytics and business intelligence solutions.
<br>

**CloudWatch**
  1. a monitoring and management service designed for AWS resources and applications.
  2. It provides real-time insights into resource utilization, operational performance, and overall application health, enabling proactive maintenance and optimization.
<br>

**Amazone Athena**
  1. Amazon Athena is an interactive query service that allows users to analyze data directly in Amazon **S3 using standard SQL** without the need to set up complex data warehouses or transformation processes.
<br>

**AWS Glue**
  1. AWS Glue is a fully managed extract, transform, and load (ETL) service designed for preparing and loading data for analytics.
  2. It makes it easy to discover, catalog, and transform data from various sources, allowing users to build data workflows in a scalable and serverless manner.
<br>

**PrincipalOrgID**
  1. an attribute used in AWS Identity and Access Management (IAM) policies, particularly in organizations that leverage AWS Organizations.
  2. This attribute is utilized to manage permissions effectively across multiple AWS accounts within an organization.
<br>

**AWS Organizations**
  1. a service that enables you to manage multiple AWS accounts centrally.
  2. It allows you to create and manage an organization with multiple AWS accounts while applying policies and controlling access to resources.
  3. This helps organizations streamline their operations and manage billing and governance across accounts.
<br>

**Principal in AWS Context**<br>
In the context of Amazon Web Services (AWS) IAM (Identity and Access Management), a principal refers to an entity that can perform actions on AWS resources. This entity can be:
1. Users: Individual IAM users within your AWS account.
2. Roles: IAM roles that can be assumed by users or services.
3. Services: AWS services like EC2, Lambda, or S3 that can interact with other AWS resources.
4. Federated Users: Users authenticated through third-party identity providers.
<br>

**Organizational Units (OUs)**
  1. enabling you to group AWS accounts in a hierarchical manner for better management, governance, and policy application.
  2. Production OU, Testing OU...
<br>

**VPC (Virtual Private Cloud)**
  1. allows you to create a private network within Amazon's cloud where you can launch AWS resources in a logically isolated environment.
<br>

**Gateway**
  1. critical components that facilitate communication between different networks.
<br>

**Gateway VPC  Endpoint**
  1. allow VPC to access AWS services, like S3 or Dynamo DB
<br>

**Instance Profile**
  1. a container for an IAM role that you can use to grant Amazon EC2 instances permissions to interact with other AWS services.
  2. EC2 shoud have instance Profile, not role.
<br>

**IAM (Identity and Access Management)**
  1.  helps you control access to your AWS resources.
  2.  With IAM, you can create and manage AWS users and groups, and use permissions to allow or deny their access to AWS resources, ensuring only authorized users can perform actions.
<br>

**IAM Role**
  1. an IAM identity that you can create in your AWS account.
  2. WebserverRole, S3AccessRole...
<br>

**Endpoint**
  1. refers to a specific URL or network address where requests are sent to access AWS services.
<br>

**NAT(Network Address Translation) Device**
  1. allows instances in a private subnet to access the internet while preventing the internet from initiating connections to those instances.
<br>

**EBS (Elastic Volumn Store)**
   1. persistent block storage service designed for use with Amazon EC2 instances.
   2. It provides highly available and durable storage that can be easily attached to instances, making it suitable for a wide range of applications.
   3. WHy EBS over S3? S3 is for the access through internet. EBS is mainly for EC2.
<br>

**EFS (Elastic File System)**
  1. a scalable, fully managed file storage service designed to be used with Amazon Web Services (AWS) cloud computing.
  2. It provides a simple, serverless, and elastic file storage solution that can grow and shrink automatically as files are added or removed.
  3. Implement Amazon EFS as shared storage for all EC2 instances behind the ALB. This ensures high availability, scalability, and consistent data access across Availability Zones with minimal operational overhead.
<br>

**AZ (Availability Zone)**
  1. isolated locations within an AWS region designed to protect applications from failures in other zones.
  2. Each region comprises multiple AZs, which are designed to be independent in terms of power, networking, and connectivity.
<br>

**NFS (Network File System)**
  1. a distributed file system protocol that allows users to access files over a network as if they were on a local disk.
  2. Primarily used in UNIX/Linux environments, NFS enables file sharing among multiple machines seamlessly.
<br>

**On-Premise**
  1. IT infrastructure and data that are housed within an organization's physical location.
  2. Unlike cloud services that operate over the internet, on-premise solutions require businesses to buy, install, and manage all hardware and software internally.
<br>

**Snowball Edge**
  1. a data transfer and edge computing device provided by Amazon Web Services (AWS).
  2. It is designed to help organizations efficiently move large amounts of data into and out of AWS, often in situations where internet bandwidth is limited or non-existent.
  3. Physical Device that user get it delievered.
<br>

**Edge Computing**
  1. refers to the practice of processing and analyzing data closer to the source of data generation rather than relying solely on centralized cloud data centers.
  2. This approach minimizes latency, reduces bandwidth use, and enhances real-time data processing capabilities.
<br>

**AWS Direct Connect**
  1. a network service that enables users to establish a dedicated, high-bandwidth, low-latency connection between their on-premises infrastructure and Amazon Web Services (AWS).
  2. This service provides a more reliable and consistent network experience compared to internet-based connections.
<br>

**Amazon Kinesis Data Analytics**
  1. is a fully managed service that allows you to process and analyze streaming data in real-time.
  2. It enables users to easily ingest, process, and analyze data streams using standard SQL, opening up opportunities for interactive dashboards and real-time analytics.
<br>

**Amazon Simple Notification Service**
  1. a fully managed messaging service designed to facilitate the sending of notifications and messages between distributed systems and applications.
  2. It enables users to send messages to a variety of endpoints, such as mobile devices, email addresses, and other applications seamlessly and effectively.
<br>

**Amazon Simple Queue Service (Amazon SOS)**
  1. is a fully managed message queuing service that enables applications to communicate and coordinate through message-based workflows.
  2. SQS allows decoupling of components in distributed systems, which enhances scalability and reliability.
<br>

**Decoupling**
  1.refers to the architectural design principle of separating components of a system to minimize dependencies between them. 
  2.In the context of application architecture  
<br>
