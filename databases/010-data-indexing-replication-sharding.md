---
id: 010-data-indexing-replication-sharding.md
title: Data Indexing, Replication, and Sharding - Basic Concepts
tags: system, system design, system design interview, database, indexing, replication, sharding
date: 2022-10-23 21:26:39 +0200 
keywords: Indexing, Sharding
categories: Database
author: Pragya Sapkota
meta-description: Database Indexing and Replication and Sharding
---

# Data Indexing, Replication, and Sharding: Basic Concepts

![Indexing, Replication, Sharding](https://miro.medium.com/max/1100/1*zPddtlzQOJUgV7NQJQruKg.jpeg)

A database is a collection of information that is structured for easy access. It mainly runs in a computer system and is controlled by a database management system (DBMS). Let’s see some concepts of the database here — Indexing, Replication, and, Sharding respectively.

## Indexing

The database can have a large amount of data with up to millions of records. In the time of need, the disorganized data with no index is very hard to retrieve and the whole database would have to be iterated one by one. And if it’s old data, then that would be an absolute nightmare. The solution to getting out of this complication is INDEX.

Database Indexing is a kind of data structure that helps with fast retrieval of the information held in the database. We use indexes to look up those data which is assigned at the time the information is stored. When the data is too large to be able to search for data iteratively, we use database indexing. This is a core necessity to a relational database and is offered on non-relational databases as well. We have a very optimized lookup time when the data is indexed.

## Replication

Replication means making copies of things to duplicate them. In a database, the term replication is heard when we learn scaling. We can duplicate our database so that if the database overloads and crash at some point, the other duplicated database handles the load, and we can avoid system failure. This creates redundancy in the system which will maintain high availability in the system.

![Replication](https://miro.medium.com/max/1100/1*9gMX9HN_uoba2kEaNEZw-w.jpeg)

We can have the data replication both synchronously and asynchronously. When chosen the synchronous way, the replicated database updates in sync with the changes in the main database. You can allocate a time interval where your main database and the replica database can be synchronized and updated. One other thing to ensure is that if the write operation to the replica fails somehow, the write operation to the main database also fails. This falls under the feature Atomicity.

However, the dispute that might occur in the replication is when the data is too large, and the only concern is to make the system more available but not to improve latency and throughput. And thus, we chunk down the data which leads us to Sharding.

## Sharding

Data sharding means breaking the huge database into smaller databases so that the latency and throughput are maintained after the database replication. You can choose how you want your data to be broken. There are two types of ways to shard your data — horizontal and vertical sharding. In horizontal sharding, the rows of the same table are stored in multiple database nodes whereas, in vertical sharding, different tables and columns are stored in a separate database.

![Sharding](https://miro.medium.com/max/1100/1*nITTQ-l2v9CTcl9q28ZhAQ.jpeg)