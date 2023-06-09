---
author: Mike Rewnick
title: Introduction
description: Apache Kafka Logger writes Apache Kafka messages into the database
date: 2023-03-07
draft: false
tags: ['Apache Kafka Logger', 'Introduction']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

## About Apache Kafka

Apache Kafka is a distributed event store and stream-processing platform. It is an open-source system developed by the Apache Software Foundation written in Java and Scala. The project aims to provide a unified, high-throughput, low-latency platform for handling real-time data feeds. Kafka can connect to external systems (for data import/export) via Kafka Connect, and provides the Kafka Streams libraries for stream processing applications. Kafka uses a binary TCP-based protocol that is optimized for efficiency and relies on a "message set" abstraction that naturally groups messages together to reduce the overhead of the network roundtrip. This "leads to larger network packets, larger sequential disk operations, contiguous memory blocks [...] which allows Kafka to turn a bursty stream of random message writes into linear writes."

Source: [Wikipedia](https://en.wikipedia.org/wiki/Apache-Kafka|Wikipedia)

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/apache-kafka-logger/apache-kafka-logger-data-flow.png" title="Usage Example" >}}
\
{{< alert color="secondary" >}}
Apache Kafka Logger works on both Windows and Linux. Please contact us if you want to run Apache Kafka Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< apache-kafka-logger >}}
