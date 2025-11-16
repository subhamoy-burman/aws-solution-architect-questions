# AWS Certified Solutions Architect – Associate (SAA-C03)
## Questions 51 – 100 (Clean Version)

---

### 51  
A company wants to collect and analyze clickstream data from multiple websites. The data must be available in near-real-time for analytics and stored durably.  
A. Amazon Kinesis Data Streams → Amazon S3 → Amazon Athena.  
B. Amazon Kinesis Data Firehose → Amazon Redshift.  
C. Amazon SQS → Amazon EMR → Amazon S3.  
D. AWS DataPipeline → Amazon RDS → Amazon QuickSight.

---

### 52  
A business needs to store 5 TB of financial records that must be retained for 7 years and accessed rarely. Immediate access is not required.  
A. S3 Standard with lifecycle to S3 Glacier after 1 year.  
B. S3 Glacier Deep Archive.  
C. S3 Standard-IA.  
D. Amazon EFS Infrequent Access.

---

### 53  
An application running on EC2 instances must access a DynamoDB table without traversing the internet.  
A. DynamoDB Accelerator (DAX).  
B. VPC endpoint for DynamoDB.  
C. NAT Gateway.  
D. AWS Direct Connect.

---

### 54  
A company needs to share large datasets (100 TB) with external partners around the world cost-effectively.  
A. AWS Snowball Edge devices.  
B. S3 buckets with Requester Pays and CloudFront.  
C. EFS with IAM access.  
D. AWS Storage Gateway File Gateway.

---

### 55  
A serverless application must process uploaded images (resize, watermark) and store results back to S3.  
A. S3 → SNS → EC2 Auto Scaling.  
B. S3 → Lambda → S3.  
C. S3 → Kinesis Data Streams → EMR.  
D. S3 → SQS → ECS.

---

### 56  
A mobile app uploads photos. The upload must resume if interrupted and should use least effort.  
A. S3 multipart upload with presigned URLs.  
B. AWS Storage Gateway Volume Gateway.  
C. AWS Transfer Family SFTP.  
D. AWS DataSync.

---

### 57  
A company needs a secure way for on-premises users to access S3 without public internet.  
A. AWS VPN CloudHub.  
B. AWS Direct Connect + private VIF.  
C. AWS Storage Gateway Cached volumes.  
D. AWS Snowball.

---

### 58  
A startup wants to host a WordPress site with automatic scaling and managed updates.  
A. EC2 Auto Scaling + RDS.  
B. AWS Elastic Beanstalk with PHP platform.  
C. Amazon Lightsail.  
D. ECS with Fargate.

---

### 59  
An IoT fleet sends 1 GB of telemetry hourly. Data must be aggregated and queried ad-hoc.  
A. IoT Core → Kinesis Data Streams → S3 → Athena.  
B. IoT Core → DynamoDB Streams → Redshift.  
C. IoT Core → SQS → EC2 → RDS.  
D. IoT Core → CloudWatch Logs → Insights.

---

### 60  
A company needs to replicate its on-premises NFS shares to AWS with low-latency local access.  
A. AWS Storage Gateway File Gateway.  
B. AWS DataSync + S3.  
C. AWS Transfer Family.  
D. AWS Storage Gateway Tape Gateway.

---

### 61  
A microservice must authenticate users via social identity providers (Google, Facebook).  
A. Amazon Cognito Identity Pools.  
B. Amazon Cognito User Pools.  
C. AWS IAM SAML provider.  
D. AWS SSO.

---

### 62  
A CI/CD pipeline must build Docker images and store them privately.  
A. AWS CodeBuild → Amazon ECR.  
B. AWS CodeDeploy → Docker Hub.  
C. AWS CloudFormation → S3.  
D. AWS OpsWorks → ECS.

---

### 63  
A company needs to encrypt data at rest on EBS volumes with customer-managed keys.  
A. Enable EBS encryption with AWS managed keys.  
B. Enable EBS encryption with KMS customer-managed keys.  
C. Use third-party encryption agents.  
D. Encrypt within the OS.

---

### 64  
A gaming company needs sub-millisecond latency for leaderboards.  
A. Amazon RDS with ElastiCache Redis.  
B. Amazon DynamoDB with DAX.  
C. Amazon S3 + CloudFront.  
D. Amazon Neptune.

---

### 65  
A SaaS application needs isolation per tenant with minimal overhead.  
A. Separate VPC per tenant.  
B. IAM roles with tag-based policies.  
C. AWS Organizations SCPs.  
D. Kubernetes namespaces on EKS.

---

### 66  
A batch job must run nightly and requires 2 TB of memory for 3 hours.  
A. EC2 X1e instance scheduled with CloudWatch Events.  
B. ECS Fargate task.  
C. Lambda with 10 GB RAM.  
D. AWS Batch with Spot instances.

---

### 67  
A company must log and alert on root-account usage.  
A. CloudTrail + CloudWatch Logs + SNS.  
B. AWS Config + SNS.  
C. GuardDuty + EventBridge.  
D. Trusted Advisor + SNS.

---

### 68  
A web app must block SQL injection and DDoS.  
A. AWS WAF + Shield Advanced.  
B. Security Groups.  
C. NACLs.  
D. IAM policies.

---

### 69  
A data-science team needs a shared Jupyter environment with GPU access.  
A. Amazon SageMaker Studio.  
B. EC2 G4 instances.  
C. AWS Glue DevEndpoints.  
D. EMR with Spark.

---

### 70  
A company must enforce encryption in transit for all APIs.  
A. API Gateway with TLS 1.2.  
B. CloudFront with custom origin.  
C. VPN-only access.  
D. PrivateLink.

---

### 71  
A Lambda function must access a private RDS instance in a VPC.  
A. Attach Lambda to the same VPC/subnets.  
B. Use RDS Proxy.  
C. Use NAT Gateway.  
D. Use EC2 bastion.

---

### 72  
A marketing team needs to send 1 M emails/month with bounce/complaint tracking.  
A. Amazon SES.  
B. SNS.  
C. Pinpoint.  
D. Connect.

---

### 73  
A company must retain API-gateway logs for 1 year and query them monthly.  
A. CloudWatch Logs → S3 → Athena.  
B. CloudTrail → Glacier.  
C. Kinesis Firehose → Redshift.  
D. Elasticsearch Service.

---

### 74  
A mobile backend needs push notifications to iOS/Android.  
A. SNS with platform endpoints.  
B. SQS.  
C. Kinesis.  
D. API Gateway.

---

### 75  
A company wants to Visualize VPC traffic flows.  
A. VPC Flow Logs → Athena.  
B. CloudTrail → QuickSight.  
C. GuardDuty → Macie.  
D. Config → CloudWatch.

---

### 76  
A legacy app requires Windows file shares with AD integration.  
A. FSx for Windows.  
B. S3 File Gateway.  
C. EFS.  
D. Storage Gateway Volume Gateway.

---

### 77  
A Kubernetes platform must run across multiple AWS accounts with shared networking.  
A. EKS with VPC sharing.  
B. ECS with awsvpc mode.  
C. Fargate with Transit Gateway.  
D. Self-managed K8s on EC2.

---

### 78  
A company must ensure S3 objects are encrypted with AES-256 by default.  
A. Bucket policy denying non-encrypted uploads.  
B. S3 default encryption SSE-S3.  
C. Lambda to reject objects.  
D. CloudWatch Alarm.

---

### 79  
A DR plan requires RPO of 15 minutes for a MySQL database.  
A. RDS automated snapshots every 15 minutes.  
B. RDS Multi-AZ.  
C. Read replica with asynchronous replication.  
D. Binlog streaming to S3.

---

### 80  
A company needs to transfer 500 TB from on-prem to S3 within 2 weeks.  
A. VPN over Direct Connect.  
B. Multiple Snowball Edge devices.  
C. S3 Transfer Acceleration.  
D. DataSync over internet.

---

### 81  
A serverless data pipeline must join streaming data with S3 reference data.  
A. Kinesis Data Analytics with S3 reference.  
B. Lambda with DynamoDB.  
C. Glue streaming ETL.  
D. EMR streaming.

---

### 82  
A company must restrict SSH access to EC2 based on IAM identity.  
A. EC2 Instance Connect.  
B. Systems Manager Session Manager.  
C. Bastion with LDAP.  
D. VPN with MFA.

---

### 83  
A BI team needs a petabyte-scale data warehouse with minimal admin.  
A. Redshift Serverless.  
B. RDS PostgreSQL.  
C. EMR with Spark.  
D. Athena.

---

### 84  
A chat application needs WebSocket support behind a load balancer.  
A. ALB with WebSocket.  
B. NLB with TCP.  
C. CloudFront with Lambda@Edge.  
D. API Gateway WebSocket API.

---

### 85  
A company must rotate IAM access keys every 90 days automatically.  
A. AWS Config rule + Lambda.  
B. CloudTrail + CloudWatch.  
C. IAM policy condition.  
D. AWS SSO.

---

### 86  
A machine-learning model must be served with auto-scaling GPUs.  
A. SageMaker endpoints with auto-scaling.  
B. ECS with GPU instances.  
C. EC2 Auto Scaling with user-data script.  
D. Lambda with EFS.

---

### 87  
A company must meet PCI-DSS compliance for credit-card data.  
A. AWS Artifact agreements.  
B. GuardDuty findings.  
C. Macie classification.  
D. Config conformance packs.

---

### 88  
A global DNS query log must be centralized and analyzed.  
A. Route 53 Resolver Query Logs → CloudWatch Logs → Kinesis → S3 → Athena.  
B. CloudTrail.  
C. VPC Flow Logs.  
D. DNS Amplification detection in Shield.

---

### 89  
A batch workload must complete within 2 hours and uses 5000 vCPUs.  
A. EC2 Spot Fleet with Spot-optimized allocation strategy.  
B. On-Demand instances.  
C. Reserved instances.  
D. Lambda.

---

### 90  
A company must ensure that only corporate laptops can access S3.  
A. VPC endpoint with endpoint policy.  
B. S3 bucket policy with aws:PrincipalTag.  
C. IAM identity center with device trust.  
D. Client VPN certificate + S3 endpoint.

---

### 91  
A streaming app must retain 30 days of data and replay any day.  
A. Kinesis Data Streams with 30-day retention.  
B. Kinesis Data Firehose to S3.  
C. DynamoDB with point-in-time recovery.  
D. MSK (Kafka) with 30-day retention.

---

### 92  
A CI/CD pipeline must deploy blue-green ECS services.  
A. AWS CodeDeploy with ECS Blue/Green.  
B. CloudFormation stack sets.  
C. ECS rolling update.  
D. Elastic Beanstalk.

---

### 93  
A company must prevent accidental S3 bucket public access.  
A. Block Public Access at account level.  
B. S3 ACLs.  
C. Bucket policy denying *Principal.  
D. CloudFront origin access identity.

---

### 94  
A Lambda function must execute daily at 02:00 UTC.  
A. CloudWatch Events cron trigger.  
B. Step Functions wait state.  
C. SQS delay queue.  
D. ECS scheduled task.

---

### 95  
A media company needs to transcode 10,000 videos weekly with variable sizes.  
A. AWS Elemental MediaConvert.  
B. EC2 Spot Fleet with FFmpeg.  
C. Lambda with FFmpeg layer.  
D. ECS with GPU instances.

---

### 96  
A security team must receive alerts when IAM policies are modified.  
A. CloudTrail → CloudWatch Logs metric filter → SNS.  
B. Config rule → SNS.  
C. GuardDuty.  
D. Trusted Advisor.

---

### 97  
A company must share EBS snapshots with another AWS account securely.  
A. Modify snapshot permissions; share encrypted snapshot with KMS key grant.  
B. Copy to S3 and presign URL.  
C. Export to Snowball.  
D. AMI with encrypted snapshot.

---

### 98  
A web app must authenticate users with MFA and provide temporary S3 access.  
A. Cognito user pools with MFA → identity pool → STS.  
B. IAM users with MFA.  
C. API Gateway custom authorizer.  
D. Lambda with JWT.

---

### 99  
A company must migrate 1 PB from on-prem NFS to EFS with minimal cut-over time.  
A. DataSync + EFS.  
B. Snowball + EFS.  
C. S3 File Gateway.  
D. rsync over Direct Connect.

---

### 100  
A serverless app must store session state with 5-minute TTL.  
A. DynamoDB with TTL.  
B. ElastiCache Redis.  
C. S3 with lifecycle.  
D. Step Functions.
