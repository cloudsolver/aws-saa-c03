## Summary

## Solution Architectures Details
- You can achieve HA  with a multi-AZ deployment but it doesn't protect against DR.
- DR can be achieved with a multi-region architecture.
- ELB does support sticky sessions, however it does have disadvantages.
- Web Clients can store full session data, however it makes the session large and increases network traffic and might increase latency.
- ElastiCache offers sub-milli-second latency and can be used for Shopping Carts as well DynamoDB

### Stateless Application Architecture
* Elastic IP and DNS round-robin is not resilient. Because TTL of DNS round-robin can cause partial failure when an instance goes down.
* Adding ALB and pointing DNS to ALB can offer protections, because ALB can point to private EC2 instances with health checks. However, ALBs and EC2 instances can fail in the AZ.
* Multi-AZ ALB, EC2 can offer High Availability with failover to another AZ.
* Multi-Region with a secondary failover region and Multi-AZ in each region can offer Disaster Recovery and business continuity along with high availability at a higher cost.
* Reserved Instances, and Auto Scaling group can help save costs. #cost-optimized 

### Stateful Application Architecture
- ELB does support sticky sessions, however it does have disadvantages.
- Web Clients can store full session data, however it makes the session large and increases network traffic and might increase latency.
- ElastiCache offers sub-milli-second latency and can be used for Shopping Carts as well DynamoDB. Multi-AZ is supported.
- RDS can store user data, and a multi-AZ setup with Read Replicas will support HA and read scalability. #resilient 
- Applying security groups to EC2 to reference ELB, and ElastiCache to EC2, and RDS to EC2 will provide an additional layer of security. #secure  
### Wordpress scalability
 - EC2 Instance with an EBS volume can be used for images, but it won't scale horizontally.
 - Instead of EBS, use ENI that points to an EFS where multiple EC2 instances can read and write files.
- You could also use S3 Buckets (I think)
### Elastic Beanstalk
- Web Server Tier
	- ASG with EC2 across Two AZs fronted by an ELB. 
	- ELB has Worker Tier
## References

1. [Elastic BeanStalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.html)
2. 