# About

You want to become an awesome database developer?

Great, that's fun but challenging. Let's collect the awesome materials here to help each other.

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

# Operating System

## Linux Kernel

### Books

- [Understanding the Linux Kernel](https://www.oreilly.com/library/view/understanding-the-linux/0596005652/)
- [Linux Device Drivers](https://www.oreilly.com/library/view/linux-device-drivers/0596005903/)

### Websites

- [The Linux Kernel Archives](https://www.kernel.org/)
- [Linux Weekly News](https://lwn.net/)

# Distributed System

## Clock

### Papers

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/distributed-system/logical-clock.pdf) (1978)
  > Propose *logical clocks (LC)*.

- [Practical Uses of Synchronized Clocks in Distributed Systems](papers/distributed-system/synchronized-clock.pdf) (1993)
  > Discuss a number of distributed algorithms that make use of synchronized clocks and analyzes how clocks are used in these algorithms.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/distributed-system/hybrid-logical-clock.pdf) (2014)
  > Propose *hybrid logical clocks (HLC)*.

## Consistency

### Papers

- [How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Progranm](papers/distributed-system/sequential-consistency.pdf) (1979)
  > Propose *sequential consistency*.

- [Linearizability: A Correctness Condition for Concurrent Objects](papers/distributed-system/linearizability.pdf) (1990)

- [Session Guarantees for Weakly Consistent Replicated Data](papers/distributed-system/session-guarantees.pdf) (1994)
  > Propose *session guarantees*: *monotonic reads*, *monotonic writes*, *read your writes*, and *writes follow reads*.

- [Causal Memory: Definitions, Implementation and Programming](papers/distributed-system/causal-consistency.pdf) (1995)
  > Propose *causal consistency*.

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/distributed-system/cap-theorem.pdf) (2002)
  > Prove the *CAP conjecture* that it is impossible to provide all the three properties: *Consistency*, *Availability*, and *Partition-tolerance*.

- [Eventually Consistent](papers/distributed-system/eventual-consistency.pdf) (2009)

- [Consistency in Non-Transactional Distributed Storage Systems](papers/distributed-system/distributed-consistency.pdf) (2016)
  > Overview more than 50 different consistency notions and provie a partial order among them.

### Articles

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)
  > Revisit the *CAP theorem* to maximize combinations of consistency and availability.

# Distributed Storage

## File System

### Papers

- [The Google File System](papers/distributed-storage/gfs.pdf) (2003)

## NoSQL Storage

### Papers

- [Bigtable: A Distributed Storage System for Structured Data](papers/distributed-storage/bigtable.pdf) (2006)

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/distributed-storage/dynamo.pdf) (2007)

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
  > Prove that recognizing the transaction histories that are serializable is an *NP-complete* problem.
  >
  > Introduce several efficiently recognizable subclasses of serializable histories.

- [Concurrency Control in Distributed Database Systems](papers/distributed-database/serializability-algorithms.pdf) (1981)
  > Charaterize serializability with *read-write* and *write-write* conflicts.
  >
  > Describe 48 concurrency control algorithms based on *two-phase locking* and *timestamp ordering*.

- [The Transaction Concept: Virtues and Limitations](papers/distributed-database/transaction-concept.pdf) (1981)
  > Propose the transaction concept with properties: *Atomicity*, *Consistency* and *Durability*.

- [Principles of Transaction-Oriented Database Recovery](papers/distributed-database/transaction-acid.pdf) (1983)
  > Propose the transaction principles and the *ACID* properties: *Atomicity*, *Consistency*, *Isolation* and *Durability*.

- [A Critique of ANSI SQL Isolation Levels](papers/distributed-database/snapshot-isolation.pdf) (1995)
  > Propose clearer definitions to charaterize existing ANSI isolation levels and a new *snapshot isolation*.

- [Weak Consistency: A Generalized Theory and Optimistic Implementations for Distributed Transactions](papers/distributed-database/generalized-isolation-thesis.pdf) (1999)
  > Propose a graph-based approach to define existing ANSI isolation levels and other widely used levels, e.g., *cursor stability*, *snapshot isolation*.
  >
  > Propose two new isolation levels: *consistent view (PL-2+)* and *monotonic view (PL-2L)*.

- [Generalized Isolation Level Definitions](papers/distributed-database/generalized-isolation.pdf) (2000)
  > Propose a graph-based approach to define existing ANSI isolation levels.
  > *This is a paper simplified from the above thesis*.

- [Serializable Isolation for Snapshot Databases](papers/distributed-database/serializable-snapshot-isolation.pdf) (2008)
  > Propose an algorithm to achieve *serializable snapshot isolation* based on *anti-dependencies* detection.

- [A Critique of Snapshot Isolation](papers/distributed-database/write-snapshot-isolation.pdf) (2012)
  > Propose a new *write-snapshot isolation*, which is serializable and comparable with *snapshot isolation* in performance.

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
  > Introduce *TrueTime* to support *external consistency*.

- [Spanner, TrueTime and the CAP Theorem](papers/distributed-database/spanner-and-cap-theorem.pdf) (2017)
  > Discuss the techniques behind *Spanner* that make it an "effectively CA" system.

### Articles

- [Living Without Atomic Clocks](https://www.cockroachlabs.com/blog/living-without-atomic-clocks/) (2016)
  > Real-world example of *hybrid logical clocks (HLC)* and *write-snapshot isolation*.

- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html) (2017)
  > *Spanner* vs. *Calvin*, Part 1

- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html) (2018)
  > *Spanner* vs. *Calvin*, Part 2

- [Consistency without Clocks: The FaunaDB Distributed Transaction Protocol](https://fauna.com/blog/consistency-without-clocks-faunadb-transaction-protocol) (2018)
  > Real-world example of *Calvin*.

- [Demystifying Database Systems, Part 1: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels) (2019)
- [Demystifying Database Systems, Part 2: Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation) (2019)
- [Demystifying Database Systems, Part 3: Introduction to Consistency Levels](https://fauna.com/blog/demystifying-database-systems-introduction-to-consistency-levels) (2019)
- [Demystifying Database Systems, Part 4: Isolation levels vs. Consistency levels](https://fauna.com/blog/demystifying-database-systems-part-4-isolation-levels-vs-consistency-levels) (2019)

----------------------------------------

# To be Continued

The following part is the original, but I'm reorganizing these materials.

## Posts

- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/)
  > Programming a database is possibly the most instructive project one can ever complete as a software developer.

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/)
  > A list of some lessons I’ve learned as a distributed systems engineer that are worth being told to a new engineer.

- [Elements Of Scale: Composing And Scaling Data Platforms](http://highscalability.com/blog/2015/5/4/elements-of-scale-composing-and-scaling-data-platforms.html)
  > A masterful tour through the evolutionary forces that shape how systems adapt to key challenges.

- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data)
  > As we’re in such a fast-moving field, we often have a tendency of dismissing older ideas as irrelevant – and consequently, we end up having to learn the same lessons over and over again, the hard way.

## Storage Engine

### Papers

- [Weaving Relations for Cache Performance](papers/pax.pdf) (2001)
  > A new data organization model called PAX (Partition Attributes Across), that significantly improves cache performance by grouping together all values of each attribute within each page.

- [Cache-Oblivious Streaming B-trees](papers/sbtree.pdf) (2007)
  > A streaming B-tree is a dictionary that efficiently implements insertions and range queries. We present two cache-oblivious streaming B-trees, the shuttle tree, and the cache-oblivious lookahead array (COLA).

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/bitcask.pdf) (2010)

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/lsm.pdf) (1996)
  > The LSM-tree uses an algorithm that defers and batches index changes, cascading the changes from a memory-based component through one or more disk components in an efficient manner reminiscent of merge sort.

- [bLSM: A General Purpose Log Structured Merge Tree](papers/blsm.pdf) (2012)
  > bLSM, a Log Structured Merge (LSM) tree with the advantages of B-Trees and log structured approaches.

- [The Bw-Tree: A B-tree for New Hardware Platforms](papers/bw-tree.pdf) (2013)
  > Our new form of B-tree, calledthe Bw-tree achieves its very  high performance via a latch-freeapproach that effectively exploits the processor caches ofmodernmulti-core chips.

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/wisckey.pdf) (2016)
  > WiscKey, a persistent LSM-tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/data-calculator.pdf) (2018)
  > We present a design engine, the Data Calculator, which enables interactive and semi-automated design of data structures.

### Links

- [Fractal tree index](https://en.wikipedia.org/wiki/Fractal_tree_index)
  > A Fractal Tree index is a tree data structure that keeps data sorted and allows searches and sequential access in the same time as a B-tree but with insertions and deletions that are asymptotically faster than a B-tree.

- [MySQL vs something else. Evaluating alternative databases.](https://vimeo.com/98428203)

## Consensus Algorithm

### Papers

- [The Part-Time Parliament](papers/paxos.pdf) (1998)
  > The Island of Paxos.

- [Paxos Made Simple](papers/paxos-made-simple.pdf) (2001)
  > The Paxos algorithm, when presented in plain English, is very simple.

- [Fast Paxos](papers/fast-paxos.pdf) (2005)
  > Fast Paxos is an extension of the classic Paxos algorithm that allows the value to be learned in two message delays.

- [Paxos Made Live - An Engineering Perspective](papers/paxos-made-live.pdf) (2007)
  > We used the Paxos algorithm (“Paxos”) as the base for a framework that implements a fault-tolerant log. We then relied on that framework to build a fault-tolerant database.

- [There Is More Consensus in Egalitarian Parliaments](papers/epaxos.pdf) (2013)
  > Egalitarian Paxos is to our knowledge the first protocol requiring only a simple majority of replicas to be non-faulty, using a number of messages linear in the number of replicas to choose a command, and committing commands after just one communication round in the common case or after at most two rounds in any case.

- [Paxos Quorum Leases: Fast Reads Without Sacrificing Writes](papers/paxos-lease.pdf) (2014)

- [In Search of an Understandable Consensus Algorithm](papers/raft.pdf) (2014)
  > Raft is a consensus algorithm for managing a replicated log. It produces a result equivalent to Paxos, and it is as efficient as Paxos.

### Links

- [Neat Algorithms - Paxos](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/)

- [Implementing Replicated Logs with Paxos](https://ramcloud.stanford.edu/~ongaro/userstudy/paxos.pdf)

## SQL Database

### Papers

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/megastore.pdf) (2011)
  > Megastore blends the scalability of a NoSQL datastore with the convenience of a traditional RDBMS in a novel way, and provides both strong consistency guarantees and high availability.

- [F1: A Distributed SQL Database That Scales](papers/f1.pdf) (2013)
  > F1 is a hybrid database that combines high availability, the scalability of NoSQL systems like Bigtable, and the consistency and usability of traditional SQL databases.

- [Online, Asynchronous Schema Change in F1](papers/f1-online-ddl.pdf) (2013)
  > We introduce a protocol for schema evolution in a globally distributed database management system with shared data, stateless servers, and no global membership.

- [Spanner: Becoming a SQL System](papers/spanner-2017.pdf) (2017)
  > In this paper, we focus on the "database system" aspects of Spanner, in particular how query execution has evolved and forced the rest of Spanner to evolve.

### Links

- [How does a relational database work](http://coding-geek.com/how-databases-work/)
  > Relational Databases are very interesting because they’re based on useful and reusable concepts. If understanding a database interests you but you’ve never had the time or the will to dig into this wide subject, you should like this article.
