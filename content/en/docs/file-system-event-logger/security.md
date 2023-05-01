---
author: Mike Rewnick
title: Security
description: File System Event Logger Security
draft: false
tags: ['File System Event Logger', 'Security']
date: 2022-04-07
menu: file-system-event-logger
group: file-system-event-logger
layout: docs
---

There are two ways of running the File System Event Logger with security enabled or disabled.\
When security is disabled every one has unlimited access to File System Event Logger, We do not recommend running File System Event Logger with disabled security

{{< image class="mx-auto d-block"  src="/images/licensing-server/settings.png" title="Settings" >}}

## Login screen

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png" title="Login" >}}

## Security is enabled

{{ :file_system_event_logger:file_system_event_logger_security_enabled.png" title="Security is enabled" >}}

## Security is disabled

{{ :file_system_event_logger:file_system_event_logger_security_disabled.png" title="Security is disabled" >}}

## Password Encryption

The passwords are encrypted using a security key. We recommend changing it immediately after installation

The procedure is as follows

- Disable security
- Update security key
- Restart the logger
- Update users passwords
- Enable security
- Restart the logger

## SSL Encryption

We recommend using SSL encryption for network communications

The procedure is as follows

- Generate SSL Certificate
- Copy server.key and server.cer into .env folder
- Enable SSL
- Restart the server

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

## ENV Folder

### Windows

C:\ProgramData\ETL-Tools.com\file-system-event-logger\

### Linux

/etc/etl-tools.com/file-system-event-logger

{{< file-system-event-logger >}}
