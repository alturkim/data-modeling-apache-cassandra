# Data Modeling for Apache Cassandra
## Overview
Apache Cassandra is a **Partition Raw Store** database that organizes raws into partitions generated using a hashing algorithm on the **partition key**. A collection of partitions represents a **table**. One table can be spread over multiple nodes, however, a single partition is stored entirely in one node. Furthmore, Apache Cassandra uses **Clustering Columns** to sort the data within each partition.

Apache Cassandra is optimized for writing which makes it a suitable option for user activities or any form of time series data.

Apache Cassandra uses CQL (Cassandra Query Language), a query language that is similar to SQL but does NOT support JOIN, GROUP BY and subqueries.

## Modeling for Apache Cassandra
Since Apache Cassandra is normally used for big data that are distrbuted across multiple nodes, we need a mechanism by which we can allocate the required data when executing a query. For this reason, data are modeled based on the queries that are going to be run against the database, a.k.a **Standard Queries**, hence, Apache Cassandra has no support for **ad hoc queries**, which are queries that arise based on future needs. Modeling for **standard queries** is done by using attributes  that appears in the **WHERE** clause as partition keys, which results in placing data in nodes such that they are easily allocated when queried, providing fast reads as a result.


