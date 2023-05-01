---
author: Mike Rewnick
title: Repository
description: IMAP4 EMail Logger Repository
draft: false
tags: ['IMAP4 EMail Logger', 'Repository']
date: 2022-04-07
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

The default repository type is SQLite, it works very well with a small amount of data. For high-load systems, we recommend using different database type

### Supported Repository Database Types

- SQLite
- Postgres
- MySQL
- MariaDB
- Microsoft SQL Server
- Oracle

### Changing Repository Type

- Set ENABLE_SECURITY=0
- Set RUN_SQL_SCRIPTS=1
- Set Set CONNECTION_TYPE, DB_USER, DB_PASS, DB_NAME, DB_HOST, DB_PORT, DB_INSTANCE to appropriate values
- Restart IMAP4 Email Logger
- Recreate/Enable Groups
- Recreate/Enable Users
- Set ENABLE_SECURITY=1
- Restart IMAP4 Email Logger

{{< imap4-email-logger >}}
