## High Performing
1. Determine high-performing and scalable storage solutions.
	1. Hybrid storage solutions to meet business requirement.
	2. Storage services with appropriate use cases: S3, [EFS](EFS.md), [EBS](EBS.md).
	3. Storage types with associated characteristics: Object, File, Block.
	4. Skills:
		1. Determining storage services and configurations that meet performance demands.
		2. Determining storage services that can scale to accommodate future needs.
2. Design high-performing and elastic compute solutions.
	1. AWS compute services with appropriate use cases: AWS Batch, EMR, Fargate.
	2. Distributed computing concepts supported by AWS [[global infrastructure]] and edge services.
	3. Queuing and messaging concepts: Pub-sub.
	4. Scalability capabilities with appropriate use cases: [[Auto Scaling]] AWS Auto Scaling.
	5. Serverless technologoes and patterns: Lambda, Fargate.
	6. Orchestration of containers: ECS, EKS.
	7. Skills:
		1. Decoupling workloads so that components can scale independently.
		2. Identifying metrics and conditions to perform scaling actions.
		3. Selecting the appropriate compute options and features.
		4. Selecting the appropriate resource type and size (Lambda) to meet business requirements.
3. Determine## Cost Optimized
1. Design cost-optimized storage solutions.
	1. Access options: S3 with Requester Pays object storage.
	2. AWS cost management service features: Cost Allocation Tags, Multi-Account billing.
	3. AWS Cost Management tools with appropriate use cases: AWS Cost Explorer, AWS Budgets, AWS Cost and Usage Report.
	4. AWS storage services with appropriate use cases: Amazon FSx, Amazon [EFS](EFS.md), Amazon S3, Amazon [EBS](EBS.md).
	5. Backup strategies.
	6. Block storage options: HDD volume types, SSD volume types.
	7. Data lifecycles.
	8. Hybrid storage options: DataSync, Transfer Family, Storage Gateway.
	9. Storage access patterns.
	10. Storage tiering: Cold Tiering for object storage.
	11. Storage types with associated characteristics: Object, File and Block.
	12. Skills:
		1. Designing appropriate storage strategies: Batch uploads to AWS S3 compared with individual uploads.
		2. Determining the correct storage size for a workload.
		3. Determining the lowest cost method of transferring data for a workload to AWS storage.
		4. Determining when storage auto scaling is required. 
		5. Managing S3 object lifecycles.
		6. Selecting the appropriate backup and archival solution.
		7. Selecting the appropriate services for data migration to storage services
		8. Selecting the appropriate storage tier
		9. Selecting the correct data lifecycle for storage.
		10. Selecting the mnost cost-effective storage service for a workload.
2. Design cost-optimized compute solutions.
	1. AWS cost management service features: Cost Allocation Tags, Multi-Account Billing.
	2. AWS Cost Management tools with appropriate use cases: Cost Explorer, AWS Budgets, AWS Cost and Usage Report.
	3. AWS [[global infrastructure]]: Availability Zone, Regions.
	4. AWS purchasing options: Spot Instances, Reserved Instances, Savings Plans.
	5. Distributed compute strategies: Edge processing.
	6. Hybrid compute options: AWS Outposts, Snowball Edge.
	7. Instance types, families, and sizes: Memory optimized, compute optimized, virtualization.
	8. Optimization of compute utilization: [[Containers]], [[Serverless]] computing, [[Microservices]].
	9. Scaling strategies: Auto scaling, hibernation.
	10. Skills:
		1. Determining an appropriate load balancing strategy: ALB (Layer 7) , Network Load Balancer (Layer 4) compared with Gateway Load Balancer.
		2. Determining appropriate scaling methods and strategies for elastic workloads (Horizontal compared with Vertical, [EC2](EC2.md) Hibernation).
		3. Determining cost-effective AWS compute services with appropriate use cases: Lambda, [EC2](EC2.md), Fargate.
		4. Determining the required availability for different classes of workloads: production workloads, non-production workloads.
		5. Selecting the appropriate instance family and size for a workload.
3. Design cost-optimized database solutions.
	1. AWS cost management service features: Cost Allocation Tags, Multi-Account Billing.
	2. AWS Cost Management tools.
	3. Caching Strategies.
	4. Data retention policies.
	5. Data capacity planning.
	6. Data connections and proxies.
	7. Database engines with appropriate use cases: heterogenouse migrations, homogenous migrations.
	8. Database replication: read replicas.
	9. Database types and services: relational compares with non-relational, Aurora, DynamoDB.
	10. Skills:
		1. Designing appropriate backup and retention policies: snapshot frequency.
		2. Determining an appropriate database engine: MySQL versus PostGres.
		3. Determining cost-effective AWS database services with appropriate use cases: DynamoDB compares with Amazon RDS, serverless.
		4. Determining cost-effective AWS database type: time series format, columnra format.
		5. Migrating database schemas and data to different locations and different database engines.
		   
1. Design cost-optimized network architectures.
	1. AWS cost management service features and tools.
	2. Load balancing concepts: ALB.
	3. NAT gateways: NAT instnace costs compared with NAT gateway costs.
	4. Network connectivity: Private lines, dedicated lines, VPNs.
	5. Network routing, topology, and peering: AWS Transit Gateway, [[VPC]] peering.
	6. Network services with appropriate use cases: DNS.
	7. Skills:
		1. Configuring appropriate NAT gateway types for a network: Single shared NAT gateway compared with NAT gateways for each AZ.
		2. Configuring appropriate network connections: Direct Connect compared with VPN compared with Internet.
		3. Configuring appropriate network routes to minimize transfer costs: Region to Region, AZ to AZ, private to public, Global Accelerator, [[VPC]] endpoints.
		4. Determining strategic needs for content delivery networks and edge caching.
		5. Reviewing existing workloads for network optimizations.
		6. Selecting an appropriate throttling strategy.
		7. Selecting the appropriate bandwidth allocation for a network device: single VPN compared with multiple VPN, Direct Connect speed.
 high-performing database solutions.
	1. Caching strategies and services: ElastiCache.
	2. Data access patterns: Read-intensive compared to write-intensive.
	3. Database capacity planning: Capacity Units, Instance Types, Provisioned IOPS.
	4. Database connections and proxies.
	5. Database engines with appropriate use cases: Hetreogeneous migrations, homogenous migration.
	6. Database replication: Read replicas.
	7. Database types and services: Serverless, relational, non-replantion and in-memory.
	8. Skills:
		1. Configuring read replicas to meet business requirements.
		2. Designing database architectures.
		3. Determining an appropriate database engine: MySQL compared with PostgreSQL.
		4. Determining an appropriate database type: Auroro, DynamoDB.
		5. Integrating caching to meet business requirements.
4. Determined high-performing and scalable network architectures.
	1. Edge networking services weith appropriate use cases: Cloud Front, Global Accelerator.
	2. How to design network architecture: Subnet tiers, routing, IP addressing.
	3. Load balancing concepts: Application Load Balancer [[ALB]]
	4. Network connection options: AWS VPN, Direct Connect, AWS PrivateLink.
	5. Skills:
		1. Creating a network topology for various architecture: Global, Hybrid, Multi-tier.
		2. Determining network configurations that can scale to accomodate future needs.
		3. Determining the appropriate placement of resoureces to meet business requirements.
		4. Selecting the approrpriate load balancing strategy.
5. Determine high-performing data ingestion and transformation solutions.
	1. Data analytics and visualization services with appropriate use cases: Amazon Athena, Lake Formation, QuickSight.
	2. Data ingestion patterns.
	3. Data transfer services with appropriate use cases: AWS DataSync, AWS Storage Gateway.
	4. Data transformation services with appropriate use cases: AWS Glue.
	5. Secure access to ingestion access points.
	6. Sizes and speeds needed to meet business requirements.
	7. Streaming data services with appropriate use cases: Amazone Kinesis.
	8. Skills:
		1. Building and securing data lakes.
		2. Designing data streaming architectures.
		3. Designing data transfer solutions.
		4. Implementing visualization strategies.
		5. Selecting appropriate compute options for data processing: Amazone EMR.
		6. Selecting appropriate configurations for ingestion.
		7. Transforming data between formats: CSV to Parquet.