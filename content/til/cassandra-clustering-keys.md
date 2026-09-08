---
title: "Designing a Watch History Schema in Cassandra"
date: 2026-09-08T17:00:00+03:30
draft: false
tags: ["Cassandra", "CQL", "Database", "DBeaver"]
---

Today I was designing a schema for a video streaming watch history (similar to Netflix) in Apache Cassandra using DBeaver. 

The key takeaway was understanding how **Clustering Keys** work in distributed databases. While the Partition Key determines *which node* stores the data, the Clustering Key determines *how* that data is physically sorted on the disk within that specific partition.

Here is a quick CQL example of how to order the watch history by date automatically:

```sql
CREATE TABLE watch_history (
    user_id uuid,
    watch_date timestamp,
    movie_id uuid,
    PRIMARY KEY ((user_id), watch_date)
) WITH CLUSTERING ORDER BY (watch_date DESC);
```

By explicitly setting the clustering order to DESC, we ensure that whenever we query a user's history, the most recently watched movies are retrieved instantly without any extra sorting overhead!