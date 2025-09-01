---
share: "true"
---
  
```table-of-contents  
```  
Large systems are distributed systems, they run on multiple servers  
  
“A system in which hardware or software components located at networked computers communicate and coordinate their actions only by message passing”  
  
Usually require high throughput, something like HTTPS is too slow  
  
“Independent computers that appear to the user as a single computer”  
  
Examples:  
  
Cluster computing  
  
Cloud computing  
  
Any system that is loosely connected over a comms network  
  
Since large systems are distributed, the two terms can be used interchangeably  
  
Clock synchronisation is a bitch  
  
“A distributed system is one on which I cannot get any work done because some machine I never heard of has crashed”  
  
# Networks vs. Distributed systems  
  
**Networks:** A media for interconnecting computers based on protocols. Entities are visible and addressed by IP addresses. Focuses on packets, routing, …  
  
**Distributed systems:** Existence of multiple autonomous computers. Every distributed system relies on a network  
  
# Why use distributed systems?  
  
- Functional separation: computers with different capabilities and purposes  
- Clients and servers: Data collection and data processing  
- Inherent distribution: distribute information and people  
- Load balancing  
- Reliability  
- Economic reasons: sharing is cheaper, economy of scale  
  
# Transparency  
  
To appear as a single system, hide:  
  
- Location  
- Failures  
- Replication (backups)  
- Relocations  
  
However, fully hiding all of this is practically impossible  
  
- Some latencies cannot be hidden  
- Completely hiding failures is impossible  
- Hard to distinguish between a slow computer and a failing one  
- Hard to be sure if a server performed an operation before a crash  
  
Fault tolerance costs performance  
  
- Keeping backups/replicas up to date takes time  
- Flushing write operations to disks for fault tolerance also has costs  
  
Sometimes, you really want data to be in sync (like in banking systems), sometimes it does not matter match (like youtube likes) (strong vs. weak consistency)  
  
# Scales  
  
Numerical size  
  
Number of users, machine, data  
  
Geographical  
  
LAN, region, country, continent, global  
  
Administrative  
  
One owner, many owners, anarchy  
  
# Scaling  
  
Bigger machines (scale up / vertical scaling) just get better machines  
  
Scores do not increase linearly  
  
There is a limit, at some point there is no bigger model  
  
Complex hardware → complex behaviour  
  
Software has to be able to utilise the hardware  
  
Replication: caching, temporary replication  
  
Partitioning: AKA sharding (db level)  
  
Asynchronous communication  
  
Virtualisation  
  
Aggregate physical parts (machines) into a larger logical whole  
  
Decouple interface from implementation (e.g. NFS)  
  
  
