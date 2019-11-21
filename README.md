# About

You want to become an awesome database developer?

Great, that's fun but challenging. Don't panic, I collect some awesome materials here for us.

# SQL

## Schema

### Papers

- [Online, Asynchronous Schema Change in F1](papers/sql/F1-Schema.pdf) (VLDB, 2013)

  Introduces a protocol for asynchronous schema changes in distributed
  databases. The protocol executes a schema change in intermediate states and
  ensures that the transitions between these states are *consistency
  preserving*.

### Posts

- [How online schema changes are possible in CockroachDB](https://www.cockroachlabs.com/blog/how-online-schema-changes-are-possible-in-cockroachdb/) (Cockroach Labs, 2016)

## Optimizer

### Papers

- [Access Path Selection in a Relational Database Management System](papers/sql/SystemR.pdf) (SIGMOD, 1979)

  Introduces a cost-based SQL optimizer in System R. The optimizer estimates
  the cost of access paths in terms of I/O and CPU costs, using statistics about
  the contents of each relation.

- [The Volcano Optimizer Generator: Extensibility and Efficient Search](papers/sql/Volcano.pdf) (ICDE, 1993)

  Introduces an optimizer generator that translates a model specification into
  optimizer source code. It also provides a search engine to be used in all
  generated optimizers. The search engine is goal-oriented using *directed
  dynamic programming* search algorithms.

### Posts

- [How We Built a Cost-Based SQL Optimizer](https://www.cockroachlabs.com/blog/building-cost-based-sql-optimizer/) (Cockroach Labs, 2018)

## Execution

### Papers

- [MonetDB/X100: Hyper-Pipelining Query Execution](papers/sql/MonetDB.pdf) (CIDR, 2005)

  Introduces a CPU efficient query processor that employs a *vectorized* query
  processing model. The processor uses *loop-pipelined* and *cache-conscious*
  operations to take advantage of modern CPUs.

### Posts

- [How We Built a Vectorized SQL Engine](https://www.cockroachlabs.com/blog/how-we-built-a-vectorized-sql-engine/) (Cockroach Labs, 2019)

# Storage Devices

I have put up a post to explain these things: [What You Should Know About Storage Devices](http://huachaohuang.com/2019/08/28/what-you-should-know-about-storage-devices.html)

## Storage Media

### HDD

#### Wikis

- [Magnetic Storage](https://en.wikipedia.org/wiki/Magnetic_storage)
- [Hard Disk Drive (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive)

#### Videos

- [How HDD Works](https://www.youtube.com/watch?v=Ep-yM894mQQ)
- [The Mechanical Structure of HDD](https://www.youtube.com/watch?v=NtPc0jI21i0)
- [The Development of HDD Technique](https://www.youtube.com/watch?v=wteUW2sL7bc)

### SSD

#### Wikis

- [Flash Memory](https://en.wikipedia.org/wiki/Flash_memory)
- [Solid-State Drive (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive)

#### Posts

- [Coding for SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/)

#### Videos

- [How Flash Memory Works](https://www.youtube.com/watch?v=s7JLXs5es7I)

## Storage Standards

### SCSI

#### Wikis

- [Small Computer System Interface (SCSI)](https://en.wikipedia.org/wiki/SCSI)
- [Parallel SCSI](https://en.wikipedia.org/wiki/Parallel_SCSI)
- [Serial Attached SCSI (SAS)](https://en.wikipedia.org/wiki/Serial_Attached_SCSI)

#### Videos

- [Understanding SCSI](https://www.youtube.com/watch?v=pR7SdrXdT4M)

### ATA

#### Wikis

- [AT Atachment (ATA)](https://en.wikipedia.org/wiki/Parallel_ATA)
- [Serial AT Attachment (SATA)](https://en.wikipedia.org/wiki/Serial_ATA)
- [Advanced Host Controller Interface (AHCI)](https://en.wikipedia.org/wiki/Advanced_Host_Controller_Interface)

### PCI

#### Wikis

- [Industry Standard Architecture (ISA)](https://en.wikipedia.org/wiki/Industry_Standard_Architecture)
- [Peripheral Component Interconnect (PCI)](https://en.wikipedia.org/wiki/Conventional_PCI)
- [PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express)
- [Non-Volatile Memory (NVM)](https://en.wikipedia.org/wiki/Non-volatile_memory)
- [NVM Express (NVMe)](https://en.wikipedia.org/wiki/NVM_Express)

#### Videos

- [A History of PC Buses - From ISA to PCI Express](https://www.youtube.com/watch?v=qla-5isbK60)

# Storage Virtualization

## Multiple Devices Management

### LVM

#### Wikis

- [Logical Volume Manager (LVM)](https://en.wikipedia.org/wiki/Logical_Volume_Manager_(Linux))

#### Videos

- [Logical Volume Management (LVM) - Linux](https://www.youtube.com/watch?v=fadQX2e_PGk)

### RAID

#### Wikis

- [Redundant Array of Independent Disks (RAID)](https://en.wikipedia.org/wiki/RAID)

#### Videos

- [What is RAID 0, 1, 2, 3, 4, 5, 6 and 10 (1+0)?](https://www.youtube.com/watch?v=wTcxRObq738)

# Storage System

## Storage Engine

### Papers

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/storage-system/lsm.pdf) (1996)
  > Introduce *LSM-Tree*, a new data structure that defers and batches index changes, cascades the changes from a memory-based component through one or more disk components in an efficient manner reminiscent of merge sort.

- [Weaving Relations for Cache Performance](papers/storage-system/pax.pdf) (2001)
  > Introduce a new data organization model called *Partition Attributes Across (PAX)* that significantly improves cache performance by grouping together all values of each attribute within each page.

- [C-Store: A Column-oriented DBMS](papers/storage-system/c-store.pdf) (2005)

- [Cache-Oblivious Streaming B-trees](papers/storage-system/streaming-btree.pdf) (2007)
  > Introduce two *cache-oblivious streaming B-trees* that efficiently implements insertions and range queries.

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/storage-system/bitcask.pdf) (2010)

- [bLSM: A General Purpose Log Structured Merge Tree](papers/storage-system/blsm.pdf) (2012)
  > Introduce *bLSM*, a new form of LSM-Tree with the advantages of B-Trees and log structured approaches.

- [The Bw-Tree: A B-tree for New Hardware Platforms](papers/storage-system/bw-tree.pdf) (2013)
  > Introduce *Bw-Tree*, a new form of B-Tree that achieves its very high performance via a latch-free approach that effectively exploits the processor caches of modern multi-core chips.

- [Hekaton: SQL Server’s Memory-Optimized OLTP Engine](papers/storage-system/hekaton.pdf) (2013)

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/storage-system/wisckey.pdf) (2016)
  > Introduce *WiscKey*, a persistent LSM-Tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/storage-system/data-calculator.pdf) (2018)
  > Introduce the *Data Calculator*, a design engine that enables interactive and semi-automated design of data structures.

## Relational Database

### Articles

- [How does a relational database work](http://coding-geek.com/how-databases-work/)

# Operating System

## Linux Kernel

### Books

- [Understanding the Linux Kernel](https://www.oreilly.com/library/view/understanding-the-linux/0596005652/)
- [Linux Device Drivers](https://www.oreilly.com/library/view/linux-device-drivers/0596005903/)

### Papers

- [What Every Programmer Should Know About Memory](papers/operating-system/cpumemory.pdf)
- [What Every Systems Programmer Should Know About Concurrency](papers/operating-system/concurrency-primer.pdf)
- [The Slab Allocator: An Object-Caching Kernel Memory Allocator](papers/operating-system/slab-allocator.pdf)

### Websites

- [The Linux Kernel Archives](https://www.kernel.org/)
- [Linux Weekly News](https://lwn.net/)

# Distributed System

## Clock

### Papers

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/distributed-system/logical-clock.pdf) (1978)
  > Propose a distributed algorithm to synchronize a system of logical clocks, which can be used to totally order the events.

- [Practical Uses of Synchronized Clocks in Distributed Systems](papers/distributed-system/synchronized-clock.pdf) (1993)
  > Discuss a number of distributed algorithms that make use of synchronized clocks and analyzes how clocks are used in these algorithms.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/distributed-system/hybrid-logical-clock.pdf) (2014)
  > Propose a hybrid logical clock, HLC, that combines the best of logical clocks and physical clocks.

## Consensus

### Papers

- [The Part-Time Parliament](papers/distributed-system/paxos.pdf) (1998)
  > Propose the Paxos algorithm.

- [Paxos Made Simple](papers/distributed-system/paxos-made-simple.pdf) (2001)
  > Present the Paxos algorithm in plain English.

- [Fast Paxos](papers/distributed-system/fast-paxos.pdf) (2005)
  > Propose an extension of the classic Paxos algorithm that allows the value to be learned in two message delays.

- [Paxos Made Live - An Engineering Perspective](papers/distributed-system/paxos-made-live.pdf) (2007)
  > Describe the experience building a fault-tolerant database using the Paxos consensus algorithm.

- [There Is More Consensus in Egalitarian Parliaments](papers/distributed-system/epaxos.pdf) (2013)
  > Describe the design and implementation of Egalitarian Paxos (EPaxos), a new distributed consensus algorithm based on Paxos.

- [Paxos Quorum Leases: Fast Reads Without Sacrificing Writes](papers/distributed-system/paxos-lease.pdf) (2014)
  > Describe quorum leases, a new technique that allows Paxos-based systems to perform reads with high throughput and low latency.

- [In Search of an Understandable Consensus Algorithm](papers/distributed-system/raft.pdf) (2014)
  > Propose the Raft algorithm, which is as efficient as Paxos but more understandable and provides a better foundation for building practical systems.

### Articles

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) (2013)

- [Neat Algorithms - Paxos](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/) (2014)

- [Implementing Replicated Logs with Paxos](https://ramcloud.stanford.edu/~ongaro/userstudy/paxos.pdf)

## Consistency

### Papers

- [How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Progranm](papers/distributed-system/sequential-consistency.pdf) (1979)
  > Define *sequential consistency* that guarantees the sequential ordering of operations.

- [Linearizability: A Correctness Condition for Concurrent Objects](papers/distributed-system/linearizability.pdf) (1990)
  > Define *linearizability* that guarantees the sequential and "real-time" precedence ordering of operations.

- [Session Guarantees for Weakly Consistent Replicated Data](papers/distributed-system/session-guarantees.pdf) (1994)
  > Define *session guarantees*: *Read Your Writes*, *Monotonic Reads*, *Writes Follow Reads*, and *Monotonic Writes*.

- [Causal Memory: Definitions, Implementation and Programming](papers/distributed-system/causal-consistency.pdf) (1995)
  > Define *causal consistency* that guarantees the relative ordering of operations that are *causally related*.

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/distributed-system/cap-theorem.pdf) (2002)
  > Prove the *CAP conjecture* that it is impossible to provide all the three properties: *Consistency*, *Availability*, and *Partition-tolerance*.

- [Eventually Consistent](papers/distributed-system/eventual-consistency.pdf) (2009)
  > Define *eventual consistency* that guarantees if no new updates are made to the object, eventually all accesses will return the last updated value.

- [Consistency in Non-Transactional Distributed Storage Systems](papers/distributed-system/distributed-consistency.pdf) (2016)
  > Overview more than 50 different consistency notions and provie a partial order among them.

### Articles

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)
  > Revisit the *CAP theorem* to maximize the combinations of consistency and availability.

# Distributed Storage

## File System

### Papers

- [The Google File System](papers/distributed-storage/gfs.pdf) (2003)

## Storage System

### Papers

- [Bigtable: A Distributed Storage System for Structured Data](papers/distributed-storage/bigtable.pdf) (2006)

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/distributed-storage/dynamo.pdf) (2007)
  > Introduce *Dynamo*, an *eventually-consistent* storage system that partitions and replicates data using *consistent hashing*.

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/distributed-storage/megastore.pdf) (2011)
  > Introduce *Megastore*, a NoSQL storage system that provides serializable ACID semantics within fine-grained partitions of data.

### Articles

- [Elements Of Scale: Composing And Scaling Data Platforms](http://highscalability.com/blog/2015/5/4/elements-of-scale-composing-and-scaling-data-platforms.html) (2015)

- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) (2015)

# Distributed Database

## Transaction

### Books

- [Concurrency Control and Recovery in Database Systems](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/05/ccontrol.zip)

### Papers

- [The Notion of Consistency and Predicate Locks in a Database System](papers/distributed-database/two-phase-locking.pdf) (1976)
  > Propose *two-phase locking (2PL)* to guarantee serializability and *predicate locks* to prevent *phantom reads*.

- [Granularity of Locks and Degrees of Consistency in a Shared Data Base](papers/distributed-database/degrees-of-isolation.pdf) (1976)
  > Propose multiple granularity of locks and degrees of consistency: *degree 0*, *degree 1 (Read Uncommitted)*, *degree 2 (Read Committed)*, and *degree 3 (Serializable)*.

- [The Serializability of Concurrent Database Updates](papers/distributed-database/serializability-npcomplete.pdf) (1979)
  > Prove the recognition of transaction histories to be serializable is an *NP-complete* problem.

- [Concurrency Control in Distributed Database Systems](papers/distributed-database/serializability-algorithms.pdf) (1981)
  > Describe 48 concurrency control algorithms based on *two-phase locking* and *timestamp ordering*.

- [The Transaction Concept: Virtues and Limitations](papers/distributed-database/transaction-concept.pdf) (1981)
  > Describe the transaction concept and its properties: *Atomicity*, *Consistency* and *Durability*.

- [Principles of Transaction-Oriented Database Recovery](papers/distributed-database/transaction-acid.pdf) (1983)
  > Describe the transaction principles and the *ACID* properties: *Atomicity*, *Consistency*, *Isolation* and *Durability*.

- [A Critique of ANSI SQL Isolation Levels](papers/distributed-database/snapshot-isolation.pdf) (1995)
  > Propose clearer definitions to charaterize existing ANSI isolation levels and a new *snapshot isolation*.

- [Weak Consistency: A Generalized Theory and Optimistic Implementations for Distributed Transactions](papers/distributed-database/generalized-isolation-thesis.pdf) (1999)
  > Propose a graph-based approach to define existing ANSI isolation levels and other widely used levels.
  > Propose two new isolation levels: *Consistent View (PL-2+)* and *Monotonic View (PL-2L)*.

- [Generalized Isolation Level Definitions](papers/distributed-database/generalized-isolation.pdf) (2000)
  > Propose a graph-based approach to define existing ANSI isolation levels.

- [Serializable Isolation for Snapshot Databases](papers/distributed-database/serializable-snapshot-isolation.pdf) (2008)
  > Propose an algorithm to achieve *serializable snapshot isolation* based on *anti-dependencies* detection.

- [A Critique of Snapshot Isolation](papers/distributed-database/write-snapshot-isolation.pdf) (2012)
  > Propose a new *write-snapshot isolation* that is serializable and comparable with *snapshot isolation* in performance.

- [Highly Available Transactions: Virtues and Limitations](papers/distributed-database/highly-available-transactions.pdf) (2014)
  > Introduce a taxonomy of highly available systems and analyze existing ACID isolation and distributed data consistency guarantees to identify which can and cannot be achieved in HAT systems.

### Articles

- [Linearizability versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/) (2014)

## Distributed Transaction

### Papers

- [Consensus on Transaction Commit](papers/distributed-database/paxos-commit.pdf) (2005)
  > Propose the *Paxos Commit* algorithm that runs a Paxos consensus algorithm on the commit/abort decision of each participant for fault-tolerance.

- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](papers/distributed-database/percolator.pdf) (2010)
  > Introduce *Percolator*, an incremental updates processing system that provides transactions with *snapshot isolation*.

- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](papers/distributed-database/calvin.pdf) (2012)
  > Introduce *Calvin*, a practical transaction scheduling and data replication layer that provides a deterministic ordering of distributed transactions.

- [Spanner: Google’s Globally-Distributed Database](papers/distributed-database/spanner.pdf) (2012)
  > Introduce *Spanner*, a globally distributed database that support *externally consistent* transactions using the *TrueTime* API.

- [Spanner, TrueTime and the CAP Theorem](papers/distributed-database/spanner-and-cap-theorem.pdf) (2017)
  > Discuss the techniques behind *Spanner* that make it an "effectively CA" system.

### Articles

- [Living Without Atomic Clocks](https://www.cockroachlabs.com/blog/living-without-atomic-clocks/) (2016)
  > Describe an implementation of *write-snapshot isolation* using *hybrid logical clocks*.

- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html) (2017)
  > Discuss the comparison between *Spanner* and *Calvin*, Part 1.

- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html) (2018)
  > Discuss the comparison between *Spanner* and *Calvin*, Part 2.

- [Consistency without Clocks: The FaunaDB Distributed Transaction Protocol](https://fauna.com/blog/consistency-without-clocks-faunadb-transaction-protocol) (2018)
  > Describe an implementation of *Calvin*.

- [Demystifying Database Systems, Part 1: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels) (2019)
- [Demystifying Database Systems, Part 2: Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation) (2019)
- [Demystifying Database Systems, Part 3: Introduction to Consistency Levels](https://fauna.com/blog/demystifying-database-systems-introduction-to-consistency-levels) (2019)
- [Demystifying Database Systems, Part 4: Isolation levels vs. Consistency levels](https://fauna.com/blog/demystifying-database-systems-part-4-isolation-levels-vs-consistency-levels) (2019)

## Distributed SQL

### Papers

- [F1: A Distributed SQL Database That Scales](papers/distributed-database/f1.pdf) (2013)
  > Introduce *F1*, a hybrid database that combines high availability, the scalability of NoSQL systems like Bigtable, and the consistency and usability of traditional SQL databases.

- [Online, Asynchronous Schema Change in F1](papers/distributed-database/f1-online-ddl.pdf) (2013)
  > Introduce a protocol for schema evolution in a globally distributed database management system with shared data, stateless servers, and no global membership.

- [Spanner: Becoming a SQL System](papers/distributed-database/spanner-2017.pdf) (2017)
  > Introduce the "database system" aspects of *Spanner*, in particular how query execution has evolved and forced the rest of Spanner to evolve.

# Miscellaneous

## General

### Books

- [Readings in Database Systems](http://www.redbook.io/)

### Articles

- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/)
