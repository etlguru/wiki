---
author: Mike Rewnick
title: Settings
description: Licensing Server Settings
draft: false
tags: ['Licensing Server']
date: 2022-03-17
menu: licensing-server
group: licensing-server
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## List of options

## Enable Security

When security is disabled every one has unlimited access to licensing server, We do not recommend running licensing server with disabled security

### Enable Preferences Screen

Enables/ disables (hides) Preferences Screen

### Enable Web Logging

Enables logging

### Use Cluster

Always set to false

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

Do not change

### Host

Do not change

### Port

Do not change

### Database

Location of licensing server repository database

### Instance

Do not change

### User Name

Do not change

### Password

Do not change

{{< alert color="secondary" >}}
The settings are stored in .ENV file
{{< /alert >}}

## Default ENV file

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
DB_NAME=%PROGRAMDATA%/etl-tools.com/licensing-server/licensing-server-repository.sqlite\
DB_HOST=\
DB_PORT=\
DB_INSTANCE=\
ENABLE_LOGGING=0\
SQL_LOGGING=0\
USE_CLUSTER=0\
USE_SSL=0\
TOOLBAR_CLASS=navbar navbar-dark shadow bg-success bg-gradient rounded

## ENV file location

- Windows: C:\ProgramData\ETL-Tools.com\licensing-server
- Linux: /etc/etl-tools.com/licensing-server

## Restarting Licensing server after changing options

### Windows

Restart ETL-Tools.com Licensing Server (64bit) windows service

### Linux

Run the following commands

{{< command >}}
sudo systemctl stop etl-tools-licensing-server\
sudo systemctl start etl-tools-licensing-server
{{< /command >}}

{{< alert color="secondary" >}}
Licensing server works on both Windows and Linux. Please contact us if you want to run Licensing server on a different OS. We will create a special build for you.
{{< /alert >}}

{{< ls >}}
