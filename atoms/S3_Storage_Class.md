## Summary
S3 offers Standard, IA, OZ, Glacier, and Intelligent Tiering storage classes all with 99.9999999% durability but with variable costs, availability, retrieval [[SLA]]s.
## S3-Storage-Class Details

![Storage Class|600](s3-storage-classes.png)
#### Standard: 
- 99.99% availability. Sustain 2 concurrent facility failures. #resilient 
- Big data analytics, mobile , gaming applications, content distribution #UseCase 
#### IA : Infrequent Access
- 99.9% availability.
- Cost on retrieval.
- Disaster recovery, backups. #UseCase 
#### OZ : One-Zone
- 99.5% availability. Data loss if AZ is destroyed.
- Storing secondary backups or data that can be recreated. #UseCase 
#### S3 Glacier 
![Glacier](Glacier.md)
#### Intelligent Tiering
Small monthly monitoring and auto-tiering fee. Move objects automatically between tiers without charges for retrieval. #CostOptimized 
- Automatic
	- Frequent Access Tier (default)
	- Infrequent Access Tier (moved after 30 days)
	- Archive Instant Access Tier (moved after 90 days)
- Configurable
	- Archive Access Tier (90-700+ days)
	- Deep Archived Access Tier (180-700+ days)
## References
1.