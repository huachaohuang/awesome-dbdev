# Awesome Database Development

Database development is fun :-)

## Posts

- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/)
  > Programming a database is possibly the most instructive project one can ever complete as a software developer.

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/)
  > A list of some lessons I’ve learned as a distributed systems engineer that are worth being told to a new engineer.

- [Elements Of Scale: Composing And Scaling Data Platforms](http://highscalability.com/blog/2015/5/4/elements-of-scale-composing-and-scaling-data-platforms.html)
  > A masterful tour through the evolutionary forces that shape how systems adapt to key challenges.

- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data)
  > As we’re in such a fast-moving field, we often have a tendency of dismissing older ideas as irrelevant – and consequently, we end up having to learn the same lessons over and over again, the hard way.

## Hard Disk

### Links

- [RAID](https://en.wikipedia.org/wiki/RAID)

- [Coding for SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/)
  > The basics of SSDs along with all of the recommended access patterns on how reads and writes should be implemented to get the best performance out of solid-state drives.

## File System

### Papers

- [The Google File System](papers/gfs.pdf) (2003)
  > The Google File System, a scalable distributed file system for large distributed data-intensive applications.

## Storage Engine

### Papers

- [Weaving Relations for Cache Performance](papers/pax.pdf) (2001)
  > A new data organization model called PAX (Partition Attributes Across), that significantly improves cache performance by grouping together all values of each attribute within each page.

- [Cache-Oblivious Streaming B-trees](papers/sbtree.pdf) (2007)
  > A streaming B-tree is a dictionary that efficiently implements insertions and range queries. We present two cache-oblivious streaming B-trees, the shuttle tree, and the cache-oblivious lookahead array (COLA).

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/bitcask.pdf) (2010)

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/lsm.pdf) (1996)
  > The LSM-tree uses an algorithm that defers and batches index changes, cascading the changes from a memory-based component through one or more disk components in an efficient manner reminiscent of merge sort.

- [bLSM: A General Purpose Log Structured Merge Tree](papers/gp-lsm.pdf) (2012)
  > bLSM, a Log Structured Merge (LSM) tree with the advantages of B-Trees and log structured approaches.

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/wisckey.pdf) (2016)
  > WiscKey, a persistent LSM-tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/datacalculator.pdf) (2018)
  > We present a design engine, the Data Calculator, which enables interactive and semi-automated design of data structures.

### Links

- [Fractal tree index](https://en.wikipedia.org/wiki/Fractal_tree_index)
  > A Fractal Tree index is a tree data structure that keeps data sorted and allows searches and sequential access in the same time as a B-tree but with insertions and deletions that are asymptotically faster than a B-tree.

- [MySQL vs something else. Evaluating alternative databases.](https://vimeo.com/98428203)

## CAP Theorem

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/cap-theorem.pdf) (2002)
  > We prove the CAP theorem in the asynchronous network model, and then discuss solutions to this dilemma in the partially synchronous model.

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)
  > The modern CAP goal should be to maximize combinations of consistency and availability that make sense for the specific application.

- [Spanner, TrueTime and the CAP Theorem](papers/cap-spanner.pdf) (2017)
  > The original point of the CAP theorem was to get designers to take this tradeoff seriously. But there are two important caveats: first, you only need forfeit something during an actual partition, and even then there are many mitigations. Second, the actual theorem is about 100% availability, while the interesting discussion here is about the tradeoffs involved for realistic high availability.

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

- [In Search of an Understandable Consensus Algorithm](papers/raft.pdf) (2014)
  > Raft is a consensus algorithm for managing a replicated log. It produces a result equivalent to Paxos, and it is as efficient as Paxos.

### Links

- [Neat Algorithms - Paxos](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/)

- [Implementing Replicated Logs with Paxos](https://ramcloud.stanford.edu/~ongaro/userstudy/paxos.pdf)

## Distributed Clock

### Papers

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/logical-clock.pdf) (1978)
  > A distributed algorithm is given for synchronizing a system of logical clocks which can be used to totally order the events.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/logical-physical-clock.pdf) (2014)
  > We propose a hybrid logical clock, HLC, that combines the best of logical clocks and physical clocks. HLC captures the causality relationship like logical clocks, and enables easy identification of consistent snapshots in distributed systems.

## Distributed Transaction

### Papers

- [A Critique of ANSI SQL Isolation Levels](papers/isolation-levels.pdf) (1995)
  > Investigating the ambiguities of the phenomena leads to clearer definitions; in addition new phenomena that better characterize isolation types are introduced. An important multiversion isolation type, Snapshot Isolation, is defined.

- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](papers/percolator.pdf) (2010)
  > Percolator provides cross-row, cross-table transactions with ACID snapshot-isolation semantics.

- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](papers/calvin.pdf) (2012)
  > Calvin is a practical transaction scheduling and data replication layer that uses a deterministic ordering guarantee to significantly reduce the normally prohibitive contention costs associated with distributed transactions.

- [A Critique of Snapshot Isolation](papers/write-snapshot-isolation.pdf) (2012)
  > We introduce write-snapshot isolation, a novel isolation level that has a performance comparable with that of snapshot isolation, and yet provides serializability.

## SQL Database

### Papers

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/megastore.pdf) (2011)
  > Megastore blends the scalability of a NoSQL datastore with the convenience of a traditional RDBMS in a novel way, and provides both strong consistency guarantees and high availability.

- [Spanner: Google’s Globally-Distributed Database](papers/spanner.pdf) (2012)
  > Spanner is Google’s scalable, multi-version, globallydistributed, and synchronously-replicated database. It is the first system to distribute data at global scale and support externally-consistent distributed transactions.

- [F1: A Distributed SQL Database That Scales](papers/f1.pdf) (2013)
  > F1 is a hybrid database that combines high availability, the scalability of NoSQL systems like Bigtable, and the consistency and usability of traditional SQL databases.

- [Online, Asynchronous Schema Change in F1](papers/f1-online-ddl.pdf) (2013)
  > We introduce a protocol for schema evolution in a globally distributed database management system with shared data, stateless servers, and no global membership.

- [Spanner: Becoming a SQL System](papers/spanner-2017.pdf) (2017)
  > In this paper, we focus on the "database system" aspects of Spanner, in particular how query execution has evolved and forced the rest of Spanner to evolve.

### Links

- [How does a relational database work](http://coding-geek.com/how-databases-work/)
  > Relational Databases are very interesting because they’re based on useful and reusable concepts. If understanding a database interests you but you’ve never had the time or the will to dig into this wide subject, you should like this article.

## NoSQL Database

### Papers

- [Bigtable: A Distributed Storage System for Structured Data](papers/bigtable.pdf) (2006)
  > Bigtable is a distributed storage system for managing structured data that is designed to scale to a very large size: petabytes of data across thousands of commodity servers.

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/dynamo.pdf) (2007)
  > This paper presents the design and implementation of Dynamo, a highly available key-value storage system that some of Amazon’s core services use to provide an “always-on” experience.
