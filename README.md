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
  1. S3 Transfer Acceleration is a feature that speeds up the upload and download of objects to and from Amazon S3 by providing a network of edge locations. 
  2. It significantly reduces the time it takes to upload large volumes of data from geographic locations.

<br>

**CloudFront**
  1. Amazon CloudFront is a globally distributed Content Delivery Network (CDN) service that accelerates the delivery of data, videos, applications, and APIs to users. It works by caching copies of content at edge locations around the world, allowing users to access data from the nearest geographical location, thereby reducing latency.
  2. Performance, Cost-efficiency
  3. Web-site acceleration, video streaming, data security.
<br>

**Global Accelerator**
  1. is a networking service that improves the availability and performance of applications with global users. It gives you static IP addresses that act as a fixed entry point to your application endpoints, which could be in different AWS regions or on-premises.

By creating a CloudFront distribution that has both the S3 bucket and the ALB as origins, the company can reduce latency for both the static and dynamic data. The CloudFront distribution acts as a content delivery network (CDN), caching the data closer to the users and reducing the latency. The company can then configure Route 53 to route traffic to the CloudFront distribution, providing improved performance for the web application.

**AWS Global Accelerator** and **Amazon CloudFront** are separate services that use the AWS global network and its edge locations around the world. CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery). Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover. Both services integrate with AWS Shield for DDoS protection.

**Quick Comparison**

Global Accelerator → accelerates **dynamic** traffic (APIs, gaming, VoIP, EC2, ALB, NLB).

CloudFront → accelerates **static** content (S3 objects, cached files, media).
<br>
**API Acceleration**
  1. API acceleration encompasses a variety of strategies aimed at optimizing API performance, making applications faster and more reliable.
<br>

**TCP (Transmission Control Protocol), UDP (User Datagrakm Protocol)**
  1. are two fundamental protocols within the Internet Protocol suite used for transmitting data over networks.
     1. TCP
         - Connection-Oriented: Establishes a connection before data is sent, ensuring both sender and receiver are ready.
         - Reliability: TCP ensures that all packets arrive and are in the correct order. If packets are lost, they are retransmitted.
         - Error Checking and Flow Control: Uses checksums for error-checking and implements flow control to manage the rate of data transmission.
     2. UDP
         - Connectionless: Does not establish a connection before sending data; packets are sent without prior agreement from the receiver.
         - Unreliable: There are no guarantees that packets arrive in order or even arrive at all. If a packet is lost, it is not retransmitted.
         - Lower Latency: Due to minimal overhead, UDP is faster, making it suitable for real-time applications where speed is more critical than reliability.
 - TCP : Web Search, Email, File Sending.. reliability.
 - UDP : Live Streaming, Online Game.. real-time stuff.
<br>
     
**S3 Cross-Region Replication**
  1. feature that automatically replicates data stored in one Amazon S3 bucket to another S3 bucket in a different AWS region. This replication helps enhance data durability, availability, and compliance by ensuring that data is stored across multiple geographic locations.
<br>

**AWS Snowball**
  1. a highly versatile, portable storage and compute device used for transferring large amounts of data in and out of AWS. Designed to handle petabyte-scale data transfers.
  2. Provides up to 80 TB of usable storage capacity.
  3. Big amount of Data into and out of AWS
<br>

**Amazon Elastic Block Store (EBS)**
  1. a high-performance block storage service designed for use with Amazon EC2 (Elastic Compute Cloud).
  2. It provides scalable storage volumes that can be attached to EC2 instances, enabling low-latency access to data for applications such as databases, file systems, and enterprise applications.
  3. WHy EBS over S3? S3 is for the access through internet. EBS is mainly for EC2.
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
  3. Redshift is optimized for **high-performance analysis** of structured and semi-structured data, making it a key component for **data analytics and business intelligence solutions**.
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
  3.  IAM role : is an AWS resource that allows you to **delegate access to AWS resources and services**. You can create an IAM role that grants access to the S3 bucket and then attach the role to the EC2 instances. This will allow the EC2 instances to access the S3 bucket and the documents stored within it.
  4.  IAM policy : is used to **define permissions for an IAM user or group**, not for an EC2 instance.
  5.  IAM Group : is used to group together IAM users and policies, not to grant access to resources.
  6.  IAM user : is used to **represent a person or service that interacts with AWS resources**, not to grant access to resources.
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
  3. For analytic purpose
<br>

**Amazon Simple Notification Service**
  1. a fully managed messaging service designed to facilitate the sending of notifications and messages between distributed systems and applications.
  2. It enables users to send messages to a variety of endpoints, such as mobile devices, email addresses, and other applications seamlessly and effectively.
<br>

**Amazon Simple Queue Service (Amazon SOS)**
  1. is a fully managed message queuing service that enables applications to communicate and coordinate through message-based workflows.
  2. SQS allows **decoupling** of components in distributed systems, which enhances scalability and reliability.
<br>

**Decoupling**
  1. refers to the architectural design principle of separating components of a system to minimize dependencies between them. 
<br>

**Auto Scaling Group (ASG)**
  1. an AWS service that automatically adjusts the number of Amazon EC2 instances in response to the specific conditions you define.
  2. This ensures that the application has the right amount of resources available to handle varying loads while maintaining performance and minimizing costs.
<br>

**fan-out**
  1. a messaging pattern commonly used in distributed systems, particularly in event-driven architectures.
  2. It refers to the practice of sending a single message to multiple consumers simultaneously, allowing each subscriber to receive the same message without duplicating the effort of sending it multiple times.
<br>

**AWS CloudTrail**
  1. AWS CloudTrail is a service that enables governance, compliance, and operational and risk auditing of your AWS account.
  2. It continuously monitors and records account activity across your AWS infrastructure, providing logs of actions taken by users, roles, or AWS services.
<br>

**AWS DataSync**
  1. a service designed to simplify and automate the process of transferring data between on-premises storage systems and AWS storage services, as well as between different AWS storage services.
  2. It accelerates and secures the transfer of large datasets, making it ideal for various use cases.
<br>

**File Lifecycle management**
  1. the process of managing files throughout their lifecycle, from creation to deletion.
  2. This practice enables organizations to optimize storage resources, ensure compliance, and maintain efficient workflows.
<br>

**Amazon FSx**
  1. a fully managed **file storage service** designed to provide high-performance storage for **machine learning, web applications, and other workloads that require fast, scalable file storage**.
<br>

**Amazon S3 Glacier Deep Archive**
  1. a low-cost cloud storage service designed for data archiving and long-term backup.
  2. It is part of Amazon S3 (Simple Storage Service) and is specifically optimized for infrequently accessed data that needs to be stored for extended periods.
  3. Low cost for Data Archiving.
<br>

**SMB(Server Message Block)**
  1. a network protocol used for providing shared access to files, printers, and serial ports between nodes on a network.
  2.  It enables applications on one computer to read and write to files and request services from server programs in a computer network.
<br>

**Amazon S3 File Gateway**
  1. a hybrid cloud storage service that allows on-premises applications to access Amazon S3 storage through standard file protocols such as NFS (Network File System) and SMB (Server Message Block).
  2. This service makes it easy to integrate on-premises environments with cloud storage, providing essential capabilities for backup, archiving, and cloud data processing.
<br>

**Amazon Cognito user pools**
  1. Amazon Cognito provides authentication, authorization, and user management for your web and mobile apps.
  2. Users can sign in directly with a user name and password, or through a trusted third party.
<br>

**Amazon RDS**
  1. a managed cloud database service offered by Amazon Web Services (AWS) that simplifies the setup, operation, and scaling of relational databases in the cloud.
  2. Diffrent engines
      1. Aurora
         1. AURORA is **5x performance improvement over MySQL** on RDS and **handles more read requests than write**
         2. Aurora is a fully managed, MySQL-compatible relational database that is designed for high performance and high availability. **Aurora Multi-AZ deployments** automatically maintain a synchronous standby replica in a different Availability Zone to provide high availability. Additionally, **Aurora Auto Scaling** allows you to automatically scale the number of Aurora Replicas in response to read workloads, allowing you to meet the demand of unpredictable read workloads while maintaining high availability. This would provide an automated solution for scaling the database to meet the demand of the application while maintaining high availability.
      2. MySQL
      3. PostgreSQL
      4. MariaDB
           1. storage configuration : gp3 includes 3000IOPS
           2. General Purpose : balance between performance and price. up to 3000IOPS
           3. Provisioned IOPS Storage : up to 64000 IOPS.
           4. Magnetic Storage : deprecated. 
<br>

**Metadata of EC2**
  1. curl http://169.254.169.254/latest/meta-data/
      1. Instance ID
      2. AMI ID
      3. Instance type
      4. Security group information
      5. IAM roles and temporary security credentials
<br>

**Lambda**
  1. a serverless computing service that lets you run code without provisioning or managing servers. You simply upload your code as a Lambda function, and AWS Lambda automatically scales and manages the infrastructure needed to run your code.
  2. event-driven compute service that runs code in response to events—such as HTTP requests, data changes, or scheduled tasks—without requiring server management, patching, or manual scaling.
<br>

**AWS Secret Manager**
  1. a managed service that secures, rotates, and manages sensitive information like database credentials, API keys, and OAuth tokens throughout their lifecycle.
  2. rotate : for example, API key changes regularly.
  3. Using AWS Secrets Manager and enabling automatic rotation is the recommended solution for minimizing the operational overhead of credential management. AWS Secrets Manager provides a secure and centralized service for storing and managing secrets, such as database credentials. By leveraging Secrets Manager, the application can retrieve the database credentials programmatically at runtime, eliminating the need to store them locally in a file. Enabling automatic rotation ensures that the database credentials are regularly rotated without manual intervention, enhancing security and compliance.
<br>

**AWS System Manager Parameter Store**
  1. provides secure, hierarchical storage for configuration data, application secrets, and database strings, enabling centralized management across AWS services.
  2. For example, DB PW, or License Code.
  3. Doesn't offer auto rotation
<br>

**DNS(Domain Name System)**
  1. The term DNS name refers to a human-readable address used to identify a resource on the Internet. It is part of the Domain Name System (DNS), which translates these names into IP addresses that computers use to communicate with each other.
<br>

**ElastiCache**
  1. It is a fully managed, in-memory data store service provided by AWS that enhances the performance of applications by improving data retrieval speeds.
      1. In-Memory Caching
      2. Automatic Scaling
      3. Data Persistence
      4. Multi-AZ Deployment
      5. Security Features

  2. **ElastiCache for Memcached** is a managed service that simplifies the setup, operation, and scaling of Memcached in the cloud. **Memcached** is an open-source, high-performance, distributed memory caching system designed to store small chunks of arbitrary data (strings, objects) from results of database calls, API calls, or page rendering.
<br>

**AWS Network Firewall**
  1.  is a managed service that offers centralized network protection for your Amazon Virtual Private Cloud (VPC). It provides flexible, scalable, and highly available network security to protect your cloud resources from threats.
  2.  It is for traffic inspection.
<br>

**AWS Firewall Manager**
  1. centralized management of firewalls across multiple AWS accounts and services.
<br>

**Traffic Mirroring**
  1. a feature that allows you to capture and inspect network traffic in your Amazon Virtual Private Cloud (VPC). It enables you to create copies of the traffic flowing to and from elastic network interfaces (ENIs) and send them to monitoring or analysis devices in your network.
  2. Use Cases : Security Monitoring, Troubleshooting, Compliance Audits
<br>

**Elastic Network Interfaces**
  1.  a key component of Amazon Web Services (AWS) networking architecture, particularly within Amazon Elastic Compute Cloud (EC2). An ENI is a virtual network interface that you can attach to an instance in a Virtual Private Cloud (VPC).
  2.  provide flexibility and enhance the networking capabilities of EC2 instances, facilitating better traffic management and higher availability.
<br>

**data lake**
  1. A data lake is a centralized repository that allows you to store large amounts of structured, semi-structured, and unstructured data in its native format until it's needed for analysis.
  2. You just put eveything in.
<br>

**Amazon QuickSight**
  1. a cloud-powered business intelligence (BI) service offered by AWS that enables users to visualize their data, perform ad-hoc analysis, and create interactive dashboards.
  <br>

**AWS Glue**
  1. AWS Glue is a fully managed extract, transform, and load (ETL) service that simplifies the process of moving data between data sources and data lakes. It provides features like data cataloging, schema discovery, and job scheduling. Two key components of AWS Glue are *tables* and *crawlers*.
   
  2. **Crawlers** are automated processes that scan your data stores to discover and catalog your data. They infer the schema, data types, and relationships, making them essential for organizing data within the Glue Data Catalog.
   
  3. **Tables** in AWS Glue refer to the metadata representations of the data stored in various data sources. When a crawler runs, it creates or updates tables in the Glue Data Catalog based on the discovered data.
<br>

**Data Cataloging**
  1. is the process of creating an organized inventory of data assets within an organization. It involves collecting, organizing, and managing metadata about data sources to make it easier for users to discover, understand, and utilize data effectively.
<br>

**stateless**
   1. refers to a system or application design philosophy where each request from a client is treated as an independent transaction, unrelated to any previous requests.
<br>

**three-tier web application**
  1. A three-tier web application architecture divides the application into three distinct layers or tiers: the presentation layer, the business logic layer, and the data layer. This separation enhances modularity, scalability, and maintainability.

**AWS marketplace**
  1. is a digital catalog that allows users to find, buy, and deploy software and services that run on Amazon Web Services (AWS).
  2. Tech Companies, software vendors sell their products here.
<br>

**Network Load Balancer**
  1. is designed to handle extreme traffic volumes while maintaining high availability and reliability. It operates at the transport layer (Layer 4) and is optimized to manage large-scale, TCP traffic across multiple availability zones.
  2. Purpose:
      - Distribute TCP / UDP traffic to backend servers with extremely low latency and very high throughput.
<br>

**Layer 4 (transport layer)**
  1. The transport layer, also known as Layer 4 in the OSI (Open Systems Interconnection) model, is responsible for the end-to-end communication over networks. It ensures reliable data transfer between devices and facilitates the proper handling of data packets.

<br>

**OSI model (Open Systems Interconnection)**
  1. The OSI model is a conceptual framework used to understand and standardize the functions of a networking system. It divides the communication process into seven distinct layers, allowing different hardware and software systems to communicate with one another.
  2. Physical Layer
  3. Data Link Layer
  4. Network Layer
  5. Transport Layer
  6. Session Layer
  7. Presentation Layer
  8. Application Layer
<br>

**Application Load Balancer**
<br>

**Gateway Load Balancer**
  1. is a specialized load balancer designed to deploy, scale, and manage network virtual appliances such as firewalls, intrusion detection systems, or packet inspection tools.
  2. It combines the capabilities of:
    1. Transparent network gateway
    2. Load balancer for security appliances
  3. GWLB allows you to insert security appliances into network traffic transparently.
  4. Purpose:
      - Insert network security appliances into traffic flow.
      - Instead of sending traffic directly to an app, GWLB sends it to security devices first.
<br>

**AWS Transit Gateway**
   1. is a network hub that connects multiple VPCs, VPNs, and on-premise networks together.
   2. Think of it as a central router for your AWS networks. Instead of N² connections, you get one central hub.
   3. TGW can connect:
    Multiple Amazon Virtual Private Cloud
      1. Site-to-site VPN
      2. Direct Connect
      3. Other AWS accounts
      4. Other AWS regions
   4. TGW Route Tables  
      1. Control which networks can communicate.
        Example:
          10.1.0.0/16 → VPC1
          10.2.0.0/16 → VPC2
          10.3.0.0/16 → VPC3