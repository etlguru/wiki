---
author: Mike Rewnick
title: Troubleshooting
description: Licensing Server Troubleshooting
draft: false
tags: ['Licensing Server']
date: 2022-04-03
menu: licensing-server
group: licensing-server
layout: docs
---

## Windows

- Stop ETL-Tools.com Licensing Server (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\Licensing Server\licensing-server.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-licensing-server
cd /opt/etl-tools.com/licensing-server
sudo ./licensing-server
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-email-logger-error.png" title="Error" >}}

{{< ls >}}
