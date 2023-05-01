---
author: Mike Rewnick
title: Repository
description: Apache Kafka Logger Repository
date: 2023-03-07
draft: false
tags: ['Apache Kafka Logger', 'Registration']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

The default repository type is SQLite, it works very well with a small amount of data. For high-load systems, we recommend using different database type

## Supported Repository Database Types

- SQLite
- Postgres
- MySQL
- MariaDB
- Microsoft SQL Server
- Oracle

## Changing Repository Type

- Set ENABLE_SECURITY=0
- Set RUN_SQL_SCRIPTS=1
- Set Set CONNECTION_TYPE, DB_USER, DB_PASS, DB_NAME, DB_HOST, DB_PORT, DB_INSTANCE to appropriate values
- Restart Apache Kafka Logger
- Recreate/Enable Groups
- Recreate/Enable Users
- Set ENABLE_SECURITY=1
- Restart Apache Kafka Logger

{{< apache-kafka-logger >}}
