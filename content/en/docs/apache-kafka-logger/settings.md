---
author: Mike Rewnick
title: Settings
description: Apache Kafka Logger Settings
date: 2023-05-08
draft: false
tags: ['Apache Kafka Logger', 'Settings']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## List of options

### Enable Security

When security is disabled every one has unlimited access to Apache Kafka Logger, We do not recommend running Apache Kafka Logger with disabled security

### Enable Preferences Screen

Enables/ disables (hides) Preferences Screen

### Enable Web Logging

Enables logging

### Use Cluster

Improves performance when logging a lot of events

### Use SSL

Enables HTTPS server

### Run SQL Scripts

Performs repository upgrade. Only set this option when asked by support

### Enable SQL Logging

Only set this option when asked by support

### Web Server Port

http://computer:port

### Environment Name

### Security Key

Used for password encryption

### Security Key Expires In

User session expiration time in days

### Default User Page

Do not change

### Toolbar class

Changes top toolbar look and feel

### Connection type

Repository Database Connection type

### Host

Repository Database hostname

### Port

Repository Database port

### Database

Location/Name of Apache Kafka Logger repository database

### Instance

SQL Server instance name

### User Name

Repository Database User Name

### Password

Repository Database Password

{{< alert color="secondary" >}}
The settings are stored in .ENV file
{{< /alert >}}

## Default ENV file

RUN_SQL_SCRIPTS=0
WEB_SERVER_PORT=3333\
ENVIRONMENT_NAME=-DEV\
ENABLE_SECURITY=1\
ENABLE_PREFERENCES_SCREEN=1\
ATTACHMENTS_DIRECTORY=./attachments/\
JWT_KEY=DB Software Laboratory\
JWT_EXPIRES_IN=30d\
DEFAULT_USER_PAGE=frontpage\
NODE_ENV=production\
CONNECTION_TYPE=sqlite\
DB_USER=\
DB_PASS=\
DB_NAME=%PROGRAMDATA%/etl-tools.com/apache-kafka-logger/apache-kafka-logger-repository.sqlite\
DB_HOST=\
DB_PORT=\
DB_INSTANCE=\
ENABLE_LOGGING=0\
SQL_LOGGING=0\
USE_CLUSTER=0\
USE_SSL=0\
TOOLBAR_CLASS=navbar navbar-dark shadow bg-success bg-gradient rounded\

## ENV file location

- Windows: C:\ProgramData\ETL-Tools.com\apache-kafka-logger
- Linux: /etc/etl-tools.com/apache-kafka-logger

## Restarting Apache Kafka Logger after changing options

### Windows

Restart ETL-Tools.com Apache Kafka Logger (64bit) windows service

### Linux

Run the following commands
{{< command >}}
sudo systemctl stop etl-tools-apache-kafka-logger
sudo systemctl start etl-tools-apache-kafka-logger
{{< /command >}}

{{< alert color="secondary" >}}
Apache Kafka Logger works on both Windows and Linux. Please contact us if you want to run Apache Kafka Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< apache-kafka-logger >}}
