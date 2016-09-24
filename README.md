# Awesome Database Development

Database development is fun :-)

## General

## Papers

* [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)

> The modern CAP goal should be to maximize combinations of
> consistency and availability that make sense for the specific
> application.

## Posts

* [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) (2013)

> Below is a list of some lessons I’ve learned as a distributed
> systems engineer that are worth being told to a new engineer. Some
> are subtle, and some are surprising, but none are
> controversial. This list is for the new distributed systems engineer
> to guide their thinking about the field they are taking on. It’s not
> comprehensive, but it’s a good beginning.

* [Elements Of Scale: Composing And Scaling Data Platforms](http://highscalability.com/blog/2015/5/4/elements-of-scale-composing-and-scaling-data-platforms.html) (2015)

> A masterful tour through the evolutionary forces that shape how
> systems adapt to key challenges.

* [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/) (2016)

> Programming a database is fascinating work.

* [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) (2016)

> Although computers have got faster, data has got bigger and
> requirements have become more complex, many old ideas are actually
> still highly relevant today.

## Storage Engine

### Papers

* [The Log-Structured Merge-Tree (LSM-Tree)](https://paperhub.s3.amazonaws.com/18e91eb4db2114a06ea614f0384f2784.pdf) (1996)

> The Log-Structured Merge-tree (LSM-tree) is a disk-based data
> structure designed to provide low-cost indexing for a file
> experiencing a high rate of record inserts (and deletes) over an
> extended period.

* [Cache-Oblivious Streaming B-trees](http://supertech.csail.mit.edu/papers/sbtree.pdf) (2007)

> A streaming B-tree is a dictionary that efficiently implements
> insertions and range queries.  We present two cache-oblivious
> streaming B-trees, the shuttle tree, and the cache-oblivious
> lookahead array (COLA).

* [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](http://basho.com/wp-content/uploads/2015/05/bitcask-intro.pdf) (2010)

> The origin of Bitcask is tied to the history of the Riak distributed
> database.

* [bLSM: A General Purpose Log Structured Merge Tree](http://www.eecs.harvard.edu/~margo/cs165/papers/gp-lsm.pdf) (2012)

> We then present bLSM, a Log Structured Merge (LSM) tree with the
> advantages of B-Trees and log structured approaches: (1) Unlike
> existing log structured trees, bLSM has near-optimal read and scan
> performance, and (2) its new “spring and gear” merge scheduler
> bounds write latency without impacting throughput or allowing merges
> to block writes for extended periods of time.

### Videos

* [MySQL vs something else. Evaluating alternative databases.](https://vimeo.com/98428203) (2013)

## SQL Database

### Papers

* [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/36971.pdf) (2011)

> Megastore blends the scalability of a NoSQL datastore with the
> convenience of a traditional RDBMS in a novel way, and provides both
> strong consistency guarantees and high availability.

* [F1: A Distributed SQL Database That Scales](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/41344.pdf) (2013)

> F1 is a hybrid database that combines high availability, the
> scalability of NoSQL systems like Bigtable, and the consistency and
> usability of traditional SQL databases.

### Posts

* [How does a relational database work](http://coding-geek.com/how-databases-work/) (2015)

> Relational Databases are very interesting because they’re based on
> useful and reusable concepts.  If understanding a database interests
> you but you’ve never had the time or the will to dig into this wide
> subject, you should like this article.

## NoSQL Database

### Papers

* [Bigtable: A Distributed Storage System for Structured Data](http://static.googleusercontent.com/media/research.google.com/en//archive/bigtable-osdi06.pdf) (2006)

> Bigtable is a distributed storage system for managing structured
> data that is designed to scale to a very large size: petabytes of
> data across thousands of commodity servers.

* [Dynamo: Amazon’s Highly Available Key-value Store](http://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf) (2007)

> This paper presents the design and implementation of Dynamo, a
> highly available key-value storage system that some of Amazon’s core
> services use to provide an “always-on” experience.

* [Spanner: Google’s Globally-Distributed Database](http://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf) (2012)

> Spanner is Google’s scalable, multi-version, globallydistributed,
> and synchronously-replicated database.  It is the first system to
> distribute data at global scale and support externally-consistent
> distributed transactions.

## Distributed System

* [The Google File System](http://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf) (2003)

> We have designed and implemented the Google File System, a scalable
> distributed file system for large distributed data-intensive
> applications.  It provides fault tolerance while running on
> inexpensive commodity hardware, and it delivers high aggregate
> performance to a large number of clients.

* [MapReduce: Simplified Data Processing on Large Clusters](http://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf) (2004)

> MapReduce is a programming model and an associated implementation
> for processing and generating large data sets.

* [The Chubby lock service for loosely-coupled distributed systems](http://static.googleusercontent.com/media/research.google.com/en//archive/chubby-osdi06.pdf) (2006)

> We describe our experiences with the Chubby lock service, which is
> intended to provide coarse-grained locking as well as reliable
> (though low-volume) storage for a loosely-coupled distributed
> system.

* [Large-scale Incremental Processing Using Distributed Transactions and Notifications](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/36726.pdf) (2010)

> Percolator provides cross-row, cross-table transactions with ACID
> snapshot-isolation semantics.

* [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](https://www.cse.buffalo.edu/tech-reports/2014-04.pdf) (2014)

> We propose a hybrid logical clock, HLC, that combines the best of
> logical clocks and physical clocks.  HLC captures the causality
> relationship like logical clocks, and enables easy identification of
> consistent snapshots in distributed systems.

## Consensus Algorithm

### Papers

* [The Part-Time Parliament](http://research.microsoft.com/en-us/um/people/lamport/pubs/lamport-paxos.pdf) (1998)

> The Island of Paxos.

* [Paxos Made Simple](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf) (2001)

> The Paxos algorithm, when presented in plain English, is very
> simple.

* [Fast Paxos](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/tr-2005-112.pdf) (2005)

> Fast Paxos is an extension of the classic Paxos algorithm that
> allows the value to be learned in two message delays.

* [Paxos Made Live - An Engineering Perspective](http://static.googleusercontent.com/media/research.google.com/en//archive/paxos_made_live.pdf) (2007)

> We describe our experience building a fault-tolerant data-base using
> the Paxos consensus algorithm.  Despite the existing literature in
> the field, building such a database proved to be non-trivial.

* [There Is More Consensus in Egalitarian Parliaments](https://www.cs.cmu.edu/~dga/papers/epaxos-sosp2013.pdf) (2013)

> This paper describes the design and implementation of Egalitarian
> Paxos (EPaxos), a new distributed consensus algorithm based on
> Paxos.  EPaxos achieves three goals: (1) optimal commit latency in
> the wide-area when tolerating one and two failures, under realistic
> conditions; (2) uniform load balancing across all replicas (thus
> achieving high throughput); and (3) graceful performance degradation
> when replicas are slow or crash.

* [In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf) (2014)

> Raft is a consensus algorithm for managing a replicated log.  It
> produces a result equivalent to (multi-)Paxos, and it is as
> efficient as Paxos, but its structure is different from Paxos; this
> makes Raft more understandable than Paxos and also provides a better
> foundation for building practical systems.

### Posts

- [Neat Algorithms - Paxos](http://harry.me/blog/2014/12/27/neat-algorithms-paxos/) (2014)

> This is an explanation and demonstration of an extraordinarily neat
> algorithm called Paxos.

### Slides

- [Implementing Replicated Logs with Paxos](https://ramcloud.stanford.edu/~ongaro/userstudy/paxos.pdf) (2013)
