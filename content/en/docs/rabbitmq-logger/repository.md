---
author: Mike Rewnick
title: Repository
description: RabbitMQ Logger Repository
draft: false
tags: ['RabbitMQ Logger', 'Event Loggers']
date: 2022-05-18
menu: rabbitmq-logger
group: rabbitmq-logger
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
- Restart Rabbit MQ Logger
- Recreate/Enable Groups
- Recreate/Enable Users
- Set ENABLE_SECURITY=1
- Restart Rabbit MQ Logger

{{< rabbitmq-logger >}}