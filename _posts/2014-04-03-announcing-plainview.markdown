---
layout: post
title:  "plainview - A Data Pipeline Toolkit"
date:   2014-04-03 08:26:05
categories:
---

As uses cases for data become more diverse and specialized, so do the platforms used to store, process and serve it. Secondary data stores for features like search, analysis, and caching need to stay in sync with the changes occuring in the primary data store, and possibly data from other sources as well. The data pipeline is an emerging architectural design pattern for propogating this data to an arbitrary number of destinations in real time without coupling these destinations to application code or eachother.

Today I'm proud to announce [plainview][plainview-gh], a toolkit for starting a data pipeline by tapping into your primary data store's replication stream. This project aims to emphasize ease-of-use, and to that end it leverages Amazon's Kinesis service for transport and durability.  Presently, it comprises two simple executables - a "Producer" application for reading a replication stream from MySQL and writing it a Kinesis pipeline, and a "Consumer" application for reading that data from Kinesis and storing it in Amazon S3. Full getting started documentation can be found in the [project repository][plainview-gh].

In the future we plan to build Producers for a number of source platforms including PostgreSQL and MongoDB, and Consumers that encompass a variety of common use cases as well.

[plainview-gh]: https://github.com/cmerrick/plainview
