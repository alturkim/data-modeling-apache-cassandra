# Data Modeling for Apache Cassandra
## Overview
Apache Cassandra is a **Partition Raw Store** database that organizes raws into partitions generated using a hashing algorithm on the partition key. A collection of partitions represents a **table**. One table can be spread over multiple nodes, however, a single partition is stored entirely in one node. Furthmore, Apache Cassandra uses **Clustering Columns** to sort the data within each partition.

Apache Cassandra is optimized for writing which makes it a suitable option for user activities or any form of time series data.

Apache Cassandra uses CQL (Cassandra Query Language), a query language that is similar to SQL but does NOT support JOIN, GROUP BY and subqueries.

