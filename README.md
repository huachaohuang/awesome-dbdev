# Awesome Database Development

Database development is interesting and challenging. You can always find interesting things to learn and challenging problems to solve. You need to know a lot of things and get them right to build a reliable and high-performance database. And it takes time, a lot of time, to think and practice. I have been working on database development for ten years. However, as the proverb goes, *the more I know, the more I realize I don't know.* So, I collect these awesome materials here to review them from time to time. I think it will be helpful to those who share the same interests as me.

## Introduction

- [Readings in Database Systems](http://www.redbook.io/)

  Readings in Database Systems (commonly known as the "Red Book") has offered readers an opinionated take on both classic and cutting-edge research in the field of data management since 1988.

- [Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/)

  In this practical and comprehensive guide, author Martin Kleppmann helps you navigate this diverse landscape by examining the pros and cons of various technologies for processing and storing data. Software keeps changing, but the fundamental principles remain the same. With this book, software engineers and architects will learn how to apply those ideas in practice, and how to make full use of data in modern applications.

- [How does a relational database work](http://coding-geek.com/how-databases-work/) (2015)

- [Elements Of Scale: Composing And Scaling Data Platforms](http://www.benstopford.com/2015/04/28/elements-of-scale-composing-and-scaling-data-platforms/) (2015)

  Today’s data platforms range greatly in complexity. From simple caching layers or polyglotic persistence right through to wholly integrated data pipelines. There are many paths. They go to many different places. In some of these places at least, nice things are found.

  So the aim for this talk is to explain how and why some of these popular approaches work. We’ll do this by first considering the building blocks from which they are composed. These are the intuitions we’ll need to pull together the bigger stuff later on.

- [Apache Kafka, Samza, and the Unix Philosophy of Distributed Data](http://www.confluent.io/blog/apache-kafka-samza-and-the-unix-philosophy-of-distributed-data) (2015)

  One of the things I realised while doing research for my book is that contemporary software engineering still has a lot to learn from the 1970s. As we’re in such a fast-moving field, we often have a tendency of dismissing older ideas as irrelevant – and consequently, we end up having to learn the same lessons over and over again, the hard way. Although computers have got faster, data has got bigger and requirements have become more complex, many old ideas are actually still highly relevant today. In this blog post I’d like to highlight one particular set of old ideas that I think deserves more attention today: the Unix philosophy. I’ll show how this philosophy is very different from the design approach of mainstream databases, and explore what it would look like if modern distributed data systems learnt a thing or two from Unix.

## System programming

- [What Every Programmer Should Know About Memory](papers/cpumemory.pdf) (2007)

  This paper explains the structure of memory subsystems in use on modern commodity hardware, illustrating why CPU caches were developed, how they work, and what programs should do to achieve optimal performance by utilizing them.

- [What Every Systems Programmer Should Know About Concurrency](papers/concurrency.pdf) (2018)

  Seasoned programmers are familiar with tools like mutexes, semaphores, and condition variables. But what makes them work? How do we write concurrent code when we can’t use them, like when we’re working below the operating system in an embedded environment, or when we can’t block due to hard time constraints? And since your system transforms your code into things you didn’t write, running in orders you never asked for, how do multithreaded programs work at all? Concurrency — especially on modern hardware — is a complicated and unintuitive topic, but let’s try to cover some fundamentals.

- [Everything You Always Wanted to Know About Synchronization but Were Afraid to Ask](papers/synchronization.pdf) (2013)

  This paper presents the most exhaustive study of synchronization to date. We span multiple layers, from hardware cache-coherence protocols up to high-level concurrent software. We do so on different types of architectures, from single-socket – uniform and non-uniform – to multi-socket – directory and broadcast-based – many-cores.

### Linux kernel

- [Understanding the Linux Kernel](https://www.oreilly.com/library/view/understanding-the-linux/0596005652/)

- [Understanding the Linux Virtual Memory Manager](https://www.kernel.org/doc/gorman/)

- [ext4 Data Structures and Algorithms](https://www.kernel.org/doc/html/latest/filesystems/ext4/index.html)

  This document attempts to describe the on-disk format for ext4 filesystems. The same general ideas should apply to ext2/3 filesystems as well, though they do not support all the features that ext4 supports, and the fields will be shorter.

- [The Slab Allocator: An Object-Caching Kernel Memory Allocator](papers/slab.pdf) (1994)

  This paper presents a comprehensive design overview of the SunOS 5.4 kernel memory allocator. This allocator is based on a set of object-caching primitives that reduce the cost of allocating complex objects by retaining their state between uses.

## Storage Device

### Media

- [Hard Disk Drive (HDD)](https://en.wikipedia.org/wiki/Hard_disk_drive)
- [How HDD Works](https://www.youtube.com/watch?v=Ep-yM894mQQ) (Video)
- [The Development of HDD Technique](https://www.youtube.com/watch?v=wteUW2sL7bc) (Video)

- [Solid-State Drive (SSD)](https://en.wikipedia.org/wiki/Solid-state_drive)
- [How Flash Memory Works](https://www.youtube.com/watch?v=s7JLXs5es7I) (Video)
- [Coding for SSDs - What every programmer should know about SSDs](http://codecapsule.com/2014/02/12/coding-for-ssds-part-1-introduction-and-table-of-contents/)

### Interface

- [A History of PC Buses - From ISA to PCI Express](https://www.youtube.com/watch?v=qla-5isbK60) (Video)
- [Serial Attached SCSI (SAS)](https://en.wikipedia.org/wiki/Serial_Attached_SCSI)
- [Understanding SCSI](https://www.youtube.com/watch?v=pR7SdrXdT4M) (Video)
- [Serial AT Attachment (SATA)](https://en.wikipedia.org/wiki/Serial_ATA)
- [PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express)
- [NVM Express (NVMe)](https://en.wikipedia.org/wiki/NVM_Express)

## Storage Engine

- [The Five-Minute Rule for Trading Memory for Disc Accesses](papers/five-minute-rule-1987.pdf) (1987)
- [The Five-Minute Rule 10 Years Later, and Other Computer Storage Rules of Thumb](papers/five-minute-rule-1997.pdf) (1997)
- [The Five-Minute Rule 20 Years Later, and How Flash Memory Changes the Rules](papers/five-minute-rule-2007.pdf) (2007)
- [The Five-Minute Rule 30 Years Later, and its Impact on the Storage Hierarchy](papers/five-minute-rule-2017.pdf) (2017)

- [The Design and Implementation of a Log-Structured File System](papers/lfs.pdf) (1991)

  This paper presents a new technique for disk storage management called a log-structured file system. A log-structured file system writes all modifications to disk sequentially in a log-like structure, thereby speeding up both file writing and crash recovery.

- [Efficiently Reclaiming Space in a Log Structured Store](papers/lss.pdf) (2020)

  A log structured store uses a single write I/O for a number of diverse and non-contiguous pages within a large buffer instead of using a write I/O for each page separately. This requires that pages be relocated on every write, because pages are never updated in place. Instead, pages are dynamically remapped on every write. Log structuring was invented for and used initially in file systems. Today, a form of log structuring is used in SSD controllers because an SSD requires the erasure of a large block of pages before flash storage can be reused. No update-in-place requires that the storage for out-of-date pages be reclaimed (garbage collected or “cleaned”). We analyze cleaning performance and introduce a cleaning strategy that uses a new way to prioritize the order in which stale pages are garbage collected. Our cleaning strategy approximates an “optimal cleaning strategy”.

- [SFS: Random Write Considered Harmful in Solid State Drives](papers/sfs.pdf) (2012)

  In this paper, we propose a new file system for SSDs, SFS. First, SFS exploits the maximum write bandwidth of SSD by taking a log-structured approach. SFS transforms all random writes at file system level to sequential ones at SSD level. Second, SFS takes a new data grouping strategy on writing, instead of the existing data separation strategy on segment cleaning. It puts the data blocks with similar update likelihood into the same segment. This minimizes the inevitable segment cleaning overhead in any log-structured file system by allowing the segments to form a sharp bimodal distribution of segment utilization.

- [Cache Craftiness for Fast Multicore Key-Value Storage](papers/masstree.pdf) (2012)

  We present Masstree, a fast key-value database designed for SMP machines. Masstree keeps all data in memory. Its main data structure is a trie-like concatenation of B+-trees, each of which handles a fixed-length slice of a variable-length key. This structure effectively handles arbitrary-length possibly-binary keys, including keys with long shared prefixes. B+-tree fanout was chosen to minimize total DRAM delay when descending the tree and prefetching each tree node. Lookups use optimistic concurrency control, a read-copy-update-like technique, and do not write shared data structures; updates lock only affected nodes. Logging and checkpointing provide consistency and durability. Though some of these ideas appear elsewhere, Masstree is the first to combine them. We discuss design variants and their consequences.

- [The Adaptive Radix Tree: ARTful Indexing for Main-Memory Databases](papers/adaptive-radix-tree.pdf) (2013)

  This paper presents ART, an adaptive radix tree (trie) for efficient indexing in main memory. Its lookup performance surpasses highly tuned, read-only search trees, while supporting very efficient insertions and deletions as well. At the same time, ART is very space efficient and solves the problem of excessive worst-case space consumption, which plagues most radix trees, by adaptively choosing compact and efficient data structures for internal nodes.

- [The ART of Practical Synchronization](papres/artsync.pdf) (2016)

  The performance of transactional database systems is critically dependent on the efficient synchronization of in-memory data structures. The traditional approach, fine-grained locking, does not scale on modern hardware. Lock-free data structures, in contrast, scale very well but are extremely difficult to implement and often require additional indirections. In this work, we argue for a middle ground, i.e., synchronization protocols that use locking, but only sparingly. We synchronize the Adaptive Radix Tree (ART) using two such protocols, Optimistic Lock Coupling and Read-Optimized Write EXclusion (ROWEX). Both perform and scale very well while being much easier to implement than lock-free techniques.

- [MICA: A Holistic Approach to Fast In-Memory Key-Value Storage](papers/mica.pdf) (2014)

  MICA is a scalable in-memory key-value store that han- dles 65.6 to 76.9 million key-value operations per second using a single general-purpose multi-core system. MICA is over 4–13.5x faster than current state-of-the-art systems, while providing consistently high throughput over a variety of mixed read and write workloads.

  MICA takes a holistic approach that encompasses all aspects of request handling, including parallel data access, network request handling, and data structure design, but makes unconventional choices in each of the three domains. First, MICA optimizes for multi-core architectures by enabling parallel access to partitioned data. Second, for efficient parallel data access, MICA maps client requests directly to specific CPU cores at the server NIC level by using client-supplied information and adopts a light-weight networking stack that bypasses the kernel. Finally, MICA’s new data structures—circular logs, lossy concurrent hash indexes, and bulk chaining—handle both read- and write-intensive workloads at low overhead.

- [TinyLFU: A Highly Efficient Cache Admission Policy](papers/tinylfu.pdf) (2017)

  This article proposes to use a frequency-based cache admission policy in order to boost the effectiveness of caches subject to skewed access distributions. Given a newly accessed item and an eviction candidate from the cache, our scheme decides, based on the recent access history, whether it is worth admitting the new item into the cache at the expense of the eviction candidate.

  This concept is enabled through a novel approximate LFU structure called TinyLFU, which maintains an approximate representation of the access frequency of a large sample of recently accessed items. TinyLFU is very compact and lightweight as it builds upon Bloom filter theory.

- [LeanStore: In-Memory Data Management Beyond Main Memory](papers/leanstore.pdf) (2018)

  In this work, we revisit this fundamental dichotomy and design a novel storage manager that is optimized for modern hardware. Our evaluation, which is based on TPC-C and micro benchmarks, shows that our approach has little overhead in comparison with a pure in-memory system when all data resides in main memory. At the same time, like a traditional buffer manager, it is fully transparent and can manage very large data sets effectively. Furthermore, due to low-overhead synchronization, our implementation is also highly scalable on multi-core CPUs.

- [HotRing: A Hotspot-Aware In-Memory Key-Value Store](papers/hotring.pdf) (2020)

  In this paper, we explore hotspot-aware designs for in-memory index structures in KVSes. We first analyze the potential benefits from ideal hotspot-aware indexes, and discuss challenges (i.e., hotspot shift and concurrent access issues) in effectively leveraging hotspot-awareness. Based on these insights, we propose a novel hotspot-aware KVS, named HotRing1, that is optimized for massively concurrent accesses to a small portion of items. HotRing is based on an ordered-ring hash index structure, which provides fast access to hot items by moving head pointers closer to them. It also applies a lightweight strategy to detect hotspot shifts at run-time. HotRing comprehensively adopts lock-free structures in its design, for both common operations (i.e., read, update) and HotRing-specific operations (i.e., hotspot shift detection, head pointer movement and ordered-ring rehash), so that massively concurrent requests can better leverage multi-core architectures. 

- [Cost/Performance in Modern Data Stores](papers/cost-performance.pdf) (2018)

  Data in traditional “caching” data systems resides on secondary storage, and is read into main memory only when operated on. This limits system performance. Main memory data stores with data always in main memory are much faster. But this performance comes at a cost. In this paper, we analyze the costs of both in-memory operations and secondary storage operations where data is not “in cache”. We study the performance impact of cache misses on caching system performance. The analysis considers both execution and storage costs. Based on our analysis, we derive cost/performance results for a data caching system and a main memory system to understand where each demonstrates the best cost per operation, what is driving the cost differences, and the scale of the differences. This analysis (1) provides insight into why data caching systems continue to dominate the market; (2) points to higher performance that does not rely on simply increasing main memory cache size; and (3) suggests a path to lower costs and hence better cost/performance.

- [The Data Calculator: Data Structure Design and Cost Synthesis from First Principles and Learned Cost Models](papers/datacalculator.pdf) (2018)

  Data structures are critical in any data-driven scenario, but they are notoriously hard to design due to a massive design space and the dependence of performance on workload and hardware which evolve continuously. We present a design engine, the Data Calculator, which enables interactive and semi-automated design of data structures. It brings two innovations. First, it offers a set of fine-grained design primitives that capture the first principles of data layout design: how data structure nodes lay data out, and how they are positioned relative to each other. This allows for a structured description of the universe of possible data structure designs that can be synthesized as combinations of those primitives. The second innovation is computation of performance using learned cost models. These models are trained on diverse hardware and data profiles and capture the cost properties of fundamental data access primitives (e.g., random access). With these models, we synthesize the performance cost of complex operations on arbitrary data structure designs without having to: 1) implement the data structure, 2) run the workload, or even 3) access the target hardware.

- [The Case for Learned Index Structures](papers/learned-index.pdf) (2018)

  Indexes are models: a B-Tree-Index can be seen as a model to map a key to the position of a record within a sorted array, a Hash-Index as a model to map a key to a position of a record within an unsorted array, and a BitMap-Index as a model to indicate if a data record exists or not. In this exploratory research paper, we start from this premise and posit that all existing index structures can be replaced with other types of models, including deep-learning models, which we term learned indexes. We theoretically analyze under which conditions learned indexes outperform traditional index structures and describe the main challenges in designing learned index structures.

- [The PGM-index: a fully-dynamic compressed learned index with provable worst-case bounds](papers/pgm-index.pdf) (2020)

  We present the first learned index that supports predecessor, range queries and updates within provably efficient time and space bounds in the worst case. In the (static) context of just predecessor and range queries these bounds turn out to be optimal. We call this learned index the Piecewise Geometric Model index (PGM-index).

### B-tree

- [Cache-Oblivious Streaming B-trees](papers/streaming-btree.pdf) (2007)

  A streaming B-tree is a dictionary that efficiently implements insertions and range queries. We present two cache-oblivious streaming B-trees, the shuttle tree, and  the cache-oblivious lookahead array (COLA).

- [Modern B-Tree Techniques](papers/modern-btree.pdf) (2011)

  This survey reviews the basics of B-trees and of B-tree indexes in databases, transactional techniques and query processing techniques related to B-trees, B-tree utilities essential for database operations, and many optimizations and improvements. It is intended both as a survey and as a reference, enabling researchers to compare index innovations with advanced B-tree techniques and enabling professionals to select features, functions, and tradeoffs most appropriate for their data management challenges.

- [The Bw-Tree: A B-tree for New Hardware Platforms](papers/bwtree.pdf) (2013)

  Our new form of B-tree, called the Bw-tree achieves its very high performance via a latch-free approach that effectively exploits the processor caches of modern multi-core chips. Our storage manager uses a unique form of log structuring that blurs the distinction between a page and a record store and works well with flash storage. This paper describes the architecture and algorithms for the Bw-tree, focusing on the main memory aspects.

- [Building a Bw-Tree Takes More Than Just Buzz Words](papers/open-bwtree.pdf) (2018)

  This paper has two contributions: First, it is the missing guide for how to build a lock-free Bw-Tree. We clarify missing points in Microsoft’s original design documents and then present techniques to improve the index’s performance. Although our focus here is on the Bw-Tree, many of our methods apply more broadly to designing and implementing future lock-free in-memory data structures. Our experimental evaluation shows that our optimized variant achieves 1.1–2.5× better performance than the original Microsoft proposal for highly concurrent workloads. Second, our evaluation shows that despite our improvements, the Bw-Tree still does not perform as well as other concurrent data structures that use locks.

- [LLAMA: A Cache/Storage Subsystem for Modern Hardware](papers/llama.pdf) (2013)

  LLAMA is a subsystem designed for new hardware environments that supports an API for page-oriented access methods, providing both cache and storage management. Caching (CL) and storage (SL) layers use a common mapping table that separates a page’s logical and physical location. CL supports data updates and management updates (e.g., for index re-organization) via latch-free compare-and-swap atomic state changes on its mapping table. SL uses the same mapping table to cope with page location changes produced by log structuring on every page flush. To demonstrate LLAMA’s suitability, we tailored our latch-free Bw-tree implementation to use LLAMA.

- [Hekaton: SQL Server’s Memory-Optimized OLTP Engine](papers/hekaton.pdf) (2013)

  Hekaton is a new database engine optimized for memory resident data and OLTP workloads. Hekaton is fully integrated into SQL Server; it is not a separate system. To take advantage of Hekaton, a user simply declares a table memory optimized. Hekaton tables are fully transactional and durable and accessed using T-SQL in the same way as regular SQL Server tables. A query can reference both Hekaton tables and regular tables and a transaction can update data in both types of tables. T-SQL stored procedures that reference only Hekaton tables can be compiled into machine code for further performance improvements. The engine is designed for high concurrency. To achieve this it uses only latch-free data structures and a new optimistic, multiversion concurrency control technique. This paper gives an overview of the design of the Hekaton engine and reports some experimental results. 

### LSM-tree

- [The Log-Structured Merge-Tree (LSM-Tree)](papers/lsmtree.pdf) (1996)

  The Log-Structured Merge-tree (LSM-tree) is a disk-based data structure designed to provide low-cost indexing for a file experiencing a high rate of record inserts (and deletes) over an extended period. The LSM-tree uses an algorithm that defers and batches index changes, cascading the changes from a memory-based component through one or more disk components in an efficient manner reminiscent of merge sort. During this process all index values are continuously accessible to retrievals (aside from very short locking periods), either through the memory component or one of the disk components. The algorithm has greatly reduced disk arm movements compared to a traditional access methods such as B-trees, and will improve cost-performance in domains where disk arm costs for inserts with traditional access methods overwhelm storage media costs.

- [bLSM: A General Purpose Log Structured Merge Tree](papers/blsm.pdf) (2012)

  We begin by presenting a new performance metric: read fanout, and argue that, with read and write amplification, it better characterizes real-world indexes than approaches such as asymptotic analysis and price/performance. We then present bLSM, a Log Structured Merge (LSM) tree with the advantages of B-Trees and log structured approaches.

- [WiscKey: Separating Keys from Values in SSD-Conscious Storage](papers/wisckey.pdf) (2016)

  We present WiscKey, a persistent LSM-tree-based key-value store with a performance-oriented data layout that separates keys from values to minimize I/O amplification. The design of WiscKey is highly SSD optimized, leveraging both the sequential and random performance characteristics of the device.

- [PebblesDB: Building Key-Value Stores using Fragmented Log-Structured Merge Trees](papers/pebblesdb.pdf) (2017)

  This paper presents a novel data structure that is inspired by Skip Lists, termed Fragmented Log-Structured Merge Trees (FLSM). FLSM introduces the notion of guards to organize logs, and avoids rewriting data in the same level.

- [Monkey: Optimal Navigable Key-Value Store](papers/monkey.pdf) (2017)

  This paper presents Monkey, an LSM-based key-value store that strikes the optimal balance between the costs of updates and lookups with any given main memory budget. The insight is that worst-case lookup cost is proportional to the sum of the false positive rates of the Bloom filters across all levels of the LSM-tree. Contrary to state-of-the-art key-value stores that assign a fixed number of bits-per-element to all Bloom filters, Monkey allocates memory to filters across different levels so as to minimize this sum.

- [Dostoevsky: Better Space-Time Trade-Offs for LSM-Tree Based Key-Value Stores via Adaptive Removal of Superfluous Merging](papers/dostoevsky.pdf) (2018)

  We introduce Lazy Leveling, a new design that removes merge operations from all levels of LSM-tree but the largest. Lazy Leveling improves the worst-case complexity of update cost while maintaining the same bounds on point lookup cost, long range lookup cost, and storage space. We further introduce Fluid LSM-tree, a generalization of the entire LSM-tree design space that can be parameterized to assume any existing design.

- [The Log-Structured Merge-Bush & the Wacky Continuum](papers/wackyandthebush.pdf) (2019)

  We introduce the Log-Structured Merge-Bush (LSM-Bush), a new data structure that sets increasing capacity ratios between adjacent pairs of smaller levels. We further introduce Wacky, a design continuum that includes LSM-Bush as well as all state-of-the-art merge policies, from laziest to greediest, and can assume any of them within a single implementation.

- [LSM-based storage techniques: a survey](papers/lsmsurvey.pdf) (2019)

  In this paper, we provide a survey of recent research efforts on LSM-trees so that readers can learn the state of the art in LSM-based storage techniques. We provide a general taxonomy to classify the literature of LSM-trees, survey the efforts in detail, and discuss their strengths and trade-offs. We further survey several representative LSM-based open-source NoSQL systems and discuss some potential future research directions resulting from the survey.

- [X-Engine: An Optimized Storage Engine for Large-scale E-commerce Transaction Processing](papers/xengine.pdf) (2019)

  We introduce X-Engine, a write-optimized storage engine of POLARDB built at Alibaba, which utilizes a tiered storage architecture with the LSM-tree (log-structured merge tree) to leverage hardware acceleration such as FPGA-accelerated compactions, and a suite of optimizations including asynchronous writes in transactions, multi-staged pipelines and incremental cache replacement during compactions.

- [MyRocks: LSM-Tree Database Storage Engine Serving Facebook's Social Graph](papers/myrocks.pdf) (2020)

  In this paper, we describe our journey to build and run an OLTP LSM-tree SQL database at scale. We also discuss the features we implemented to keep pace with UDB workloads, what made migrations easier, and what operational and software development challenges we faced during the two years of running MyRocks in production.

### Hash table

- [Bitcask: A Log-Structured Hash Table for Fast Key/Value Data](papers/bitcask.pdf) (2010)

- [SILT: A Memory-Efficient, High-Performance Key-Value Store](papers/silt.pdf) (2011)

  SILT (Small Index Large Table) is a memory-efficient, high-performance key-value store system based on flash storage that scales to serve billions of key-value items on a single node. It requires only 0.7 bytes of DRAM per entry and retrieves key/value pairs using on average 1.01 flash reads each. SILT combines new algorithmic and systems techniques to balance the use of memory, storage, and computation. Our contributions include: (1) the design of three basic key-value stores each with a different emphasis on memory-efficiency and write-friendliness; (2) synthesis of the basic key-value stores to build a SILT key-value store system; and (3) an analytical model for tuning system parameters carefully to meet the needs of different workloads. SILT requires one to two orders of magnitude less memory to provide comparable throughput to current high-performance key-value systems on a commodity desktop system with flash storage.

- [Faster: A Concurrent Key-Value Store with In-Place Updates](papers/faster.pdf) (2018)

  This paper presents Faster, a new key-value store for point read, blind update, and read-modify-write operations. Faster combines a highly cache-optimized concurrent hash index with a hybrid log: a concurrent log-structured record store that spans main memory and storage, while supporting fast in-place updates of the hot set in memory.

## Relational database

### SQL

- [Access Path Selection in a Relational Database Management System](papers/systemr.pdf) (1979)

  In a high level query and data manipulation language such as SQL, requests are stated non-procedurally, without reference to access paths. This paper describes how System R chooses access paths for both simple (single relation) and complex queries (such as joins), given a user specification of desired data as a boolean expression of predicates. System R is an experimental database management system developed to carry out research on the relational model of data.

- [The Volcano Optimizer Generator: Extensibility and Efficient Search](papers/volcano.pdf) (1993)

  Emerging database application domains demand not only new functionality but also high performance. To satisfy these two requirements, the Volcano project provides efficient, extensible toolsfor query and request processing, particularly for object-oriented and scientific database systems. One of these tools is a new optimizer generator. Data model, logical algebra, physical algebra, and optimization rules are translated by the optimizer generator into optimizer source code. Compared with our earlier EXODUS optimizer generator prototype, the search engine is more extensible and powerful; it provides effective support for non-trivial cost models and for physical properties such as sort order. At the same time, it is much more efficient as it combines dynamic programming, which until now had been used only for relational select-project-join optimization, with goal-directed search and branch-and-bound pruning. Compared with other rule-based optimization systems, it provides complete data model independence and more natural extensibility.

- [The Cascades Framework for Query Optimization](papers/cascades.pdf) (1995)

  This paper describes a new extensible query optimization framework that resolves many of the shortcomings of the EXODUS and Volcano optimizer generators. In addition to extensibility, dynamic programming, and memorization based on and extended from the EXODUS and Volcano prototypes, this new optimizer provides (i) manipulation of operator arguments using rules or functions, (ii) operators that are both logical and physical for predicates etc., (iii) schema-specific rules for materialized views, (iv) rules to insert "enforcers" or "glue operators," (v) rule-specific guidance, permitting grouping of rules, (vi) basic facilities that will later permit parallel search, partially ordered cost measures, and dynamic plans, (vii) extensive tracing support, and (viii) a clean interface and implementation making full use of the abstraction mechanisms of C++. We describe and justify our design choices for each of these issues. The optimizer system described here is operational and will serve as the foundation for new query optimizers in Tandem’s NonStop SQL product and in Microsoft’s SQL Server product.

- [How We Built a Cost-Based SQL Optimizer](https://www.cockroachlabs.com/blog/building-cost-based-sql-optimizer/) (Cockroach Labs, 2018)
- [How We Built a Vectorized SQL Engine](https://www.cockroachlabs.com/blog/how-we-built-a-vectorized-sql-engine/) (Cockroach Labs, 2019)

### OLTP

- [The End of an Architectural Era (It’s Time for a Complete Rewrite)](papers/hstore.pdf) (2007)

  In previous papers, some of us predicted the end of “one size fits all” as a commercial relational DBMS paradigm. These papers presented reasons and experimental evidence that showed that the major RDBMS vendors can be outperformed by 1-2 orders of magnitude by specialized engines in the data warehouse, stream processing, text, and scientific database markets.

  Assuming that specialized engines dominate these markets over time, the current relational DBMS code lines will be left with the business data processing (OLTP) market and hybrid markets where more than one kind of capability is required. In this paper we show that current RDBMSs can be beaten by nearly two orders of magnitude in the OLTP market as well. The experimental evidence comes from comparing a new OLTP prototype, H-Store, which we have built at M.I.T., to a popular RDBMS on the standard transactional benchmark, TPC-C.

  We conclude that the current RDBMS code lines, while attempting to be a “one size fits all” solution, in fact, excel at nothing. Hence, they are 25 year old legacy code lines that should be retired in favor of a collection of “from scratch” specialized engines. The DBMS vendors (and the research community) should start with a clean sheet of paper and design systems for tomorrow’s requirements, not continue to push code lines and architectures designed for yesterday’s needs.

- [Megastore: Providing Scalable, Highly Available Storage for Interactive Services](papers/megastore.pdf) (2011)

  Megastore is a storage system developed to meet the requirements of today's interactive online services. Megastore blends the scalability of a NoSQL datastore with the convenience of a traditional RDBMS in a novel way, and provides both strong consistency guarantees and high availability. We provide fully serializable ACID semantics within fine-grained partitions of data. This partitioning allows us to synchronously replicate each write across a wide area network with reasonable latency and support seamless failover between datacenters. This paper describes Megastore's semantics and replication algorithm. It also describes our experience supporting a wide range of Google production services built with Megastore.

- [Spanner: Google’s Globally-Distributed Database](papers/spanner-2012.pdf) (2012)

  Spanner is Google’s scalable, multi-version, globally-distributed, and synchronously-replicated database. It is the first system to distribute data at global scale and support externally-consistent distributed transactions. This paper describes how Spanner is structured, its feature set, the rationale underlying various design decisions, and a novel time API that exposes clock uncertainty. This API and its implementation are critical to supporting external consistency and a variety of powerful features: non-blocking reads in the past, lock-free read-only transactions, and atomic schema changes, across all of Spanner.

- [F1: A Distributed SQL Database That Scales](papers/f1.pdf) (2013)

  F1 is a distributed relational database system built at Google to support the AdWords business. F1 is a hybrid database that combines high availability, the scalability of NoSQL systems like Bigtable, and the consistency and usability of traditional SQL databases. F1 is built on Spanner, which provides synchronous cross-datacenter replication and strong consistency. Synchronous replication implies higher commit latency, but we mitigate that latency by using a hierarchical schema model with structured data types and through smart application design. F1 also includes a fully functional distributed SQL query engine andautomatic change tracking and publishing.

- [Online, Asynchronous Schema Change in F1](papers/f1-schema.pdf) (2013)

  We introduce a protocol for schema evolution in a globally distributed database management system with shared data, stateless servers, and no global membership. Our protocol is asynchronous — it allows different servers in the database system to transition to a new schema at different times — and online—all servers can access and update all data during a schema change. We provide a formal model for determining the correctness of schema changes under these conditions, and we demonstrate that many common schema changes can cause anomalies and database corruption. We avoid these problems by replacing corruption - causing schema changes with a sequence of schema changes that is guaranteed to avoid corrupting the database so long as all servers are no more than one schema version behind at any time. Finally, we discuss a practical implementation of our protocol in F1, the database management system that stores data for Google AdWords.

- [Spanner: Becoming a SQL System](papers/spanner-2017.pdf) (2017)

  Spanner is a globally-distributed data management system that backs hundreds of mission-critical services at Google. Spanner is built on ideas from both the systems and database communities. The first Spanner paper published at OSDI’12 focused on the systems aspects such as scalability, automatic sharding, fault tolerance, consistent replication, external consistency, and wide-area distribution. This paper highlights the database DNA of Spanner. We describe distributed query execution in the presence of resharding, query restarts upon transient failures, range extraction that drives query routing and index seeks, and the improved blockwise-columnar storage format. We touch upon migrating Spanner to the common SQL dialect shared with other systems at Google.

- [Amazon Aurora: Design Considerations for High Throughput Cloud-Native Relational Databases](papers/aurora-2017.pdf) (2017)

  Amazon Aurora is a relational database service for OLTP workloads offered as part of Amazon Web Services (AWS). In this paper, we describe the architecture of Aurora and the design considerations leading to that architecture. We believe the central constraint in high throughput data processing has moved from compute and storage to the network. Aurora brings a novel architecture to the relational database to address this constraint, most notably by pushing redo processing to a multi-tenant scale-out storage service, purpose-built for Aurora. We describe how doing so not only reduces network traffic, but also allows for fast crash recovery, failovers to replicas without loss of data, and fault-tolerant, self-healing storage. We then describe how Aurora achieves consensus on durable state across numerous storage nodes using an efficient asynchronous scheme, avoiding expensive and chatty recovery protocols.

- [Amazon Aurora: On Avoiding Distributed Consensus for I/Os, Commits, and Membership Changes](papers/aurora-2018.pdf) (2018)

  Amazon Aurora is a high-throughput cloud-native relational database offered as part of Amazon Web Services (AWS). One of the more novel differences between Aurora and other relational databases is how it pushes redo processing to a multi-tenant scale-out storage service, purpose-built for Aurora. Doing so reduces networking traffic, avoids checkpoints and crash recovery, enables failovers to replicas without loss of data, and enables fault-tolerant storage that heals without database involvement. Traditional implementations that leverage distributed storage would use distributed consensus algorithms for commits, reads, replication, and membership changes and amplify cost of underlying storage. In this paper, we describe how Aurora avoids distributed consensus under most circumstances by establishing invariants and leveraging local transient state. Doing so improves performance, reduces variability, and lowers costs.

- [Socrates: The New SQL Server in the Cloud](papers/socrates.pdf) (SIGMOD, 2019)

  This paper presents a novel DBaaS architecture, called Socrates. Socrates has been implemented in Microsoft SQL Server and is available in Azure as SQL DB Hyperscale. This paper describes the key ideas and features of Socrates, and it compares the performance of Socrates with the previous SQL DB offering in Azure.

- [CockroachDB: The Resilient Geo-Distributed SQL Database](papers/cockroachdb.pdf) (SIGMOD, 2020)

  CockroachDB is a scalable SQL DBMS that was built from the ground up to support these global OLTP workloads while maintaining high availability and strong consistency. Just like its namesake, CockroachDB is resilient to disasters through replication and automatic recovery mechanisms.

  This paper presents the design of CockroachDB and its novel transaction model that supports consistent geo-distributed transactions on commodity hardware. We describe how CockroachDB replicates and distributes data to achieve fault tolerance and high performance, as well as how its distributed SQL layer automatically scales with the size of the database cluster while providing the standard SQL interface that users expect.

- [How CockroachDB Does Distributed, Atomic Transactions](https://www.cockroachlabs.com/blog/how-cockroachdb-distributes-atomic-transactions/) (Cockroach Labs, 2015)
- [How online schema changes are possible in CockroachDB](https://www.cockroachlabs.com/blog/how-online-schema-changes-are-possible-in-cockroachdb/) (Cockroach Labs, 2016)
- [Living Without Atomic Clocks](https://www.cockroachlabs.com/blog/living-without-atomic-clocks/) (Cockroach Labs, 2016)
- [Serializable, Lockless, Distributed: Isolation in CockroachDB](https://www.cockroachlabs.com/blog/serializable-lockless-distributed-isolation-cockroachdb/) (Cockroach Labs, 2016)
- [CockroachDB’s Consistency Model](https://www.cockroachlabs.com/blog/consistency-model/) (Cockroach Labs, 2019)

### OLAP

- [C-Store: A Column-oriented DBMS](papers/c-store.pdf) (2005)

  This paper presents the design of a read-optimized relational DBMS that contrasts sharply with most current systems, which are write-optimized. Among the many differences in its design are: storage of data by column rather than by row, careful coding and packing of objects into storage including main memory during query processing, storing an overlapping collection of column-oriented projections, rather than the current fare of tables and indexes, a non-traditional implementation of transactions which includes high availability and snapshot isolation for read-only transactions, and the extensive use of bitmap indexes to complement B-tree structures.

- [MonetDB/X100: Hyper-Pipelining Query Execution](papers/monetdb.pdf) (2005)

  Database systems tend to achieve only low IPC (instructions-per-cycle) efficiency on modern CPUs in compute-intensive application areas like decision support, OLAP and multimedia retrieval. This paper starts with an in-depth investigation to the reason why this happens, focusing on the TPC-H benchmark. Our analysis of various relational systems and MonetDB leads us to a new set of guidelines for designing a query processor.

  The second part of the paper describes the architecture of our new X100 query engine for the MonetDB system that follows these guidelines. On the surface, it resembles a classical Volcano-style engine, but the crucial difference to base all execution on the concept of vector processing makes it highly CPU efficient.

- [Database Cracking](papers/database-cracking.pdf) (2007)

  Database indices provide a non-discriminative navigational infrastructure to localize tuples of interest. Their mainte- nance cost is taken during database updates. In this pa- per, we study the complementary approach, addressing in- dex maintenance as part of query processing using continu- ous physical reorganization, i.e., cracking the database into manageable pieces. The motivation is that by automatically organizing data the way users request it, we can achieve fast access and the much desired self-organized behavior.

  We present the first mature cracking architecture and re- port on our implementation of cracking in the context of a full fledged relational system. It led to a minor enhancement to its relational algebra kernel, such that cracking could be piggy-backed without incurring too much processing over- head. Furthermore, we illustrate the ripple effect of dynamic reorganization on the query plans derived by the SQL opti- mizer. The experiences and results obtained are indicative of a significant reduction in system complexity. We show that the resulting system is able to self-organize based on incom- ing requests with clear performance benefits. This behavior is visible even when the user focus is randomly shifting to different parts of the data.

- [Dremel: Interactive Analysis of Web-Scale Datasets](papers/dremel.pdf) (2010)

  Dremel is a scalable, interactive ad-hoc query system for analysis of read-only nested data. By combining multi-level executiontrees and columnar data layout, it is capable of running aggregation queries over trillion-row tables in seconds. The system scales to thousands of CPUs and petabytes of data, and has thousands of users at Google.  In this paper, we describe the architecture and implementation of Dremel, and explain how it complements MapReduce-based computing. We present a novel columnar storage representation for nested records and discuss experiments on few-thousand node instances of the system.

- [The Design and Implementation of Modern Column-Oriented Database Systems](papers/modern-column-stores.pdf) (2013)

  In this article, we survey recent research on column-oriented database systems, or column-stores, where each attribute of a table is stored in a separate file or region on storage. Such databases have seen a resurgence in recent years with a rise in interest in analytic queries that perform scans and aggregates over large portions of a few columns of a table. The main advantage of a column-store is that it can access just the columns needed to answer such queries. We specifically focus on three influential research prototypes, MonetDB, VectorWise, and C-Store. These systems have formed the basis for several well-known commercial column-store implementations. We describe their similarities and differences and discuss their specific architectural features for compression, late materialization, join processing, vectorization and adaptive indexing (database cracking).

- [The Snowflake Elastic Data Warehouse](papers/snowflake.pdf) (2016)

  Snowflake is a multi-tenant, transactional, secure, highly scalable and elastic system with full SQL support and built-in extensions for semi-structured and schema-less data. The system is offered as a pay-as-you-go service in the Amazon cloud. Users upload their data to the cloud and can immediately manage and query it using familiar tools and interfaces.

  In this paper, we describe the design of Snowflake and its novel multi-cluster, shared-data architecture. The paper highlights some of the key features of Snowflake: extreme elasticity and availability, semi-structured and schema-less data, time travel, and end-to-end security. It concludes with lessons learned and an outlook on ongoing work.

- [AnalyticDB: Real-time OLAP Database System at Alibaba Cloud](papers/analyticdb.pdf) (2019)

  In this paper, we introduce AnalyticDB, a real-time OLAP database system developed at Alibaba. AnalyticDB maintains all-column indexes in an asynchronous manner with acceptable overhead, which provides low latency for complex ad-hoc queries. Its storage engine extends hybrid row-column layout for fast retrieval of both structured data and data of complex types. To handle large-scale data with high query concurrency and write throughput, AnalyticDB decouples read and write access paths. To further reducequery latency, novel storage-aware SQL optimizer and execution engine are developed to fully utilize the advantages of the underlying storage and indexes.

- [Delta Lake: High-Performance ACID Table Storage over Cloud Object Stores](papers/deltalake.pdf) (2021)

  Cloud object stores such as Amazon S3 are some of the largest and most cost-effective storage systems on the planet, making them an attractive target to store large data warehouses and data lakes. Unfortunately, their implementation as key-value stores makes it difficult to achieve ACID transactions and high performance: metadata operations such as listing objects are expensive, and consistency guarantees are limited. In this paper, we present Delta Lake, an open source ACID table storage layer over cloud object stores initially developed at Databricks. Delta Lake uses a transaction log that is compacted into Apache Parquet format to provide ACID properties, time travel, and significantly faster metadata operations for large tabular datasets (e.g., the ability to quickly search billions of table partitions for those relevant to a query). It also leverages this design to provide high-level features such as automatic data layout optimization, upserts, caching, and audit logs. Delta Lake tables can be accessed from Apache Spark, Hive, Presto, Redshift and other systems. Delta Lake is deployed at thousands of Databricks customers that process exabytes of data per day, with the largest instances managing exabyte-scale datasets and billions of objects.

- [Amazon Redshift Re-invented](papers/redshift-reinvented.pdf) (2022)

  In the last few years, the use cases for Amazon Redshift have evolved and in response, the service has delivered and continues to deliver a series of innovations that delight customers. Through architectural enhancements, Amazon Redshift has maintained its industry-leading performance. Redshift improved storage and compute scalability with innovations such as tiered storage, multi-cluster auto-scaling, cross-cluster data sharing and the AQUA query acceleration layer. Autonomics have made Amazon Redshift easier to use. Amazon Redshift Serverless is the culmination of autonomics effort, which allows customers to run and scale analytics without the need to set up and manage data warehouse infrastructure. Finally, Amazon Redshift extends beyond traditional data warehousing workloads, by integrating with the broad AWS ecosystem with features such as querying the data lake with Spectrum, semistructured data ingestion and querying with PartiQL, streaming ingestion from Kinesis and MSK, Redshift ML, federated queries to Aurora and RDS operational databases, and federated materialized views.

### HTAP

- [TiDB: A Raft-based HTAP Database](papers/tidb.pdf) (2020)

  We propose extending replicated state machine-based consensus algorithms to provide consistent replicas for HTAP workloads. Based on this novel idea, we present a Raft-based HTAP database: TiDB. In the database, we design a multi-Raft storage system which consists of a row store and a column store. The row store is built based on the Raft algorithm. It is scalable to materialize updates from transactional requests with high availability. In particular, it asynchronously replicates Raft logs to learners which transform row format to column format for tuples, forming a real-time updatable column store. This column store allows analytical queries to efficiently read fresh and consistent data with strong isolation from transactions on the row store. Based on this storage system, we build an SQL engine to process large-scale distributed transactions and expensive analytical queries. The SQL engine optimally accesses row-format and column-format replicas of data.

### HSAP

- [Procella: Unifying serving and analytical data at YouTube](papers/procella.pdf) (2019)

  Large organizations like YouTube are dealing with exploding data volume and increasing demand for data driven applications. Broadly, these can be categorized as: reporting and dashboarding, embedded statistics in pages, time-series monitoring, and ad-hoc analysis. Typically, organizations build specialized infrastructure for each of these use cases. This, however, creates silos of data and processing, and results in a complex, expensive, and harder to maintain infrastructure.

  At YouTube, we solved this problem by building a new SQL query engine – Procella. Procella implements a superset of capabilities required to address all of the four use cases above, with high scale and performance, in a single product. Today, Procella serves hundreds of billions of queries per day across all four workloads at YouTube and several other Google product areas.

- [Alibaba Hologres: A Cloud-Native Service for Hybrid Serving/Analytical Processing](papers/hologres.pdf) (2020)

  In this work, we propose Hologres, which is a cloud native service for hybrid serving and analytical processing (HSAP). Hologres decouples the computation and storage layers, allowing flexible scaling in each layer. Tables are partitioned into self-managed shards. Each shard processes its read and write requests concurrently independent of each other. Hologres leverages hybrid row/column storage to optimize operations such as point lookup, column scan and data ingestion used in HSAP. We propose Execution Context as a resource abstraction between system threads and user tasks. Execution contexts can be cooperatively scheduled with little context switching overhead. Queries are parallelized and mapped to execution contexts for concurrent execution. The scheduling framework enforces resource isolation among different queries and supports customizable schedule policy.

## Replication

- [Paxos Made Simple](papers/paxos-made-simple.pdf) (2001)

  The Paxos algorithm, when presented in plain English, is very simple.

- [Paxos Made Live - An Engineering Perspective](papers/paxos-made-live.pdf) (2007)

  We used the Paxos algorithm (“Paxos”) as the base for a framework that implements a fault-tolerant log. We then relied on that framework to build a fault-tolerant database. This paper discusses a selection of the algorithmic and engineering challenges we encountered in moving Paxos from theory to practice.

- [There Is More Consensus in Egalitarian Parliaments](papers/epaxos.pdf) (2013)

  This paper describes the design and implementation of Egalitarian Paxos (EPaxos), a new distributed consensus algorithm based on Paxos. EPaxos achieves three goals: (1) optimal commit latency in the wide-area when toler- ating one and two failures, under realistic conditions; (2) uniform load balancing across all replicas (thus achieving high throughput); and (3) graceful performance degrada- tion when replicas are slow or crash.

- [Paxos Quorum Leases: Fast Reads Without Sacrificing Writes](papers/paxos-quorum-leases.pdf) (2014)

  This paper describes quorum leases, a new technique that allows Paxos-based systems to perform reads with high throughput and low latency. Quorum leases do not sacrifice consistency and have only a small impact on system availability and write latency. Quorum leases allow a majority of replicas to perform strongly consistent local reads, which substantially reduces read latency at those replicas (e.g., by two orders of magnitude in wide-area scenarios). Previous techniques for performing local reads in Paxos systems either (a) sacrifice consistency; (b) allow only one replica to read locally; or (c) decrease the availability of the system and increase the latency of all updates by requiring all replicas to be notified synchronously.

- [In Search of an Understandable Consensus Algorithm](papers/raft.pdf) (2014)

  Raft is a consensus algorithm for managing a replicated log. It produces a result equivalent to (multi-)Paxos, and it is as efficient as Paxos, but its structure is different from Paxos; this makes Raft more understandable than Paxos and also provides a better foundation for building practical systems. In order to enhance understandability, Raft separates the key elements of consensus, such as leader election, log replication, and safety, and it enforces a stronger degree of coherency to reduce the number of states that must be considered. Results from a user study demonstrate that Raft is easier for students to learn than Paxos. Raft also includes a new mechanism for changing the cluster membership, which uses overlapping majorities to guarantee safety.

- [Weighted Voting for Replicated Data](papers/quorum.pdf) (1979)

  In a new algorithm for maintaining replicated data, every copy of a replicated file is assigned some number of votes. Every transaction collects a read quorum of r votes to read a file, and a write quorum of w votes to write a file, such that r+w is greater than the total number of votes assigned to the file. This ensures that there is a non-null intersection between every read quorum and every write quorum. Version numbers make it possible to determine which copies are current. The reliability and performance characteristics of a replicated file can be controlled by appropriately choosing r, w, and the file's voting configuration. The algorithm guarantees serial consistency, admits temporary copies in a natural way by the introduction of copies with no votes, and has been implemented in the context of an application system called Violet.

- [Chain Replication for Supporting High Throughput and Availability](papers/chain-replication.pdf) (2004)

  Chain replication is a new approach to coordinating clusters of fail-stop storage servers. The approach is intended for supporting large-scale storage services that exhibit high throughput and availability without sacrificing strong consistency guarantees. Besides outlining the chain replication protocols themselves, simulation experiments explore the performance characteristics of a prototype implementation. Throughput, availability, and several object-placement strategies (including schemes based on distributed hash table routing) are discussed.

- [Conflict-free Replicated Data Types](papers/crdt.pdf) (2011)

  Under a formal Strong Eventual Consistency (SEC) model, we study sufficient conditions for convergence. A data type that satisfies these conditions is called a Conflict-free Replicated Data Type (CRDT). Replicas of any CRDT are guaranteed to converge in a self-stabilising manner, despite any number of failures. This paper formalises two popular approaches (state- and operation-based) and their relevant sufficient conditions. We study a number of useful CRDTs, such as sets with clean semantics, supporting both add and remove operations, and consider in depth the more complex Graph data type. CRDT types can be composed to develop large-scale distributed applications, and have interesting theoretical properties.

## Transaction

- [Granularity of Locks and Degrees of Consistency in a Shared Data Base](papers/locks.pdf) (1975)

  The first part of this paper introduces a locking protocol that allows simultaneous locking at various granularities in a database with a hierarchical structure. The second part of this paper introduces four degrees of consistency and the relationships of the four degrees to the locking protocol.

- [The Notion of Consistency and Predicate Locks in a Database System](papers/predicate-locks.pdf) (1976)

  In database systems, users access shared data under the assumption that the data satisfies certain consistency constraints. This paper defines the concepts of transaction, consistency and schedule and shows that consistency requires that a transaction cannot request new locks after releasing a lock. Then it is argued that a transaction needs to lock a logical rather than a physical subset of the database. These subsets may be specified by predicates. An implementation of predicate locks which satisfies the consistency condition is suggested.

- [How to Make a Multiprocessor Computer That Correctly Executes Multiprocess Program](papers/sequential-consistency.pdf) (1979)

  I forget what prompted me to be thinking about memory caching, but it occurred to me one day that multiprocessor synchronization algorithms assume that each processor accesses the same word in memory, but each processor actually accesses its own copy in its cache. It hardly required a triple-digit IQ to realize that this could cause problems. I suppose what made this paper worth reading was its simple, precise definition of sequential consistency as the required correctness condition. This was not the first paper about cache coherence. However, it is the early paper most often cited in the cache-coherence literature.

- [Linearizability: A Correctness Condition for Concurrent Objects](papers/linearizability.pdf) (1990)

  A concurrent object is a data object shared by concurrent processes. Linearizability is a correctness condition for concurrent objects that exploits the semantics of abstract data types. It permits a high degree of concurrency, yet it permits programmers to specify and reason about concurrent objects using known techniques from the sequential domain. Linearizability provides the illusion that each operation applied by concurrent processes takes effect instantaneously at some point between its invocation and its response, implying that the meaning of a concurrent object’s operations can be given by pre- and post-conditions. This paper defines linearizability, compares it to other correctness conditions, presents and demonstrates a method for proving the correctness of implementations, and shows how to reason about concurrent objects, given they are linearizable.

- [Linearizability versus Serializability](http://www.bailis.org/blog/linearizability-versus-serializability/) (2014)

  Linearizability and serializability are both important properties about interleavings of operations in databases and distributed systems, and it’s easy to get them confused. This post gives a short, simple, and hopefully practical overview of the differences between the two.

- [Session Guarantees for Weakly Consistent Replicated Data](papers/session-guarantees.pdf) (1994)

  Four per-session guarantees are proposed to aid users and applications of weakly consistent replicated data: Read Your Writes, Monotonic Reads, Writes Follow Reads, and Monotonic Writes. The intent is to present individual applications with a view of the database that is consistent with their own actions, even if they read and write from various, potentially inconsistent servers. The guarantees can be layered on existing systems that employ a read-any/write-any replication scheme while retaining the principal benefits of such a scheme, namely high-availability, simplicity, scalability, and support for disconnected operation. These session guarantees were developed in the context of the Bayou project at Xerox PARC in which we are designing and building a replicated storage system to support the needs of mobile computing users who may be only intermittently connected.

- [Causal Memory: Definitions, Implementation and Programming](papers/causal-consistency.pdf) (1995)

  The abstraction of a shared memory is of growing importance in distributed computing systems. Traditional memory consistency ensures that all processes agree on a common order of all operations on memory. Unfortunately, providing these guarantees entails access latencies that prevent scaling to large systems. This paper weakens such guarantees by defining causal memory, an abstraction that ensures that processes in a system agree on the relative ordering of operations that are causally related. Because causal memory is weakly consistent, it admits more executions, and hence more concurrency, than either atomic or sequentially consistent memories. This paper provides a formal definition of causal memory and gives an implementation for message-passing systems. In addition, it describes a practical class of programs that, if developed for a strongly consistent memory, run correctly with causal memory.

- [A Critique of ANSI SQL Isolation Levels](papers/snapshot-isolation.pdf) (1995)

  ANSI SQL-92 defines Isolation Levels in terms of phenomena: Dirty Reads, Non-Repeatable Reads, and Phantoms. This paper shows that these phenomena and the ANSI SQL definitions fail to characterize several popular isolation levels, including the standard locking implementations of the levels. Investigating the ambiguities of the phenomena leads to clearer definitions; in addition new phenomena that better characterize isolation types are introduced. An important multiversion isolation type, Snapshot Isolation, is defined.

- [Generalized Isolation Level Definitions](papers/generalized-isolation.pdf) (2000)

  Commercial databases support different isolation levels to allow programmers to trade off consistency for a potential gain in performance. The isolation levels are defined in the current ANSI standard, but the definitions are ambiguous and revised definitions proposed to correct the problem are too constrained since they allow only pessimistic (locking) implementations. This paper presents new specifications for the ANSI levels. Our specifications are portable; they apply not only to locking implementations, but also to optimistic and multi-version concurrency control schemes. Furthermore, unlike earlier definitions, our new specifications handle predicates in a correct and flexible manner at all levels.

- [Serializable Isolation for Snapshot Databases](papers/serializable-snapshot-isolation.pdf) (2008)

  This paper describes a modification to the concurrency control algorithm of a database management system that automatically detects and prevents snapshot isolation anomalies at runtime for arbitrary applications, thus providing serializable isolation. The new algorithm preserves the properties that make snapshot isolation attractive, including that readers do not block writers and vice versa. An implementation and performance study of the algorithm are described, showing that the throughput approaches that of snapshot isolation in most cases.

- [A Critique of Snapshot Isolation](papers/write-snapshot-isolation.pdf) (2012)

  There have been recent attempts to enrich large-scale data stores, such as HBase and BigTable, with transactional support. Not surprisingly, inspired by traditional database management systems, serializability is usually compromised for the benefit of efficiency. For example, Google Percolator, implements lock-based snapshot isolation on top of BigTable. We show in this paper that this compromise is not necessary in lock-free implementations of transactional support. We introduce write-snapshot isolation, a novel isolation level that has a performance comparable with that of snapshot isolation, and yet provides serializability. The main insight in write-snapshot isolation is to prevent read-write conflicts in contrast to write-write conflicts that are prevented by snapshot isolation.

## Distributed transaction

- [Time, Clocks, and the Ordering of Events in a Distributed System](papers/logical-clocks.pdf) (1978)

  The concept of one event happening before another in a distributed system is examined, and is shown to define a partial ordering of the events. A distributed algorithm is given for synchronizing a system of logical clocks which can be used to totally order the events. The use of the total ordering is illustrated with a method for solving synchronization problems. The algorithm is then specialized for synchronizing physical clocks, and a bound is derived on how far out of synchrony the clocks can become.

- [Logical Physical Clocks and Consistent Snapshots in Globally Distributed Databases](papers/hybrid-logical-clocks.pdf) (2014)

  We propose a hybrid logical clock, HLC, that com- bines the best of logical clocks and physical clocks. HLC captures the causality relationship like logical clocks, and enables easy identification of consistent snapshots in dis- tributed systems. Dually, HLC can be used in lieu of phys- ical/NTP clocks since it maintains its logical clock to be always close to the NTP clock. Moreover HLC fits in to 64 bits NTP timestamp format, and is masking toler- ant to NTP kinks and uncertainties. We show that HLC has many benefits for wait-free transaction ordering and performing snapshot reads in multiversion globally dis- tributed databases.

- [Consensus on Transaction Commit](papers/paxos-commit.pdf) (2004)

  The distributed transaction commit problem requires reaching agreement on whether a transaction is committed or aborted. The classic Two-Phase Commit protocol blocks if the coordinator fails. Fault-tolerant consensus algorithms also reach agreement, but do not block whenever any majority of the processes are working. The Paxos Commit algorithm runs a Paxos consensus algorithm on the commit/abort decision of each participant to obtain a transaction commit protocol that uses 2F + 1 coordinators and makes progress if at least F + 1 of them are working properly. Paxos Commit has the same stable-storage write delay, and can be implemented to have the same message delay in the fault-free case, as Two-Phase Commit, but it uses more messages. The classic Two-Phase Commit algorithm is obtained as the special F = 0 case of the Paxos Commit algorithm.

- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](papers/percolator.pdf) (2010)

  We have built Percolator, a system for incrementally processing updates to a large data set, and deployed it to create the Google web search index. By replacing a batch-based indexing system with an indexing system based on incremental processing using Percolator, we process the same number of documents per day, while reducing the average age of documents in Google search results by 50%.

- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](papers/calvin.pdf) (2012)

  Many distributed storage systems achieve high data access throughput via partitioning and replication, each system with its own advantages and tradeoffs. In order to achieve high scalability, however, today’s systems generally reduce transactional support, disallowing single transactions from spanning multiple partitions. Calvin is a practical transaction scheduling and data replication layer that uses a deterministic ordering guarantee to significantly reduce the normally prohibitive contention costs associated with distributed transactions. Unlike previous deterministic database system prototypes, Calvin supports disk-based storage, scales near-linearly on a cluster of commodity machines, and has no single point of failure. By replicating transaction inputs rather than effects, Calvin is also able to support multiple consistency levels—including Paxos-based strong consistency across geographically distant replicas—at no cost to transactional throughput.

- [Highly Available Transactions: Virtues and Limitations](papers/highly-available-transactions.pdf) (2013)

  To minimize network latency and remain online during server failures and network partitions, many modern distributed data storage systems eschew transactional functionality, which provides strong semantic guarantees for groups of multiple operations over multiple data items. In this work, we consider the problem of providing Highly Available Transactions (HATs): transactional guarantees that do not suffer unavailability during system partitions or incur high network latency. We introduce a taxonomy of highly available systems and analyze existing ACID isolation and distributed data consistency guarantees to identify which can and cannot be achieved in HAT systems. This unifies the literature on weak transactional isolation, replica consistency, and highly available systems.

- [Consistency in Non-Transactional Distributed Storage Systems](papers/consistency-overview.pdf) (2016)

  In this paper we aim to fill the void in literature, by providing a structured and comprehensive overview of different consistency notions that appeared in distributed systems, and in particular storage systems research, in the last four decades. We overview more than 50 different consistency notions, ranging from linearizability to eventual and weak consistency, defining precisely many of these, in particular where the previous definitions were ambiguous. We further provide a partial order among different consistency predicates, ordering them by their semantic “strength”, which we believe will reveal useful in future research. Finally, we map the consistency semantics to different practical systems and research prototypes.

- [SLOG: Serializable, Low-latency, Geo-replicated Transactions](papers/slog.pdf) (2019)

  For decades, applications deployed on a world-wide scale have been forced to give up at least one of (1) strict serializability (2) low latency writes (3) high transactional throughput. In this paper we discuss SLOG: a system that avoids this tradeoff for work- loads which contain physical region locality in data access. SLOG achieves high-throughput, strictly serializable ACID transactions at geo-replicated distance and scale for all transactions submitted across the world, all the while achieving low latency for transactions that initiate from a location close to the home region for data they access. Experiments find that SLOG can reduce latency by more than an order of magnitude relative to state-of-the-art strictly serializable geo-replicated database systems such as Spanner and Calvin, while maintaining high throughput under contention.

- [Transactional Causal Consistency for Serverless Computing](papers/transactional-causal-consistency.pdf) (2020)

  We consider the setting of serverless Function-as-a-Service (FaaS) platforms, where storage services are disaggregated from the machines that support function execution. FaaS applications consist of compositions of functions, each of which may run on a separate machine and access remote storage.

  The challenge we address is improving I/O latency in this setting while also providing application-wide consistency. Previous work has explored providing causal consistency for individual I/Os by carefully managing the versions stored in a client-side data cache. In our setting, a single application may execute multiple functions across different nodes, and therefore issue interrelated I/Os to multiple distinct caches. This raises the challenge of Multisite Transactional Causal Consistency (MTCC): the ability to provide causal consistency for all I/Os within a given transaction even if it runs across multiple physical sites. We present protocols for MTCC implemented in a system called HydroCache. Our evaluation demonstrates orders-of-magnitude performance improvements due to caching, while also protecting against consistency anomalies that otherwise arise frequently.

- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html) (2017)
- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html) (2018)
- [Consistency without Clocks: The FaunaDB Distributed Transaction Protocol](https://fauna.com/blog/consistency-without-clocks-faunadb-transaction-protocol) (Fauna, 2018)
- [Demystifying Database Systems, Part 1: An Introduction to Transaction Isolation Levels](https://fauna.com/blog/introduction-to-transaction-isolation-levels) (Fauna, 2019)
- [Demystifying Database Systems, Part 2: Correctness Anomalies Under Serializable Isolation](https://fauna.com/blog/demystifying-database-systems-correctness-anomalies-under-serializable-isolation) (Fauna, 2019)
- [Demystifying Database Systems, Part 3: Introduction to Consistency Levels](https://fauna.com/blog/demystifying-database-systems-introduction-to-consistency-levels) (Fauna, 2019)
- [Demystifying Database Systems, Part 4: Isolation levels vs. Consistency levels](https://fauna.com/blog/demystifying-database-systems-part-4-isolation-levels-vs-consistency-levels) (Fauna, 2019)

## Distributed system

- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web Services](papers/cap-theorem.pdf) (2002)

  When designing distributed web services, there are three properties that are commonly desired: consistency, availability, and partition tolerance. It is impossible to achieve all three. In this note, we prove this conjecture in the asynchronous network model, and then discuss solutions to this dilemma in the partially synchronous model.

- [CAP Twelve Years Later: How the "Rules" Have Changed](https://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed) (2012)

  Although designers still need to choose between consistency and availability when partitions are present, there is an incredible range of flexibility for handling partitions and recovering from them. The modern CAP goal should be to maximize combinations of consistency and availability that make sense for the specific application. Such an approach incorporates plans for operation during a partition and for recovery afterward, thus helping designers think about CAP beyond its historically perceived limitations.

- [The Google File System](papers/gfs.pdf) (2003)

  We have designed and implemented the Google File System, a scalable distributed file system for large distributed data-intensive applications. It provides fault tolerance while running on inexpensive commodity hardware, and it delivers high aggregate performance to a large number of clients.

- [Bigtable: A Distributed Storage System for Structured Data](papers/bigtable.pdf) (2006)

  Bigtable is a distributed storage system for managing structured data that is designed to scale to a very large size: petabytes of data across thousands of commodity servers. Many projects at Google store data in Bigtable, including web indexing, Google Earth, and Google Finance. These applications place very different demands on Bigtable, both in terms of data size (from URLs to web pages to satellite imagery) and latency requirements (from backend bulk processing to real-time data serving). Despite these varied demands, Bigtable has successfully provided a flexible, high-performance solution for all of these Google products. In this paper we describe the simple data model provided by Bigtable, which gives clients dynamic control over data layout and format, and we describe the design and implementation of Bigtable.

- [Dynamo: Amazon’s Highly Available Key-value Store](papers/dynamo.pdf) (2007)

  This paper presents the design and implementation of Dynamo, a highly available key-value storage system that some of Amazon’s core services use to provide an “always-on” experience. To achieve this level of availability, Dynamo sacrifices consistency under certain failure scenarios. It makes extensive use of object versioning and application-assisted conflict resolution in a manner that provides a novel interface for developers to use.

- [Finding a needle in Haystack: Facebook’s photo storage](papers/haystack.pdf) (2010)

  This paper describes Haystack, an object storage system optimized for Facebook’s Photos application. Facebook currently stores over 260 billion images, which translates to over 20 petabytes of data. Users up- load one billion new photos (∼60 terabytes) each week and Facebook serves over one million images per second at peak. Haystack provides a less expensive and higher performing solution than our previous approach, which leveraged network attached storage appliances over NFS. Our key observation is that this traditional design incurs an excessive number of disk operations because of metadata lookups. We carefully reduce this per photo metadata so that Haystack storage machines can perform all metadata lookups in main memory. This choice conserves disk operations for reading actual data and thus increases overall throughput.

- [Windows Azure Storage: A Highly Available Cloud Storage Service with Strong Consistency](papers/azure-storage.pdf) (2011)

  Windows Azure Storage (WAS) is a cloud storage system that provides customers the ability to store seemingly limitless amounts of data for any duration of time. WAS customers have access to their data from anywhere at any time and only pay for what they use and store. In WAS, data is stored durably using both local and geographic replication to facilitate disaster recovery. Currently, WAS storage comes in the form of Blobs (files), Tables (structured storage), and Queues (message delivery). In this paper, we describe the WAS architecture, global namespace, and data model, as well as its resource provisioning, load balancing, and replication systems.

- [TAO: Facebook’s Distributed Data Store for the Social Graph](papers/tao.pdf) (2013)

  We introduce a simple data model and API tailored for serving the social graph, and TAO, an implementation of this model. TAO is a geographically distributed data store that provides efficient and timely access to the social graph for Facebook’s demanding workload using a fixed set of queries. It is deployed at Facebook, replacing memcache for many data types that fit its model. The system runs on thousands of machines, is widely distributed, and provides access to many petabytes of data. TAO can process a billion reads and millions of writes each second.

- [f4: Facebook’s Warm BLOB Storage System](papers/f4.pdf) (2014)

  Facebook’s corpus of photos, videos, and other Binary Large OBjects (BLOBs) that need to be reliably stored and quickly accessible is massive and continues to grow. As the footprint of BLOBs increases, storing them in our traditional storage system, Haystack, is becoming increasingly inefficient. To increase our storage efficiency, measured in the effective-replication-factor of BLOBs, we examine the underlying access patterns of BLOBs and identify temperature zones that include hot BLOBs that are accessed frequently and warm BLOBs that are accessed far less often. Our overall BLOB storage system is designed to isolate warm BLOBs and enable us to use a specialized warm BLOB storage system, f4. f4 is a new system that lowers the effective-replication-factor of warm BLOBs while remaining fault tolerant and able to support the lower throughput demands.

- [The RAMCloud Storage System](papers/ramcloud.pdf) (2015)

  RAMCloud is a storage system that provides low-latency access to large-scale datasets. To achieve low latency, RAMCloud stores all data in DRAM at all times. To support large capacities (1 PB or more), it aggregates the memories of thousands of servers into a single coherent key-value store. RAMCloud ensures the durability of DRAM-based data by keeping backup copies on secondary storage. It uses a uniform log-structured mechanism to manage both DRAM and secondary storage, which results in high performance and efficient memory usage. RAMCloud uses a polling-based approach to communication, bypassing the kernel to communicate directly with NICs; with this approach, client applications can read small objects from any RAMCloud storage server in less than 5 μs; durable writes of small objects take about 15 μs. RAMCloud does not keep multiple copies of data online; instead, it provides high availability by recovering from crashes very quickly (1–2 seconds). RAMCloud’s crash recovery mechanism harnesses the resources of the entire cluster working concurrently, so that its performance scales with cluster size.

- [High Performance Transactions in Deuteronomy](papers/deuteronomy.pdf) (2015)

  The Deuteronomy architecture provides a clean separation of transaction functionality (performed in a transaction component, or TC) from data management functionality (performed in a data component, or DC). In prior work we implemented both a TC and DC that achieved modest performance. We recently built a high performance DC (the Bw-tree key value store) that achieves very high performance on modern hardware and is currently shipping as an indexing and storage layer in a number of Microsoft systems. This new DC executes operations more than 100× faster than the TC we previously implemented. This paper describes how we achieved two orders of magnitude speedup in TC performance and shows that a full Deuteronomy stack can achieve very high performance overall. Importantly, the resulting full stack is a system that caches data residing on secondary storage while exhibiting performance on par with main memory systems. Our new prototype TC combined with the previously re-architected DC scales to effectively use 48 hardware threads on our 4 socket NUMA machine and commits more than 1.5 million transactions per second (6 million total operations per second) for a variety of workloads.

- [Sharding the Shards: Managing Datastore Locality at Scale with Akkio](papers/akkio.pdf) (2018)

  Akkio is a locality management service layered between client applications and distributed datastore systems. It determines how and when to migrate data to reduce response times and resource usage. Akkio primarily targets multi-datacenter geo-distributed datastore systems. Its design was motivated by the observation that many of Facebook’s frequently accessed datasets have low R/W ratios that are not well served by distributed caches or full replication. Akkio’s unit of migration is called a μ-shard. Each μ-shard is designed to contain related data with some degree of access locality. At Facebook, μ-shards have become a first-class abstraction.

- [Anna: A KVS for Any Scale](papers/anna-2018.pdf) (2018)

  We explore a new key-value store system called Anna: a partitioned, multi-mastered system that achieves high performance and elasticity via wait-free execution and coordination-free consistency. Our design rests on a simple architecture of coordination-free actors that perform state update via merge of lattice-based composite data structures. We demonstrate that a wide variety of consistency models can be elegantly implemented in this architecture with unprecedented consistency, smooth fine-grained elasticity, and performance that far exceeds the state of the art.

- [Autoscaling Tiered Cloud Storage in Anna](papers/anna-2019.pdf) (2019)

  In this paper, we describe how we extended a distributed key-value store called Anna into an autoscaling, multi-tier service for the cloud. In its extended form, Anna is designed to overcome the narrow cost-performance limitations typical of current cloud storage systems. We describe three key aspects of Anna’s new design: multi-master selective replication of hot keys, a vertical tiering of storage layers with different cost-performance tradeoffs, and horizontal elasticity of each tier to add and remove nodes in response to load dynamics. Anna’s policy engine uses these mechanisms to balance service-level objectives around cost, latency and fault tolerance. Experimental results explore the behavior of Anna’s mechanisms and policy, exhibiting orders of magnitude efficiency improvements over both commodity cloud KVS services and research systems.

- [DistCache: Provable Load Balancing for Large-Scale Storage Systems with Distributed Caching](papers/distcache.pdf) (2019)

  We present DistCache, a new distributed caching mechanism that provides provable load balancing for large-scale storage systems. DistCache co-designs cache allocation with cache topology and query routing. The key idea is to partition the hot objects with independent hash functions between cache nodes in different layers, and to adaptively route queries with the power-of-two-choices. We prove that DistCache enables the cache throughput to increase linearly with the number of cache nodes, by unifying techniques from expander graphs, network flows, and queuing theory. DistCache is a general solution that can be applied to many storage systems.

- [FoundationDB Record Layer: A Multi-Tenant Structured Datastore](papers/foundationdb-2019.pdf) (2019)

  The FoundationDB Record Layer is an open source library that provides a record-oriented data store with semantics similar to a relational database implemented on top of FoundationDB, an ordered, transactional key-value store. The Record Layer provides a lightweight, highly extensible way to store structured data. It offers schema management and a rich set of query and indexing facilities, some of which are not usually found in traditional relational databases, such as nested record types, indexes on commit versions, and indexes that span multiple record types. The Record Layer is stateless and built for massive multi-tenancy, encapsulating and isolating all of a tenant’s state, including indexes, into a separate logical database. We demonstrate how the Record Layer is used by CloudKit, Apple’s cloud backend service, to provide powerful abstractions to applications serving hundreds of millions of users. CloudKit uses the Record Layer to host billions of independent databases, many with a common schema. Features provided by the Record Layer enable CloudKit to provide richer APIs and stronger semantics with reduced maintenance overhead and improved scalability.

- [FoundationDB: A Distributed Unbundled Transactional Key Value Store](papers/foundationdb-2021.pdf) (2021)

  FoundationDB is an open source transactional key value store created more than ten years ago. It is one of the first systems to combine the flexibility and scalability of NoSQL architectures with the power of ACID transactions (a.k.a. NewSQL). FoundationDB adopts an unbundled architecture that decouples an in-memory transaction management system, a distributed storage system, and a built-in distributed configuration system. Each sub-system can be independently provisioned and configured to achieve the desired scalability, high-availability and fault tolerance properties. FoundationDB uniquely integrates a deterministic simulation framework, used to test every new feature of the system under a myriad of possible faults. This rigorous testing makes FoundationDB extremely stable and allows developers to introduce and release new features in a rapid cadence. FoundationDB offers a minimal and carefully chosen feature set, which has enabled a range of disparate systems (from semi-relational databases, document and object stores, to graph databases and more) to be built as layers on top. FoundationDB is the underpinning of cloud infrastructure at Apple, Snowflake and other companies, due to its consistency, robustness and availability for storing user data, system metadata and configuration, and other critical information.

- [Virtual Consensus in Delos](papers/delos-2020.pdf) (2020)

  We propose virtualizing consensus by virtualizing the shared log API, allowing services to change consensus protocols without downtime. Virtualization splits the logic of consensus into the VirtualLog, a generic and reusable reconfiguration layer; and pluggable ordering protocols called Loglets. Loglets are simple, since they do not need to support reconfiguration or leader election; diverse, consisting of different protocols, codebases, and even deployment modes; and composable, via RAID-like stacking and striping. We describe a production database called Delos, which leverages virtual consensus for rapid, incremental development and deployment.

- [Log-structured Protocols in Delos](papers/delos-2021.pdf) (2021)

  Developers have access to a wide range of storage APIs and functionality in large-scale systems, such as rela- tional databases, key-value stores, and namespaces. However, this diversity comes at a cost: each API is implemented by a complex distributed system that is difficult to develop and operate. Delos amortizes this cost by enabling different APIs on a shared codebase and operational platform. The primary innovation in Delos is a log-structured protocol: a fine-grained replicated state machine executing above a shared log that can be layered into reusable protocol stacks under different databases.

- [Amazon DynamoDB: A Scalable, Predictably Performant, and Fully Managed NoSQL Database Service](papers/dynamodb.pdf) (2022)

  Amazon DynamoDB is a NoSQL cloud database service that provides consistent performance at any scale. Hundreds of thousands of customers rely on DynamoDB for its fundamental properties: consistent performance, availability, durability, and a fully managed serverless experience. In 2021, during the 66-hour Amazon Prime Day shopping event, Amazon systems - including Alexa, the Amazon.com sites, and Amazon fulfillment centers, made trillions of API calls to DynamoDB, peaking at 89.2 million requests per second, while experiencing high availability with single-digit millisecond performance. Since the launch of DynamoDB in 2012, its design and implementation have evolved in response to our experiences operating it. The system has successfully dealt with issues related to fairness, traffic imbalance across partitions, monitoring, and automated system operations without impacting availability or performance. Reliability is essential, as even the slightest disruption can significantly impact customers. This paper presents our experience operating DynamoDB at a massive scale and how the architecture continues to evolve to meet the ever-increasing demands of customer workloads.

## Testing and deployment

- [Benchmarking Cloud Serving Systems with YCSB](papers/ycsb.pdf) (2010)

  We present the Yahoo! Cloud Serving Benchmark (YCSB) framework, with the goal of facilitating performance comparisons of the new generation of cloud data serving systems. We define a core set of benchmarks and report results for four widely used systems: Cassandra, HBase, Yahoo!’s PNUTS, and a simple sharded MySQL implementation. We also hope to foster the development of additional cloud benchmark suites that represent other classes of applications by making our benchmark tool available via open source. In this regard, a key feature of the YCSB framework/tool is that it is extensible — it supports easy definition of new workloads, in addition to making it easy to benchmark new systems.

- [An Opportunity Cost Approach for Job Assignment in a Scalable Computing Cluster](papers/epvm.pdf) (2000)

  A new method is presented for job assignment to and reassignment between machines in a computing cluster. Our method is based on a theoretical framework that has been experimentally tested and shown to be useful in practice. This opportunity cost method converts the usage of several heterogeneous resources in a machine to a single homogeneous cost. Assignment and reassignment are then performed based on that cost. This is in contrast to traditional, ad hoc methods for job assignment and reassignment. These treated each resource as an independent entity with its own constraints, as there was no clean way to balance one resource against another.

- [Large-scale cluster management at Google with Borg](papers/borg.pdf) (2015)

  Google’s Borg system is a cluster manager that runs hundreds of thousands of jobs, from many thousands of different applications, across a number of clusters each with up to tens of thousands of machines. It achieves high utilization by combining admission control, efficient task-packing, over-commitment, and machine sharing with process-level performance isolation. It supports high-availability applications with runtime features that minimize fault-recovery time, and scheduling policies that reduce the probability of correlated failures. Borg simplifies life for its users by offering a declarative job specification language, name service integration, real-time job monitoring, and tools to analyze and simulate system behavior.

- [Using Lightweight Formal Methods to Validate a Key-Value Storage Node in Amazon S3](papers/lightweight-formal-methods.pdf) (2021)

  This paper reports our experience applying lightweight formal methods to validate the correctness of ShardStore, a new key-value storage node implementation for the Amazon S3 cloud object storage service. By "lightweight formal methods" we mean a pragmatic approach to verifying the correctness of a production storage node that is under ongoing feature development by a full-time engineering team.

## Lessons learned and the future

- [Notes on Distributed Systems for Young Bloods](https://www.somethingsimilar.com/2013/01/14/notes-on-distributed-systems-for-young-bloods/) (2013)

  This is a list of some lessons I’ve learned as a distributed systems engineer that are worth being told to a new engineer. Some are subtle, and some are surprising, but none are controversial. This list is for the new distributed systems engineer to guide their thinking about the field they are taking on. It’s not comprehensive, but it’s a good beginning.

- [What I Learned From Programming Databases](http://www.philipotoole.com/what-i-learned-from-programming-a-database/) (2016)

  If there was one piece of advice I would give to fellow developers looking to improve their programming ability, it would be to become part of a database development team. My programming skills increased enormously as a result of database development — it is a wonderful coding experience.

- [What Goes Around Comes Around](papers/what-goes-around-comes-around.pdf) (2005)

  This paper provides a summary of 35 years of data model proposals, grouped into 9 different eras. We discuss the proposals of each era, and show that there are only a few basic data modeling ideas, and most have been around a long time. Later proposals inevitably bear a strong resemblance to certain earlier proposals. Hence, it is a worthwhile exercise to study previous proposals.

  In addition, we present the lessons learned from the exploration of the proposals in each era. Most current researchers were not around for many of the previous eras, and have limited (if any) understanding of what was previously learned. There is an old adage that he who does not understand history is condemned to repeat it. By presenting “ancient history”, we hope to allow future researchers to avoid replaying history.

- ["One Size Fits All": An Idea Whose Time Has Come and Gone](papers/one-size-fits-all.pdf) (2005)

  The last 25 years of commercial DBMS development can be summed up in a single phrase: “One size fits all”. This phrase refers to the fact that the traditional DBMS architecture (originally designed and optimized for business data processing) has been used to support many data-centric applications with widely varying characteristics and requirements.

  In this paper, we argue that this concept is no longer applicable to the database market, and that the commercial world will fracture into a collection of independent database engines, some of which may be unified by a common front-end parser. We use examples from the stream-processing market and the data-warehouse market to bolster our claims. We also briefly discuss other markets for which the traditional architecture is a poor fit and argue for a critical rethinking of the current factoring of systems services into products.

- [The Seattle Report on Database Research](papers/the-seattle-report-2019.pdf) (2019)

  Approximately every five years, a group of database researchers meet to do a self-assessment of our community, including reflections on our impact on the industry as well as challenges facing our research community. This report summarizes the discussion and conclusions of the 9th such meeting, held during October 9-10, 2018 in Seattle.
