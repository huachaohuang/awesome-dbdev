# About

You want to become an awesome database developer?

Great, that's fun but challenging. Don't panic, I collect some awesome materials here for us.

# SQL

## Optimizer

### Papers

- [Access Path Selection in a Relational Database Management System](papers/sql/systemr.pdf) (SIGMOD, 1979)

  This paper introduces a cost-based SQL optimizer in System R. The optimizer
  estimates the cost of access paths in terms of I/O and CPU costs, using
  statistics about the contents of each relation.

- [The Volcano Optimizer Generator: Extensibility and Efficient Search](papers/sql/volcano.pdf) (ICDE, 1993)

  This paper introduces an optimizer generator that translates a model
  specification into an optimizer source code. It also provides a search engine
  to be used in all generated optimizers. The search engine is goal-oriented
  using directed dynamic programming search algorithms.

- [The Cascades Framework for Query Optimization](papers/sql/cascades.pdf) (IEEE, 1995)

### Posts

- [How We Built a Cost-Based SQL Optimizer](https://www.cockroachlabs.com/blog/building-cost-based-sql-optimizer/) (Cockroach Labs, 2018)

## Execution

### Papers

- [MonetDB/X100: Hyper-Pipelining Query Execution](papers/sql/monetdb.pdf) (CIDR, 2005)

  This paper introduces a CPU efficient query processor that employs a
  vectorized query processing model. The processor uses loop-pipelined and
  cache-conscious operations to take advantage of modern CPUs.

### Posts

- [How We Built a Vectorized SQL Engine](https://www.cockroachlabs.com/blog/how-we-built-a-vectorized-sql-engine/) (Cockroach Labs, 2019)

# Transaction

## Concurrency

### Books

- [Concurrency Control and Recovery in Database Systems](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/05/ccontrol.zip) (1987)

### Papers

- [Granularity of Locks and Degrees of Consistency in a Shared Data Base](papers/transaction/consistency-and-locks.pdf) (IBM, 1975)

  The first part of this paper introduces a locking protocol that allows
  simultaneous locking at various granularities in a database with a
  hierarchical structure. The second part of this paper introduces four degrees
  of consistency and the relationships of the four degrees to the locking
  protocol.

- [The Notion of Consistency and Predicate Locks in a Database System](papers/transaction/consistency-and-predicate-locks.pdf) (IBM, 1976)

  This paper proofs that two-phase locking (2PL) guarantees serializability and
  introduces predicate locks to address the problem of phantom reads.

- [A Critique of ANSI SQL Isolation Levels](papers/transaction/snapshot-isolation.pdf) (SIGMOD, 1995)

  This paper analyzes the ambiguities of ANSI isolation levels and provides
  clearer phenomena definitions. It also introduces a new MVCC isolation level
  called *snapshot isolation*. A transaction in snapshot isolation reads data
  from a snapshot of the committed data as of the time the transaction started,
  and checks for write-write conflicts.

- [Generalized Isolation Level Definitions](papers/transaction/generalized-isolation.pdf) (ICDE, 2000)

  This paper proposes a graph-based approach to define existing ANSI isolation levels.

- [Serializable Isolation for Snapshot Databases](papers/transaction/serializable-snapshot-isolation.pdf) (SIGMOD, 2008)

  This paper presents an algorithm to achieve serializable snapshot isolation
  based on anti-dependencies detection.

- [A Critique of Snapshot Isolation](papers/transaction/write-snapshot-isolation.pdf) (EuroSys, 2012)

  This paper introduces a new MVCC isolation level called *write-snapshot
  isolation*. A transaction in write-snapshot isolation checks for read-write
  conflicts instead of write-write conflicts in snapshot isolation.

## Consistency

### Papers

- [How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Progranm](papers/transaction/sequential-consistency.pdf) (Lamport, 1979)

  This paper defines the condition of *sequential consistency* and describes a
  method to ensure the sequential consistency of interconnecting sequential
  processors with memory modules.

- [Linearizability: A Correctness Condition for Concurrent Objects](papers/transaction/linearizability.pdf) (1990)

  This paper defines the condition of *linearizability* and discusses the
  differences between it and other correctness conditions.

- [Session Guarantees for Weakly Consistent Replicated Data](papers/transaction/session-guarantees.pdf) (PDIS, 1994)

  This paper proposes four per-session guarantees to aid users and applications
  of weakly consistent replicated data: Read Your Writes, Monotonic Reads,
  Writes Follow Reads, and Monotonic Writes.

- [Causal Memory: Definitions, Implementation and Programming](papers/transaction/causal-memory.pdf) (1995)

  This paper defines the condition of *causal consistency* based on Lamport's
  "happened before" relation.

- [Consistency in Non-Transactional Distributed Storage Systems](papers/transaction/consistency-overview.pdf) (CSUR, 2016)

  This paper provides a structured and comprehensive overview of different
  consistency notions and provide a partial order among different consistency
  predicates.

## Distributed Transaction

### Papers

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/transaction/logical-clocks.pdf) (Lamport, 1978)

  This paper discusses the partial ordering defined by the "happened before"
  relation, and gives a distributed algorithm for extending it to a consistent
  total ordering of all the events.

- [Consensus on Transaction Commit](papers/transaction/paxos-commit.pdf) (2004)

  This paper presents the Paxos Commit algorithm. Paxos Commit runs a Paxos
  consensus algorithm on the commit/abort decision of each participant to obtain
  a transaction commit protocol that uses 2F + 1 coordinators and makes progress
  if at least F + 1 of them are working properly.

- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](papers/transaction/percolator.pdf) (OSDI, 2010)

  This paper presents Percolator, an incremental update processing system built
  on top of Bigtable. Percolator provides snapshot isolation transactions using
  a two-phase commit protocol.

- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](papers/transaction/calvin.pdf) (SIGMOD, 2012)

  This paper presents Calvin, a practical transaction scheduling and data
  replication layer that uses a deterministic ordering guarantee to
  significantly reduce the normally prohibitive contention costs associated with
  distributed transactions.

- [Highly Available Transactions: Virtues and Limitations](papers/transaction/highly-available-transactions.pdf) (VLDB, 2013)

  This paper introduces a taxonomy of highly available systems and analyze
  existing ACID isolation and distributed data consistency guarantees to
  identify which can and cannot be achieved in HAT systems.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/transaction/hybrid-logical-clocks.pdf) (OPODIS, 2014)

  This paper proposes a hybrid logical clock, HLC, that combines the best of
  logical clocks and physical clocks.

- [SLOG: Serializable, Low-latency, Geo-replicated Transactions](papers/transaction/slog.pdf) (VLDB, 2019)

  This paper presents SLOG, a system that provides strictly serializable ACID
  transactions at geo-replicated distance. SLOG achieves high-throughtput and
  low latency for transactions that initiate from a location close to the home
  region for data they access.

### Posts

- [Linearizability versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/) (Peter Bailis, 2014)
- [How CockroachDB Does Distributed, Atomic Transactions](https://www.cockroachlabs.com/blog/how-cockroachdb-distributes-atomic-transactions/) (Cockroach Labs, 2015)
- [Living Without Atomic Clocks](https://www.cockroachlabs.com/blog/living-without-atomic-clocks/) (Cockroach Labs, 2016)
- [Serializable, Lockless, Distributed: Isolation in CockroachDB](https://www.cockroachlabs.com/blog/serializable-lockless-distributed-isolation-cockroachdb/) (Cockroach Labs, 2016)
- [CockroachDB’s Consistency Model](https://www.cockroachlabs.com/blog/consistency-model/) (Cockroach Labs, 2019)
- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html) (Daniel Abadi, 2017)
- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html) (Daniel Abadi, 2018)
- [Consistency without Clocks: The FaunaDB Distributed Transaction Protocol](https://fauna.com/blog/consistency-without-clocks-faunadb-transaction-protocol) (Fauna, 2018)
- [Demystifying Database Systems, Part 1: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels) (Fauna, 2019)
- [Demystifying Database Systems, Part 2: Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation) (Fauna, 2019)
- [Demystifying Database Systems, Part 3: Introduction to Consistency Levels](https://fauna.com/blog/demystifying-database-systems-introduction-to-consistency-levels) (Fauna, 2019)
- [Demystifying Database Systems, Part 4: Isolation levels vs. Consistency levels](https://fauna.com/blog/demystifying-database-systems-part-4-isolation-levels-vs-consistency-levels) (Fauna, 2019)

# Replication

## Principles

### Papers

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/replication/cap-theorem.pdf) (SIGACT, 2002)

  This paper proves the *CAP conjecture* in the asynchronous network model, and
  then discusses solutions to this dilemma in the partially synchronous model.

### Posts

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (Eric Brewer, 2012)

## Consensus

### Papers

- [Paxos Made Simple](papers/replication/paxos.pdf) (Lamport, 2001)

  > The Paxos algorithm, when presented in plain English, is very simple.

- [Paxos Made Live - An Engineering Perspective](papers/replication/paxos-made-live.pdf) (PODC, 2007)

  This paper describes the experience of building Chubby, a fault-tolerant
  storage system using the Paxos consensus algorithm.

- [There Is More Consensus in Egalitarian Parliaments](papers/replication/epaxos.pdf) (SOSP, 2013)

  This paper describes the design and implementation of Egalitarian Paxos
  (EPaxos), a new distributed consensus algorithm based on Paxos that achieves
  uniform load balancing across all replicas.

- [Paxos Quorum Leases: Fast Reads Without Sacrificing Writes](papers/replication/paxos-quorum-leases.pdf) (SOCC, 2014)

  This paper describes *quorum leases*, a technique that allows Paxos-based
  systems to perform consistent local reads on multiple replicas.

- [In Search of an Understandable Consensus Algorithm](papers/replication/raft.pdf) (USENIX, 2014)

  This paper introduces Raft, a consensus algorithm for managing a replicated
  log. Raft produces a result equivalent to Paxos, and it is as efficient as
  Paxos, but its structure is different from Paxos. Raft is more understandable
  than Paxos and also provides a better foundation for building practical
  systems.

### Posts

- [Implementing Replicated Logs with Paxos](https://ongardie.net/static/raft/userstudy/paxos.pdf) (2013)
- [Neat Algorithms - Paxos](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/) (2014)

# Storage Engine

## Principles

### Papers

- [The Five-Minute Rule for Trading Memory for Disc Accesses](papers/storage-engine/five-minute-rule-1987.pdf) (SIGMOD, 1987)
- [The Five-Minute Rule 10 Years Later, and Other Computer Storage Rules of Thumb](papers/storage-engine/five-minute-rule-1997.pdf) (SIGMOD, 1997)
- [The Five-Minute Rule 20 Years Later, and How Flash Memory Changes the Rules](papers/storage-engine/five-minute-rule-2007.pdf) (2007)
- [The Five-Minute Rule 30 Years Later, and its Impact on the Storage Hierarchy](papers/storage-engine/five-minute-rule-2017.pdf) (2017)

## Data Structures

### Papers

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/storage-engine/lsmtree.pdf) (1996)

  This paper introduces the *Log-Structured Merge-tree (LSM-tree)*, a disk-based
  data structure designed to provide low-cost indexing for a file experiencing a
  high rate of record inserts (and deletes) over an extended period. The
  LSM-tree uses an algorithm that defers and batches index changes, cascading
  the changes from a memory-based component through one or more disk components
  in an efficient manner reminiscent of merge sort.

- [bLSM: A General Purpose Log Structured Merge Tree](papers/storage-engine/blsm.pdf) (SIGMOD, 2012)

  This paper introduces *bLSM*, a Log Structured Merge (LSM) tree with the
  advantages of B-Trees and log structured approaches. bLSM uses Bloom filters
  to improve index performance and uses *spring and gear scheduler* to avoid
  long write pauses.

# Storage Device

There are a lot of concepts here, I have put up a post to explain them:
[What You Should Know About Storage Devices](http://huachaohuang.com/2019/08/28/what-you-should-know-about-storage-devices.html)

## Media

### Wikis

- [Hard Disk Drive (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive)
- [Solid-State Drive (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive)

### Posts

- [Coding for SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/)

### Videos

- [How HDD Works](https://www.youtube.com/watch?v=Ep-yM894mQQ)
- [The Development of HDD Technique](https://www.youtube.com/watch?v=wteUW2sL7bc)
- [How Flash Memory Works](https://www.youtube.com/watch?v=s7JLXs5es7I)

## Interface

### Wikis

- [Small Computer System Interface (SCSI)](https://en.wikipedia.org/wiki/SCSI)
- [Serial Attached SCSI (SAS)](https://en.wikipedia.org/wiki/Serial_Attached_SCSI)
- [AT Atachment (ATA)](https://en.wikipedia.org/wiki/Parallel_ATA)
- [Serial AT Attachment (SATA)](https://en.wikipedia.org/wiki/Serial_ATA)
- [Advanced Host Controller Interface (AHCI)](https://en.wikipedia.org/wiki/Advanced_Host_Controller_Interface)
- [Peripheral Component Interconnect (PCI)](https://en.wikipedia.org/wiki/Conventional_PCI)
- [PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express)
- [NVM Express (NVMe)](https://en.wikipedia.org/wiki/NVM_Express)

### Videos

- [Understanding SCSI](https://www.youtube.com/watch?v=pR7SdrXdT4M)
- [A History of PC Buses - From ISA to PCI Express](https://www.youtube.com/watch?v=qla-5isbK60)

## Virtualization

### Wikis

- [Logical Volume Manager (LVM)](https://en.wikipedia.org/wiki/Logical_Volume_Manager_(Linux))
- [Redundant Array of Independent Disks (RAID)](https://en.wikipedia.org/wiki/RAID)

### Videos

- [Logical Volume Management (LVM) - Linux](https://www.youtube.com/watch?v=fadQX2e_PGk)
- [What is RAID 0, 1, 2, 3, 4, 5, 6 and 10 (1+0)?](https://www.youtube.com/watch?v=wTcxRObq738)

# Operating System

## Books

- [Linux Device Drivers](https://www.oreilly.com/library/view/linux-device-drivers/0596005903/)
- [Understanding the Linux Kernel](https://www.oreilly.com/library/view/understanding-the-linux/0596005652/)
- [Understanding the Linux Virtual Memory Manager](https://www.kernel.org/doc/gorman/)
- [ext4 Data Structures and Algorithms](https://www.kernel.org/doc/html/latest/filesystems/ext4/index.html)

## Papers

- [The Slab Allocator: An Object-Caching Kernel Memory Allocator](papers/operating-system/slab-allocator.pdf) (1994)

  This paper presents a comprehensive design overview of the SunOS 5.4 kernel
  memory allocator.

- [What Every Programmer Should Know About Memory](papers/operating-system/cpumemory.pdf) (2007)

  This paper explains the structure of memory subsystems in use on modern
  commodity hardware, illustrating why CPU caches were developed, how they work,
  and what programs should do to achieve optimal performance by utilizing them.

- [What Every Systems Programmer Should Know About Concurrency](papers/operating-system/concurrency-primer.pdf) (2018)

  This paper explains some fundamentals about concurrency on modern hardware.

# Distributed Storage

## Papers

- [The Google File System](papers/distributed-storage/gfs.pdf) (SOSP, 2003)

  This paper presents the Google File System, a scalable distributed file system
  for large distributed data-intensive applications.

- [Bigtable: A Distributed Storage System for Structured Data](papers/distributed-storage/bigtable.pdf) (OSDI, 2006)

  This paper presents Bigtable, a distributed storage system for managing
  structured data that is designed to scale to a very large size.

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/distributed-storage/dynamo.pdf) (SOSP, 2007)

  This paper presents the design and implementation of Dynamo, a highly
  available key-value storage system that some of Amazon's core services use to
  provide an “always-on” experience.

# Distributed Database

## Papers

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/distributed-database/megastore.pdf) (CIDR, 2011)

  This paper presents Megastore, a storage system that blends the scalability of
  a NoSQL datastore with the convenience of a traditional RDBMS in a novel way,
  and provides both strong consistency guarantees and high availability.

- [Spanner: Google’s Globally-Distributed Database](papers/distributed-database/spanner.pdf) (OSDI, 2012)

  This paper presents Spanner, a scalable, multi-version, globally-distributed,
  and synchronously-replicated database.

- [F1: A Distributed SQL Database That Scales](papers/distributed-database/f1.pdf) (VLDB, 2013)

  This paper presents F1, a hybrid database that combines high availability, the
  scalability of NoSQL systems like Bigtable, and the consistency and usability
  of traditional SQL databases. F1 is built on Spanner, which provides
  synchronous cross-datacenter replication and strong consistency.

- [Online, Asynchronous Schema Change in F1](papers/distributed-database/f1-schema.pdf) (VLDB, 2013)

  This paper introduces a protocol for schema evolution in a globally
  distributed database management system with shared data, stateless servers,
  and no global membership.

- [Spanner: Becoming a SQL System](papers/distributed-database/spanner-sql.pdf) (SIGMOD, 2017)

  This paper highlights the database DNA of Spanner. It describes distributed
  query execution in the presence of resharding, query restarts upon transient
  failures, range extraction that drives query routing and index seeks, and the
  improved blockwise-columnar storage format.

- [Spanner, TrueTime and the CAP Theorem](papers/distributed-database/spanner-cap.pdf) (Eric Brewer, 2017)

  This paper justifies Spanner as an "effectively CA" system despite operating
  over a wide area.

## Posts

- [How online schema changes are possible in CockroachDB](https://www.cockroachlabs.com/blog/how-online-schema-changes-are-possible-in-cockroachdb/) (Cockroach Labs, 2016)

# Miscellaneous

## Books

- [Readings in Database Systems](http://www.redbook.io/)

## Posts

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) (2013)
- [How does a relational database work](http://coding-geek.com/how-databases-work/) (2015)
- [Elements Of Scale: Composing And Scaling Data Platforms](http://www.benstopford.com/2015/04/28/elements-of-scale-composing-and-scaling-data-platforms/) (2015)
- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) (2015)
- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/) (2016)

--------------------------------------------------------------------------------

THE FOLLOWING PARTS ARE UNDER RE-ORGANIZING

--------------------------------------------------------------------------------

# Storage System

## Storage Engine

### Papers

- [Weaving Relations for Cache Performance](papers/storage-system/pax.pdf) (2001)
  > Introduce a new data organization model called *Partition Attributes Across (PAX)* that significantly improves cache performance by grouping together all values of each attribute within each page.

- [C-Store: A Column-oriented DBMS](papers/storage-system/c-store.pdf) (2005)

- [Cache-Oblivious Streaming B-trees](papers/storage-system/streaming-btree.pdf) (2007)
  > Introduce two *cache-oblivious streaming B-trees* that efficiently implements insertions and range queries.

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/storage-system/bitcask.pdf) (2010)

- [The Bw-Tree: A B-tree for New Hardware Platforms](papers/storage-system/bw-tree.pdf) (2013)
  > Introduce *Bw-Tree*, a new form of B-Tree that achieves its very high performance via a latch-free approach that effectively exploits the processor caches of modern multi-core chips.

- [Hekaton: SQL Server’s Memory-Optimized OLTP Engine](papers/storage-system/hekaton.pdf) (2013)

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/storage-system/wisckey.pdf) (2016)
  > Introduce *WiscKey*, a persistent LSM-Tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/storage-system/data-calculator.pdf) (2018)
  > Introduce the *Data Calculator*, a design engine that enables interactive and semi-automated design of data structures.
