# Awesome Database Development

Database development is interesting and challenging. You can always find interesting things to learn and challenging problems to solve. You need to get a lot of things right to build a reliable and high-performance database. And it takes time, a lot of time, to think and practice. I have been working on databases for ten years. However, as the proverb goes, *the more I know, the more I realize I don't know.* So, I collect the database development materials I have read here to review them from time to time. I think it will be helpful to those who share the same interests as me.

## Storage Device

### Media

- [Hard Disk Drive (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive)
- [How HDD Works](https://www.youtube.com/watch?v=Ep-yM894mQQ) (Video)
- [The Development of HDD Technique](https://www.youtube.com/watch?v=wteUW2sL7bc) (Video)
- [Solid-State Drive (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive)
- [Coding for SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/)
- [How Flash Memory Works](https://www.youtube.com/watch?v=s7JLXs5es7I) (Video)

### Interface

- [A History of PC Buses - From ISA to PCI Express](https://www.youtube.com/watch?v=qla-5isbK60) (Video)
- [Small Computer System Interface (SCSI)](https://en.wikipedia.org/wiki/SCSI)
- [Serial Attached SCSI (SAS)](https://en.wikipedia.org/wiki/Serial_Attached_SCSI)
- [Understanding SCSI](https://www.youtube.com/watch?v=pR7SdrXdT4M) (Video)
- [AT Atachment (ATA)](https://en.wikipedia.org/wiki/Parallel_ATA)
- [Serial AT Attachment (SATA)](https://en.wikipedia.org/wiki/Serial_ATA)
- [Advanced Host Controller Interface (AHCI)](https://en.wikipedia.org/wiki/Advanced_Host_Controller_Interface)
- [Peripheral Component Interconnect (PCI)](https://en.wikipedia.org/wiki/Conventional_PCI)
- [PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express)
- [NVM Express (NVMe)](https://en.wikipedia.org/wiki/NVM_Express)

## Operating System

### Kernel

- [Understanding the Linux Kernel](https://www.oreilly.com/library/view/understanding-the-linux/0596005652/)
- [Understanding the Linux Virtual Memory Manager](https://www.kernel.org/doc/gorman/)
- [Linux Device Drivers](https://www.oreilly.com/library/view/linux-device-drivers/0596005903/)

- [The Slab Allocator: An Object-Caching Kernel Memory Allocator](papers/slab.pdf) (1994)

  This paper presents a comprehensive design overview of the SunOS 5.4 kernel memory allocator. This allocator is based on a set of object-caching primitives that reduce the cost of allocating complex objects by retaining their state between uses.

### File system

- [ext4 Data Structures and Algorithms](https://www.kernel.org/doc/html/latest/filesystems/ext4/index.html)

- [The Design and Implementation of a Log-Structured File System](papers/lfs.pdf) (1991)

  This paper presents a new technique for disk storage management called a log-structured file system. A log- structured file system writes all modifications to disk sequentially in a log-like structure, thereby speeding up both file writing and crash recovery.

- [SFS: Random Write Considered Harmful in Solid State Drives](papers/sfs.pdf) (2012)

  In this paper, we propose a new file system for SSDs, SFS. First, SFS exploits the maximum write bandwidth of SSD by taking a log-structured approach. SFS transforms all random writes at file system level to sequential ones at SSD level. Second, SFS takes a new data grouping strategy on writing, instead of the existing data separation strategy on segment cleaning. It puts the data blocks with similar update likelihood into the same segment. This minimizes the inevitable segment cleaning overhead in any log-structured file system by allowing the segments to form a sharp bimodal distribution of segment utilization.

### Modern hardware

- [What Every Programmer Should Know About Memory](papers/cpumemory.pdf) (2007)

  This paper explains the structure of memory subsystems in use on modern commodity hardware, illustrating why CPU caches were developed, how they work, and what programs should do to achieve optimal performance by utilizing them.

- [What Every Systems Programmer Should Know About Concurrency](papers/concurrency.pdf) (2018)

  Seasoned programmers are familiar with tools like mutexes, semaphores, and condition variables. But what makes them work? How do we write concurrent code when we can’t use them, like when we’re working below the operating system in an embedded environment, or when we can’t block due to hard time constraints? And since your system transforms your code into things you didn’t write, running in orders you never asked for, how do multithreaded programs work at all? Concurrency — especially on modern hardware — is a complicated and unintuitive topic, but let’s try to cover some fundamentals.

- [Everything You Always Wanted to Know About Synchronization but Were Afraid to Ask](papers/synchronization.pdf) (2013)

  This paper presents the most exhaustive study of synchronization to date. We span multiple layers, from hardware cache-coherence protocols up to high-level concurrent software. We do so on different types of architectures, from single-socket – uniform and non- uniform – to multi-socket – directory and broadcast-based – many-cores.

### Storage virtualization

- [Logical volume management](https://en.wikipedia.org/wiki/Logical_volume_management)
- [Logical Volume Management (LVM) - Linux](https://www.youtube.com/watch?v=fadQX2e_PGk) (Video)
- [Redundant Array of Independent Disks (RAID)](https://en.wikipedia.org/wiki/RAID)
- [What is RAID 0, 1, 2, 3, 4, 5, 6 and 10 (1+0)?](https://www.youtube.com/watch?v=wTcxRObq738) (Video)

## Storage Engine

- [The Five-Minute Rule for Trading Memory for Disc Accesses](papers/five-minute-rule-1987.pdf) (1987)
- [The Five-Minute Rule 10 Years Later, and Other Computer Storage Rules of Thumb](papers/five-minute-rule-1997.pdf) (1997)
- [The Five-Minute Rule 20 Years Later, and How Flash Memory Changes the Rules](papers/five-minute-rule-2007.pdf) (2007)
- [The Five-Minute Rule 30 Years Later, and its Impact on the Storage Hierarchy](papers/five-minute-rule-2017.pdf) (2017)

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/lsmtree.pdf) (1996)

  This paper presents the Log-Structured Merge-tree (LSM-tree), a disk-based data structure designed to provide low-cost indexing for a file experiencing a high rate of record inserts (and deletes) over an extended period. The LSM-tree uses an algorithm that defers and batches index changes, cascading the changes from a memory-based component through one or more disk components in an efficient manner reminiscent of merge sort.

- [Weaving Relations for Cache Performance](papers/pax.pdf) (2001)

  This paper presents a new data organization model, Partition Attributes Across (PAX), that significantly improves cache performance by grouping together all values of each attribute within each page.

- [Cache-Oblivious Streaming B-trees](papers/streaming-btree.pdf) (2007)

  This paper presents two cache-oblivious streaming B-trees, the shuttle tree, and the cache-oblivious lookahead array (COLA).

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/bitcask.pdf) (2010)

- [bLSM: A General Purpose Log Structured Merge Tree](papers/blsm.pdf) (2012)

  This paper presents bLSM, a Log Structured Merge (LSM) tree with the advantages of B-Trees and log structured approaches. bLSM uses Bloom filters to improve index performance and uses spring and gear scheduler to avoid long write pauses.

- [The Adaptive Radix Tree: ARTful Indexing for Main-Memory Databases](papers/adaptive-radix-tree.pdf) (2013)

  This paper presents ART, an adaptive radix tree (trie) for efficient indexing in main memory. Its lookup performance surpasses highly tuned, read-only search trees, while supporting very efficient insertions and deletions as well. At the same time, ART is very space efficient and solves the problem of excessive worst-case space consumption, which plagues most radix trees, by adaptively choosing compact and efficient data structures for internal nodes.

- [The Bw-Tree: A B-tree for New Hardware Platforms](papers/bw-tree.pdf) (2013)

  This paper presents Bw-Tree, a new form of B-Tree that achieves its very high performance via a latch-free approach that effectively exploits the processor caches of modern multi-core chips.

- [LLAMA: A Cache/Storage Subsystem for Modern Hardware](papers/llama.pdf) (2013)

  LLAMA is a subsystem designed for new hardware environments that supports an API for page-oriented access methods, providing both cache and storage management.

- [Hekaton: SQL Server’s Memory-Optimized OLTP Engine](papers/hekaton.pdf) (2013)

  This paper presents Hekaton, a new database engine optimized for memory resident data and OLTP workloads. Hekaton uses only latch-free data structures and a new optimistic, multiversion concurrency control technique.

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/wisckey.pdf) (2016)

  This paper presents WiscKey, a persistent LSM-Tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification.

- [PebblesDB: Building Key-Value Stores using Fragmented Log-Structured Merge Trees](papers/pebblesdb.pdf) (2017)

  This paper presents a novel data structure that is inspired by Skip Lists, termed Fragmented Log-Structured Merge Trees (FLSM). FLSM introduces the notion of guards to organize logs, and avoids rewriting data in the same level.

- [TinyLFU: A Highly Efficient Cache Admission Policy](papers/tinylfu.pdf) (2017)

  This article proposes to use a frequency-based cache admission policy in order to boost the effectiveness of caches subject to skewed access distributions. Given a newly accessed item and an eviction candidate from the cache, our scheme decides, based on the recent access history, whether it is worth admitting the new item into the cache at the expense of the eviction candidate.

- [Monkey: Optimal Navigable Key-Value Store](papers/monkey.pdf) (2017)

  This paper presents Monkey, an LSM-based key-value store that strikes the optimal balance between the costs of updates and lookups with any given main memory budget. The insight is that worst-case lookup cost is proportional to the sum of the false positive rates of the Bloom filters across all levels of the LSM-tree. Contrary to state-of-the-art key-value stores that assign a fixed number of bits-per-element to all Bloom filters, Monkey allocates memory to filters across different levels so as to minimize this sum.

- [Dostoevsky: Better Space-Time Trade-Offs for LSM-Tree Based Key-Value Stores via Adaptive Removal of Superfluous Merging](papers/dostoevsky.pdf) (2018)

  We introduce Lazy Leveling, a new design that removes merge operations from all levels of LSM-tree but the largest. Lazy Leveling improves the worst-case complexity of update cost while maintaining the same bounds on point lookup cost, long range lookup cost, and storage space. We further introduce Fluid LSM-tree, a generalization of the entire LSM-tree design space that can be parameterized to assume any existing design.

- [The Log-Structured Merge-Bush & the Wacky Continuum](papers/wackyandthebush.pdf) (2019)

  We introduce the Log-Structured Merge-Bush (LSM-Bush), a new data structure that sets increasing capacity ratios between adjacent pairs of smaller levels. We further introduce Wacky, a design continuum that includes LSM-Bush as well as all state-of-the-art merge policies, from laziest to greediest, and can assume any of them within a single implementation.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/datacalculator.pdf) (2018)

- [Faster: A Concurrent Key-Value Store with In-Place Updates](papers/faster.pdf) (2018)

- [LSM-based storage techniques: a survey](papers/lsmsurvey.pdf) (2019)

  In this paper, we provide a survey of recent research efforts on LSM-trees so that readers can learn the state of the art in LSM-based storage techniques. We provide a general taxonomy to classify the literature of LSM-trees, survey the efforts in detail, and discuss their strengths and trade-offs. We further survey several representative LSM-based open-source NoSQL systems and discuss some potential future research directions resulting from the survey.

- [X-Engine: An Optimized Storage Engine for Large-scale E-commerce Transaction Processing](papers/xengine.pdf) (2019)

- [MyRocks: LSM-Tree Database Storage Engine Serving Facebook's Social Graph](papers/myrocks.pdf) (2020)

- [The Case for Learned Index Structures](papers/learned-index.pdf) (2018)

- [The PGM-index: a fully-dynamic compressed learned index with provable worst-case bounds](papers/pgm-index.pdf) (2020)

## SQL

- [Access Path Selection in a Relational Database Management System](papers/systemr.pdf) (1979)

  This paper presents a cost-based SQL optimizer in System R. The optimizer estimates the cost of access paths in terms of I/O and CPU costs, using statistics about the contents of each relation.

- [The Volcano Optimizer Generator: Extensibility and Efficient Search](papers/volcano.pdf) (1993)

  This paper presents an optimizer generator that translates a model specification into an optimizer source code. It also provides a search engine to be used in all generated optimizers. The search engine is goal-oriented using directed dynamic programming search algorithms.

- [The Cascades Framework for Query Optimization](papers/cascades.pdf) (1995)

- [How We Built a Cost-Based SQL Optimizer](https://www.cockroachlabs.com/blog/building-cost-based-sql-optimizer/) (2018)
- [How We Built a Vectorized SQL Engine](https://www.cockroachlabs.com/blog/how-we-built-a-vectorized-sql-engine/) (2019)

## Transaction

- [Granularity of Locks and Degrees of Consistency in a Shared Data Base](papers/locks.pdf) (1975)

  The first part of this paper introduces a locking protocol that allows simultaneous locking at various granularities in a database with a hierarchical structure. The second part of this paper introduces four degrees of consistency and the relationships of the four degrees to the locking protocol.

- [The Notion of Consistency and Predicate Locks in a Database System](papers/predicate-locks.pdf) (1976)

  This paper proofs that two-phase locking (2PL) guarantees serializability and introduces predicate locks to address the problem of phantom reads.

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/logical-clocks.pdf) (1978)

  This paper discusses the partial ordering defined by the "happened before" relation, and gives a distributed algorithm for extending it to a consistent total ordering of all the events.

- [How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Progranm](papers/sequential-consistency.pdf) (1979)

  This paper defines the condition of sequential consistency and describes a method to ensure the sequential consistency of interconnecting sequential processors with memory modules.

- [Linearizability: A Correctness Condition for Concurrent Objects](papers/linearizability.pdf) (1990)

  This paper defines the condition of linearizability and discusses the differences between it and other correctness conditions.

- [Session Guarantees for Weakly Consistent Replicated Data](papers/session-guarantees.pdf) (1994)

  This paper proposes four per-session guarantees to aid users and applications of weakly consistent replicated data: Read Your Writes, Monotonic Reads, Writes Follow Reads, and Monotonic Writes.

- [Causal Memory: Definitions, Implementation and Programming](papers/causal-consistency.pdf) (1995)

  This paper defines the condition of causal consistency based on Lamport's "happened before" relation.

- [A Critique of ANSI SQL Isolation Levels](papers/ansi-isolation.pdf) (SIGMOD, 1995)

  This paper analyzes the ambiguities of ANSI isolation levels and provides clearer phenomena definitions. It also presents a new MVCC isolation level called snapshot isolation. A transaction in snapshot isolation reads data from a snapshot of the committed data as of the time the transaction started, and checks for write-write conflicts.

- [Generalized Isolation Level Definitions](papers/generalized-isolation.pdf) (2000)

  This paper proposes a graph-based approach to define existing ANSI isolation levels.

- [Serializable Isolation for Snapshot Databases](papers/serializable-snapshot-isolation.pdf) (2008)

  This paper presents an algorithm to achieve serializable snapshot isolation based on anti-dependencies detection.

- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](papers/percolator.pdf) (2010)

  This paper presents Percolator, an incremental update processing system built on top of Bigtable. Percolator provides snapshot isolation transactions using a two-phase commit protocol.

- [A Critique of Snapshot Isolation](papers/snapshot-isolation.pdf) (2012)

  This paper presents a new MVCC isolation level called write-snapshot isolation. A transaction in write-snapshot isolation checks for read-write conflicts instead of write-write conflicts in snapshot isolation.

- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](papers/calvin.pdf) (2012)

  This paper presents Calvin, a practical transaction scheduling and data replication layer that uses a deterministic ordering guarantee to significantly reduce the normally prohibitive contention costs associated with distributed transactions.

- [Highly Available Transactions: Virtues and Limitations](papers/highly-available-transactions.pdf) (2013)

  This paper introduces a taxonomy of highly available systems and analyze existing ACID isolation and distributed data consistency guarantees to identify which can and cannot be achieved in HAT systems.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/hybrid-logical-clocks.pdf) (2014)

  This paper proposes a hybrid logical clock, HLC, that combines the best of logical clocks and physical clocks.

- [Linearizability versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/) (2014)

- [Consistency in Non-Transactional Distributed Storage Systems](papers/consistency-overview.pdf) (2016)

  This paper provides a structured and comprehensive overview of different consistency notions and provide a partial order among different consistency predicates.

- [SLOG: Serializable, Low-latency, Geo-replicated Transactions](papers/slog.pdf) (2019)

  This paper presents SLOG, a system that provides strictly serializable ACID transactions at geo-replicated distance. SLOG achieves high-throughtput and low latency for transactions that initiate from a location close to the home region for data they access.

- [Transactional Causal Consistency for Serverless Computing](papers/transactional-causal-consistency.pdf) (2020)

- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html) (2017)
- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html) (2018)
- [Consistency without Clocks: The FaunaDB Distributed Transaction Protocol](https://fauna.com/blog/consistency-without-clocks-faunadb-transaction-protocol) (2018)
- [Demystifying Database Systems, Part 1: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels) (2019)
- [Demystifying Database Systems, Part 2: Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation) (2019)
- [Demystifying Database Systems, Part 3: Introduction to Consistency Levels](https://fauna.com/blog/demystifying-database-systems-introduction-to-consistency-levels) (2019)
- [Demystifying Database Systems, Part 4: Isolation levels vs. Consistency levels](https://fauna.com/blog/demystifying-database-systems-part-4-isolation-levels-vs-consistency-levels) (2019)

## Distributed algorithm

- [Paxos Made Simple](papers/paxos-made-simple.pdf) (2001)

  The Paxos algorithm, when presented in plain English, is very simple.

- [Consensus on Transaction Commit](papers/paxos-commit.pdf) (2004)

  This paper presents the Paxos Commit algorithm. Paxos Commit runs a Paxos consensus algorithm on the commit/abort decision of each participant to obtain a transaction commit protocol that uses 2F + 1 coordinators and makes progress if at least F + 1 of them are working properly.

- [Paxos Made Live - An Engineering Perspective](papers/paxos-made-live.pdf) (2007)

  This paper presents the experience of building Chubby, a fault-tolerant storage system using the Paxos consensus algorithm.

- [There Is More Consensus in Egalitarian Parliaments](papers/epaxos.pdf) (2013)

  This paper presents the design and implementation of Egalitarian Paxos (EPaxos), a new distributed consensus algorithm based on Paxos that achieves uniform load balancing across all replicas.

- [Paxos Quorum Leases: Fast Reads Without Sacrificing Writes](papers/paxos-quorum-leases.pdf) (2014)

  This paper presents quorum leases, a technique that allows Paxos-based systems to perform consistent local reads on multiple replicas.

- [In Search of an Understandable Consensus Algorithm](papers/raft.pdf) (2014)

  This paper presents Raft, a consensus algorithm for managing a replicated log. Raft produces a result equivalent to Paxos, and it is as efficient as Paxos, but its structure is different from Paxos. Raft is more understandable than Paxos and also provides a better foundation for building practical systems.

- [Weighted Voting for Replicated Data](papers/quorum.pdf) (1979)

  In a new algorithm for maintaining replicated data, every copy of a replicated file is assigned some number of votes. Every transaction collects a read quorum of r votes to read a file, and a write quorum of w votes to write a file, such that r+ w is greater than the total number of votes assigned to the file.

- [Chain Replication for Supporting High Throughput and Availability](papers/chain-replication.pdf) (2004)

  Chain replication is a new approach to coordinating clusters of fail-stop storage servers. The approach is intended for supporting large-scale storage services that exhibit high throughput and availability with-out sacrificing strong consistency guarantees.

- [Conflict-free Replicated Data Types](papers/crdt.pdf) (2011)

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/cap-therom.pdf) (2002)

  This paper proves the CAP conjecture in the asynchronous network model, and then discusses solutions to this dilemma in the partially synchronous model.

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)

## Distributed System

### Papers

- [An Opportunity Cost Approach for Job Assignment in a Scalable Computing Cluster](papers/distributed-system/epvm.pdf) (2000)

- [The Google File System](papers/distributed-system/gfs-sosp03.pdf) (SOSP, 2003)

  This paper presents the Google File System, a scalable distributed file system
  for large distributed data-intensive applications.

- [Bigtable: A Distributed Storage System for Structured Data](papers/distributed-system/bigtable-osdi06.pdf) (OSDI, 2006)

  This paper presents Bigtable, a distributed storage system for managing
  structured data that is designed to scale to a very large size.

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/distributed-system/dynamo-sosp07.pdf) (SOSP, 2007)

  This paper presents the design and implementation of Dynamo, a highly
  available key-value storage system that some of Amazon's core services use to
  provide an “always-on” experience.

- [Finding a needle in Haystack: Facebook’s photo storage](papers/distributed-system/haystack-osdi10.pdf) (OSDI, 2010)

- [f4: Facebook’s Warm BLOB Storage System](papers/distributed-system/f4-osdi14.pdf) (OSDI, 2014)

- [Large-scale cluster management at Google with Borg](papers/distributed-system/borg.pdf) (EuroSys, 2015)

- [Sharding the Shards: Managing Datastore Locality at Scale with Akkio](papers/distributed-system/akkio.pdf) (OSDI, 2018)

  In this paper we present Akkio, a locality management service for distributed
  datastore systems whose aim is to improve data access response times and to
  reduce cross-datacenter bandwidth usage as well as the total amount of storage
  capacity needed.

- [Anna: A KVS for Any Scale](papers/distributed-system/anna-ieee18.pdf) (ICDE, 2018)

- [Autoscaling Tiered Cloud Storage in Anna](papers/distributed-system/anna-vldb19.pdf) (VLDB, 2019)

- [DistCache: Provable Load Balancing for Large-Scale Storage Systems with Distributed Caching](papers/distributed-system/distcache-fast19.pdf) (FAST, 2019)

- [Virtual Consensus in Delos](papers/distributed-system/delos-osdi20.pdf) (OSDI, 2020)

## OLTP Database

### Papers

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/oltp-database/megastore-cidr11.pdf) (CIDR, 2011)

  This paper presents Megastore, a storage system that blends the scalability of
  a NoSQL datastore with the convenience of a traditional RDBMS in a novel way,
  and provides both strong consistency guarantees and high availability.

- [Spanner: Google’s Globally-Distributed Database](papers/oltp-database/spanner-osdi12.pdf) (OSDI, 2012)

  This paper presents Spanner, a scalable, multi-version, globally-distributed,
  and synchronously-replicated database.

- [F1: A Distributed SQL Database That Scales](papers/oltp-database/f1-vldb13.pdf) (VLDB, 2013)

  This paper presents F1, a hybrid database that combines high availability, the
  scalability of NoSQL systems like Bigtable, and the consistency and usability
  of traditional SQL databases. F1 is built on Spanner, which provides
  synchronous cross-datacenter replication and strong consistency.

- [Online, Asynchronous Schema Change in F1](papers/oltp-database/f1-schema-vldb13.pdf) (VLDB, 2013)

  This paper describes a protocol for schema evolution in a globally
  distributed database management system with shared data, stateless servers,
  and no global membership.

- [Spanner: Becoming a SQL System](papers/oltp-database/spanner-sigmod17.pdf) (SIGMOD, 2017)

  This paper highlights the database DNA of Spanner. It describes distributed
  query execution in the presence of resharding, query restarts upon transient
  failures, range extraction that drives query routing and index seeks, and the
  improved blockwise-columnar storage format.

- [Amazon Aurora: Design Considerations for High Throughput Cloud-Native Relational Databases](papers/oltp-database/aurora-sigmod17.pdf) (SIGMOD, 2017)

- [Amazon Aurora: On Avoiding Distributed Consensus for I/Os, Commits, and Membership Changes](papers/oltp-database/aurora-sigmod18.pdf) (SIGMOD, 2018)

- [Socrates: The New SQL Server in the Cloud](papers/oltp-database/socrates-sigmod19.pdf) (SIGMOD, 2019)

- [CockroachDB: The Resilient Geo-Distributed SQL Database](papers/oltp-database/cockroachdb-sigmod20.pdf) (SIGMOD, 2020)

  This paper presents the design of CockroachDB and its novel transaction model
  that supports consistent geo-distrib- uted transactions on commodity hardware.

- [TiDB: A Raft-based HTAP Database](papers/oltp-database/tidb-vldb20.pdf) (VLDB, 2020)

### Links

- [How CockroachDB Does Distributed, Atomic Transactions](https://www.cockroachlabs.com/blog/how-cockroachdb-distributes-atomic-transactions/) (Cockroach Labs, 2015)
- [How online schema changes are possible in CockroachDB](https://www.cockroachlabs.com/blog/how-online-schema-changes-are-possible-in-cockroachdb/) (Cockroach Labs, 2016)
- [Living Without Atomic Clocks](https://www.cockroachlabs.com/blog/living-without-atomic-clocks/) (Cockroach Labs, 2016)
- [Serializable, Lockless, Distributed: Isolation in CockroachDB](https://www.cockroachlabs.com/blog/serializable-lockless-distributed-isolation-cockroachdb/) (Cockroach Labs, 2016)
- [CockroachDB’s Consistency Model](https://www.cockroachlabs.com/blog/consistency-model/) (Cockroach Labs, 2019)

## OLAP Database

### Papers

- [C-Store: A Column-oriented DBMS](papers/olap-database/c-store-vldb05.pdf) (VLDB, 2005)

  This paper presents the design of a read-optimized relational DBMS that stores
  data by column.

- [MonetDB/X100: Hyper-Pipelining Query Execution](papers/olap-database/monetdb-cidr05.pdf) (CIDR, 2005)

  This paper presents a CPU efficient query processor that employs a vectorized
  query processing model. The processor uses loop-pipelined and cache-conscious
  operations to take advantage of modern CPUs.

- [Dremel: Interactive Analysis of Web-Scale Datasets](papers/olap-database/dremel-vldb10.pdf) (VLDB, 2010)

- [The Snowflake Elastic Data Warehouse](papers/olap-database/snowflake-sigmod16.pdf) (SIGMOD, 2016)

- [AnalyticDB: Real-time OLAP Database System at Alibaba Cloud](papers/olap-database/analyticdb-vldb19.pdf) (VLDB, 2019)

- [Procella: Unifying serving and analytical data at YouTube](papers/olap-database/procella-vldb19.pdf) (VLDB, 2019)

- [Alibaba Hologres: A Cloud-Native Service for Hybrid Serving/Analytical Processing](papers/olap-database/hologres-vldb20.pdf) (VLDB, 2020)

### Books

- [The Design and Implementation of Modern Column-Oriented Database Systems](papers/olap-database/modern-column-stores.pdf) (2013)

  This book discusses modern column-stores, their architecture and evolution as
  well the benefits they can bring in data analytics. There is a specific focus
  on three influential research prototypes, MonetDB, MonetDB/X100, and C-Store.

## Miscellaneous

### Papers

- [What Goes Around Comes Around](papers/miscellaneous/what-goes-around-comes-around.pdf) (2005)

- ["One Size Fits All": An Idea Whose Time Has Come and Gone](papers/miscellaneous/one-size-fits-all.pdf) (ICDE, 2005)

- [The Seattle Report on Database Research](papers/miscellaneous/the-seattle-report-sigmod19.pdf) (SIGMOD, 2019)

### Books

- [Readings in Database Systems](http://www.redbook.io/)

- [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/)

### Links

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) (2013)

- [How does a relational database work](http://coding-geek.com/how-databases-work/) (2015)

- [Elements Of Scale: Composing And Scaling Data Platforms](http://www.benstopford.com/2015/04/28/elements-of-scale-composing-and-scaling-data-platforms/) (2015)

- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) (2015)

- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/) (2016)
