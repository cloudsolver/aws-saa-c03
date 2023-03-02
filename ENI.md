Eth0 is the primary ENI. Primary private IPv4, one or more secondary IPv4. One [Elastic IP](Elastic%20IP.md) per private IPv4. One public IPv4, onr or more security groups.
### [EC2](EC2.md), AZ and Other
An [EC2](EC2.md) instance can have one or more ENI attached to it e.g. Eth0 (primary) and Eth1 (secondary).
ENI can be created independently and attached to [EC2](EC2.md) instances or move them for failover. These are bound to a specific Availability Zone. 
Moving an ENI from one [EC2](EC2.md) instance to another is a network failover.
ENI's that are created separately will stay after an instance is destroyed.
Each ENI lives within a particular subnet of the VPC (and hence within a particular Availability Zone) and has the following attributes:

-   Description
-   Private IP Address
-   [[Elastic IP]] Address
-   [MAC Address](http://en.wikipedia.org/wiki/MAC_address)
-   [[Security Group]](s)
-   Source/Destination Check Flag
-   Delete on Termination Flag

#antipattern The idea of launching an [EC2](EC2.md) instance on a particular VPC subnet is effectively obsolete. A single [EC2](EC2.md) instance can now be attached to two ENIs, each one on a distinct subnet. The ENI (not the instance) is now associated with a subnet. #bestpractice 
#usecase MAC-based licensing can use an ENI. 
#usecase Low-Budget HA: Attach an ENI to an instance, if the instance dies launch another and then attach the ENI to it. Traffic flow will resume within seconds. 
#Q ENI can be attached to EC2 instance in another AZ?
Answer: False.
*Elastic Network Interfaces (ENIs) are bounded to a specific AZ. You can not attach an ENI to an EC2 instance in a different AZ.*