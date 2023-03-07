## Summary

## ElastiCache Detail
- ElastiCache is a managed Redis or Memcached #awsservice 
- In-memory databases with high performance and low latency. #performant 
- Reduce load off of databases for read-intensive workloads. #operational-excellence 
- Requires application code changes to use the cache.
### Solution Architecture
- Application will attempt to fetch data from the cache, if `cache miss` it will fetch from RDS, write to cache. #usecase 
- Sticky session can be eliminated from ALB by using a distributed cache - ensuring stateless infrastructure.
### Technology
- REDIS
	- Multi-AZ with Auto-Failover #reliable 
	- Read replicas scale reads #reliable #performant 
	- Data durability using AOF persistence #reliable 
	- Backup and restores.
	- Supports sets and sorted sets.
	- Gaming Leaderboards with guaranteed uniqueness and element ordering, and real time ranking through Redis Sorted Sets. #usecase 
- MEMCACHED
	- No HA, non-persistent, no backup and restore.
	- Multi-node for partitioning #performant 
### Security
- IAM Authentication for Redis
- IAM policies on ElastiCache are only used for AWS API-level security
#### Redis Auth
- You can set a "password/token" when you create a Redis cluster.
- This is an extra level of security for your cache.
- Support SSL in flight encryption.
#### Memcached
- Supports [[SASL]]-based authentication.
### Design Patterns
- Lazy Loading: Cache is loaded on demand.
- Write Through: Data is written to cache first, persistence occurs after.
- Session Store: Store temporary session data in cache with a TTL.
- 
## References

	1.