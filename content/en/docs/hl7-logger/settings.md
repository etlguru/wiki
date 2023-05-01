---
author: Mike Rewnick
title: Settings
description: HL7 Logger Settings
draft: false
tags: ['HL7 Event Logger', 'Settings']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

### List of options

## Enable Security

When security is disabled every one has unlimited access to HL7 Logger, We do not recommend running HL7 Logger with disabled security

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

Location/Name of HL7 Logger repository database

### Instance

SQL Server instance name

### User Name

Repository Database User Name

### Password

Repository Database Password

{{< alert color="secondary" >}}
The settings are stored in .ENV file
{{< /alert >}}

### Default ENV file

RUN_SQL_SCRIPTS=0\
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
DB_NAME=%PROGRAMDATA%/etl-tools.com/hl7-logger/hl7-logger-repository.sqlite\
DB_HOST=\
DB_PORT=\
DB_INSTANCE=\
ENABLE_LOGGING=0\
SQL_LOGGING=0\
USE_CLUSTER=0\
USE_SSL=0\
TOOLBAR_CLASS=navbar navbar-dark shadow bg-success bg-gradient rounded

### ENV file location

- Windows: C:\ProgramData\ETL-Tools.com\hl7-logger
- Linux: /etc/etl-tools.com/hl7-logger

### Restarting HL7 Logger after changing options

### Windows

Restart ETL-Tools.com HL7 Logger (64bit) windows service

### Linux

Run the following commands

{{< command >}}
sudo systemctl stop etl-tools-hl7-logger
sudo systemctl start etl-tools-hl7-logger
{{< /command >}}

{{< alert color="secondary" >}}
HL7 Logger works on both Windows and Linux. Please contact us if you want to run HL7 Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< hl7-event-logger >}}
