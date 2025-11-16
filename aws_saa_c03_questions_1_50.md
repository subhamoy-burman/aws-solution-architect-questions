# AWS Certified Solutions Architect – Associate (SAA-C03)
## Questions 

---

### 1  
A company collects 500 GB of sensor data per site per day from global locations and wants to aggregate everything into one S3 bucket as quickly as possible while minimizing operational overhead. Each site has high-speed internet.  
A. Turn on S3 Transfer Acceleration on the destination bucket; upload directly with multipart upload.  
B. Upload to the nearest regional bucket; use Cross-Region Replication to the destination bucket; delete from origin.  
C. Ship daily Snowball Edge devices from each site; replicate to destination bucket.  
D. Upload to EC2 in the nearest region; store on EBS; snapshot and copy to destination region.

---

### 2  
A company stores application logs in JSON format in S3 and needs to run simple on-demand SQL queries with minimal operational overhead.  
A. Use Amazon Redshift to load the logs and run queries.  
B. Store logs in CloudWatch Logs; run SQL from the CloudWatch console.  
C. Use Amazon Athena directly on S3 for queries.  
D. Catalog logs with AWS Glue and run queries on a transient EMR Spark cluster.

---

### 3  
An organization uses AWS Organizations and wants to limit access to an S3 bucket in the management account to IAM principals only from accounts inside the organization.  
A. Add the aws:PrincipalOrgID condition key to the bucket policy.  
B. Create OUs per department; add aws:PrincipalOrgPaths to the bucket policy.  
C. Monitor CloudTrail events and update the bucket policy manually.  
D. Tag every user; add aws:PrincipalTag to the bucket policy.

---

### 4  
An EC2 instance in a private subnet must reach an S3 bucket without internet connectivity.  
A. Create a gateway VPC endpoint for S3.  
B. Stream logs to CloudWatch Logs; export to S3.  
C. Create an instance profile to allow S3 access.  
D. Create an API Gateway private link to access the S3 endpoint.

---

### 5  
A web application stores user documents on EBS volumes behind an ALB in one AZ. After duplicating the stack in a second AZ, users see only a subset of their documents after each refresh.  
A. Copy data so both EBS volumes contain all documents.  
B. Configure ALB to direct a user to the server that owns the documents.  
C. Migrate data to Amazon EFS and modify the application to use EFS.  
D. Configure ALB to send every request to both servers and merge responses.

---

### 6  
A company has 70 TB of video files (1 MB–500 GB each) on NFS and wants to migrate to S3 as fast as possible while using the least network bandwidth. The NFS store is no longer growing.  
A. Use the AWS CLI to copy files directly to S3.  
B. Order a Snowball Edge device; copy data and return the device.  
C. Deploy an S3 File Gateway; copy data through the gateway.  
D. Set up Direct Connect plus S3 File Gateway; copy data through the gateway.

---

### 7  
An application ingests 100 000 messages/second spikes and dozens of microservices must consume them. The company wants a decoupled, scalable solution.  
A. Persist messages to Kinesis Data Analytics; let consumers read from it.  
B. Run ingestion on EC2 in an Auto Scaling group based on CPU.  
C. Write to a single-shard Kinesis Data Stream; preprocess with Lambda; store in DynamoDB; consumers read from DynamoDB.  
D. Publish to an SNS topic with multiple SQS subscriptions; consumers read from queues.

---

### 8  
A distributed legacy application has a primary server that submits jobs to compute nodes. The company wants to modernize for resiliency and scalability.  
A. Replace the primary server with an SQS queue; run compute nodes in an Auto Scaling group; use scheduled scaling.  
B. Replace the primary server with an SQS queue; run compute nodes in an Auto Scaling group; scale on queue depth.  
C. Put primary and compute nodes in one Auto Scaling group; use CloudTrail as job destination; scale on primary load.  
D. Put primary and compute nodes in one Auto Scaling group; use EventBridge as job destination; scale on compute load.

---

### 9  
An SMB file server holds 70 TB of videos accessed frequently for 7 days, rarely afterwards. The company wants to extend storage without losing low-latency access to new files and automate lifecycle.  
A. Use DataSync to copy &gt;7-day-old data to AWS.  
B. Create an S3 File Gateway; transition &gt;7-day data to Glacier Deep Archive with lifecycle.  
C. Create an FSx for Windows file system.  
D. Install an S3 utility on user desktops; transition &gt;7-day data to Glacier Flexible Retrieval with lifecycle.

---

### 10  
An ecommerce order must be processed exactly in the order received; peak load is millions of requests/hour with millisecond latency.  
A. API Gateway → SNS topic → Lambda.  
B. API Gateway → SQS FIFO queue → Lambda.  
C. API Gateway authorizer blocks concurrent requests.  
D. API Gateway → SQS standard queue → Lambda.

---

### 11  
An application on EC2 uses local files to store DB passwords. The company wants to minimise credential-management overhead.  
A. Store credentials in AWS Secrets Manager with rotation.  
B. Store credentials in Systems Manager Parameter Store with rotation.  
C. Encrypt credentials with KMS; store in S3; point application to S3.  
D. Encrypt credentials; store on a new encrypted EBS volume per instance.

---

### 12  
A global company serves static content from S3 and dynamic content from EC2 behind an ALB. Route 53 is authoritative. How to reduce latency worldwide?  
A. CloudFront with S3 and ALB as origins; Route 53 → CloudFront.  
B. CloudFront (ALB origin) + Global Accelerator (S3 endpoint); Route 53 → CloudFront.  
C. CloudFront (S3 origin) + Global Accelerator (ALB + CloudFront); custom domain → accelerator.  
D. CloudFront (ALB origin) + Global Accelerator (S3); two domains for static vs dynamic.

---

### 13  
A company must rotate RDS MySQL credentials monthly across multiple regions with least overhead.  
A. Secrets Manager multi-region secret with automatic rotation.  
B. Parameter Store secure-string parameter with multi-region replication.  
C. Store encrypted credentials in S3; EventBridge triggers Lambda to rotate.  
D. Encrypt with KMS multi-region key; store in DynamoDB global table; Lambda rotates.

---

### 14  
An ecommerce site on EC2/ALB uses a large MySQL 8.0 EC2 instance. Reads are high; performance degrades quickly; the DB must auto-scale reads and stay highly available.  
A. Redshift single-node.  
B. Single-AZ RDS MySQL with read replicas.  
C. Multi-AZ Aurora with Aurora Auto Scaling read replicas.  
D. ElastiCache Memcached on Spot instances.

---

### 15  
A production VPC needs inline traffic inspection/filtering like the on-premises firewall appliance.  
A. Enable GuardDuty.  
B. Mirror traffic with Traffic Mirroring.  
C. Deploy AWS Network Firewall with rules.  
D. Use Firewall Manager to create rules.

---

### 16  
A data lake in S3 and RDS PostgreSQL needs dashboards for management only; others get limited access.  
A. QuickSight analysis; share dashboards via IAM roles.  
B. QuickSight analysis; share dashboards via users/groups.  
C. Glue crawler + ETL job; publish reports to S3; bucket policies control access.  
D. Glue crawler; Athena federated query; publish to S3; bucket policies control access.

---

### 17  
Two EC2 instances need access to an S3 bucket.  
A. Create IAM role for S3; attach to EC2 instances.  
B. Create IAM policy; attach to EC2 instances.  
C. Create IAM group; attach to EC2 instances.  
D. Create IAM user; attach to EC2 instances.

---

### 18  
A stateless microservice must compress user-uploaded images (S3 → Lambda → S3). Choose TWO.  
A. S3 event → SQS queue.  
B. Lambda triggered by SQS; delete message after success.  
C. Lambda monitors S3; keeps state in memory.  
D. EC2 polls SQS; logs state; invokes Lambda.  
E. EventBridge → SNS alert to owner.

---

### 19  
A three-tier web app (public subnet) must send all traffic through a third-party firewall appliance in an inspection VPC before reaching the web server.  
A. Public NLB in app VPC → appliance.  
B. Public ALB in app VPC → appliance.  
C. Transit Gateway in inspection VPC; route through it.  
D. Gateway Load Balancer in inspection VPC; GWLB endpoint receives traffic → appliance.

---

### 20  
Clone 20 TB production EBS volumes to a test environment in the same region; must deliver high I/O immediately; production must not be affected.  
A. Snapshot → restore to instance-store volumes.  
B. Multi-Attach EBS; snapshot; attach production volumes to test.  
C. Snapshot → create new volumes → attach to test instances.  
D. Snapshot with fast-snapshot-restore → create new volumes → attach.

---

### 21  
A one-deal-a-day website serves static content; must handle millions of requests/hour with millisecond latency and least operational overhead.  
A. Full site in multiple S3 buckets + CloudFront.  
B. Full site on EC2 Auto Scaling + dual ALB + RDS MySQL.  
C. Containerised on EKS with Cluster-Autoscaler + RDS.  
D. Static content in S3 + CloudFront; APIs via API Gateway + Lambda; data in DynamoDB.

---

### 22  
Media files (some hot, some cold, unpredictable pattern) must survive AZ loss; storage and retrieval cost must be minimised.  
A. S3 Standard.  
B. S3 Intelligent-Tiering.  
C. S3 Standard-IA.  
D. S3 One Zone-IA.

---

### 23  
Backup files in S3 Standard are accessed frequently for 1 month, never afterwards; must be kept indefinitely at lowest cost.  
A. Intelligent-Tiering auto-migration.  
B. Lifecycle → Glacier Deep Archive after 1 month.  
C. Lifecycle → Standard-IA after 1 month.  
D. Lifecycle → One Zone-IA after 1 month.

---

### 24  
Unwanted vertical scaling of EC2 types increased cost. Generate a 2-month cost graph by instance type with least overhead.  
A. AWS Budgets report.  
B. Cost Explorer granular filter.  
C. Billing dashboard graphs.  
D. Cost & Usage Report → S3 → QuickSight.

---

### 25  
Lambda receives data via API Gateway and inserts into Aurora PostgreSQL. Volume grew; quotas had to be raised. Need scalable, low-config refactor.  
A. Rewrite Lambda to Tomcat on EC2; use JDBC.  
B. Switch Aurora to DynamoDB + DAX cluster.  
C. Two Lambdas: receiver + loader; link via SNS.  
D. Two Lambdas: receiver + loader; link via SQS.

---

### 26  
Ensure S3 buckets have no unauthorised configuration changes.  
A. Enable AWS Config with rules.  
B. Enable Trusted Advisor.  
C. Enable Amazon Inspector.  
D. Enable S3 server-access logging + EventBridge.

---

### 27  
A CloudWatch dashboard must be shared with a product manager who has no AWS account; follow least privilege.  
A. Share dashboard via email; PM creates password.  
B. Create IAM user with CloudWatchReadOnlyAccess; send credentials + URL.  
C. Create IAM user with ViewOnlyAccess; PM navigates to dashboard.  
D. Bastion host with cached credentials; RDP to view.

---

### 28  
Central SSO for multi-account AWS Organization; users/groups remain in on-prem AD.  
A. Enable AWS SSO; one-way forest/domain trust via AWS Managed AD.  
B. Enable AWS SSO; two-way forest trust via AWS Managed AD.  
C. AWS Directory Service; two-way trust with on-prem AD.  
D. Deploy on-prem IdP; enable AWS SSO.

---

### 29  
VoIP service on EC2 in multiple regions; UDP traffic; route users to lowest-latency region; automatic failover.  
A. NLB + target group; use NLB as Global Accelerator endpoint in each region.  
B. ALB + target group; use ALB as Global Accelerator endpoint in each region.  
C. NLB + target group; Route 53 latency record to NLB aliases; CloudFront origin.  
D. ALB + target group; Route 53 weighted record; CloudFront origin.

---

### 30  
RDS MySQL instance used 48 h/month; must minimise cost without reducing compute/memory; Performance Insights enabled.  
A. Stop/start instance when needed.  
B. Auto Scaling policy.  
C. Snapshot → terminate → restore snapshot when needed.  
D. Modify to smaller instance when not needed.

---

### 31  
Ensure every EC2, RDS and Redshift resource is tagged with least effort.  
A. AWS Config rules.  
B. Cost Explorer display.  
C. API script on EC2.  
D. Scheduled Lambda to check tags.

---

### 32  
Host a static website (HTML, CSS, client JS, images) most cost-effectively.  
A. Containerise and run on Fargate.  
B. S3 static-website hosting.  
C. EC2 web server.  
D. ALB with Lambda target.

---

### 33  
Online marketplace: millions of financial transactions/day; share with internal apps in near-real-time; remove PII; store in document DB for low-latency lookup.  
A. DynamoDB → DynamoDB Streams → consumers; Lambda scrubs PII.  
B. Kinesis Firehose → DynamoDB + S3; Lambda scrubs PII; consumers read S3.  
C. Kinesis Data Streams → Lambda (scrub) → DynamoDB; consumers read stream.  
D. Batch files in S3 → Lambda scrub → update S3 → DynamoDB; consumers read S3.

---

### 34  
Track configuration changes on AWS resources AND record API call history for compliance.  
A. CloudTrail for config; Config for API calls.  
B. Config for config; CloudTrail for API calls.  
C. Config for config; CloudWatch for API calls.  
D. CloudTrail for config; CloudWatch for API calls.

---

### 35  
Public-facing web app behind ELB; third-party DNS; detect and protect against large-scale DDoS.  
A. GuardDuty.  
B. Inspector on EC2.  
C. Shield + Route 53.  
D. Shield Advanced + assign ELB.

---

### 36  
Data in two S3 buckets (two regions) must be encrypted/decrypted with the same customer-managed KMS key; key must exist in both regions; least overhead.  
A. SSE-S3 + replication.  
B. Multi-region customer-managed key; client-side encryption; replication.  
C. Customer-managed key per region; SSE-S3; replication.  
D. Customer-managed key per region; SSE-KMS; replication.

---

### 37  
1000 EC2 Linux instances run third-party software. Patch all quickly for critical vulnerability; repeatable; native AWS; least overhead.  
A. Lambda to patch all.  
B. Patch Manager.  
C. Maintenance Window.  
D. Run Command custom script.

---

### 38  
Static website on S3 + Route 53; global users; decrease latency; most cost-effective.  
A. Replicate bucket to every region; geolocation routing.  
B. Global Accelerator IPs → bucket; update Route 53.  
C. CloudFront in front; Route 53 → CloudFront.  
D. S3 Transfer Acceleration; Route 53 → new endpoint.

---

### 39  
Searchable 10 M-row MySQL table; 2 TB GP-SSD; inserts &gt;10 s; storage performance bottleneck.  
A. Switch to Provisioned IOPS SSD.  
B. Memory-optimised instance class.  
C. Burstable instance class.  
D. Multi-AZ read replicas.

---

### 40  
1000 edge devices; 1 TB alerts/day; 2 KB each; highly available; no infrastructure to manage; 14 days hot, then archive.  
A. Kinesis Firehose → S3; lifecycle to Glacier after 14 days.  
B. EC2 fleet behind ALB → S3; lifecycle to Glacier.  
C. Firehose → OpenSearch; manual snapshots; delete &gt;14 days.  
D. SQS 14-day retention; consumer moves to S3 after 14 days.

---

### 41  
Ingest data from many SaaS sources to S3; files up to 200 GB; EC2 does upload & notification; slow; least overhead improvement.  
A. Auto Scaling EC2 + S3 event → SNS.  
B. AppFlow SaaS→S3; S3 event → SNS.  
C. EventBridge per SaaS → S3; second rule → SNS.  
D. Containerise on ECS; Container Insights → SNS.

---

### 42  
EC2 in private subnets download/upload images via single NAT gateway; want to remove regional data-transfer charges; most cost-effective.  
A. NAT gateway per AZ.  
B. Replace NAT gateway with NAT instance.  
C. Gateway VPC endpoint for S3.  
D. EC2 Dedicated Host.

---

### 43  
On-prem app backs up 70 TB/month to S3; internet bandwidth saturated; timely backups; minimal impact; long-term.  
A. VPN + VPC gateway endpoint.  
B. Direct Connect new connection; route backup traffic.  
C. Daily Snowball devices.  
D. Request removal of S3 limits.

---

### 44  
Critical S3 bucket must be protected from accidental deletion. (Choose TWO.)  
A. Enable versioning.  
B. Enable MFA Delete.  
C. Bucket policy.  
D. Default encryption.  
E. Lifecycle policy.

---

### 45  
SNS → Lambda ingestion; occasional network failures cause lost data; manual reruns needed; ensure all data ingested. (Choose TWO.)  
A. Deploy Lambda in multiple AZ.  
B. SNS → SQS queue.  
C. Increase Lambda CPU/memory.  
D. Increase Lambda provisioned throughput.  
E. Lambda reads from SQS.

---

### 46  
Stores upload 200 GB+ files via SFTP; some contain PII; alert admins and auto-remediate; least development effort.  
A. S3 + Inspector → lifecycle delete.  
B. S3 + Macie → SNS alert admins.  
C. Custom Lambda scanner → SNS alert admins.  
D. Custom Lambda scanner → SES + lifecycle delete.

---

### 47  
Need guaranteed EC2 capacity in three specific AZs in one region for one week.  
A. Buy Regional Reserved Instances.  
B. On-Demand Capacity Reservation (region only).  
C. Buy zonal Reserved Instances.  
D. On-Demand Capacity Reservation (region + three AZs).

---

### 48  
Catalog on EC2 instance-store must become highly available and durable.  
A. Move to ElastiCache Redis.  
B. Larger EC2 with bigger instance-store.  
C. Move to S3 Glacier Deep Archive.  
D. Move to Amazon EFS.

---

### 49  
Call-transcript files: random access within 1 year (fast), rare afterwards (delay acceptable); most cost-effective.  
A. Glacier Instant Retrieval + tag queries.  
B. Intelligent-Tiering → Glacier Flexible Retrieval; Athena for &lt;1 yr, Glacier Select for &gt;1 yr.  
C. Standard + metadata in Standard → Glacier Instant Retrieval after 1 yr; query metadata.  
D. Standard → Deep Archive after 1 yr; metadata in RDS; query RDS.

---

### 50  
1000 EC2 Linux instances; critical third-party patch; must apply quickly; repeatable; native AWS; least overhead.  
A. Lambda function.  
B. Patch Manager.  
C. Maintenance Window.  
D. Run Command.
