---
author: Mike Rewnick
title: Troubleshooting
description: Office365 Email Logger Troubleshooting
draft: false
tags: ['Office365 Email Logger', 'Troubleshooting']
date: 2022-04-11
menu: office365-email-logger
group: office365-email-logger
layout: docs
---

## Windows

- Stop ETL-Tools.com Office365 Email Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\Office365 Email Logger\office365_logger.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-office365-logger
cd /opt/etl-tools.com/office365-logger
sudo ./office365_logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/office365-email-logger/office365-email-logger-error.png" title="Error" >}}

{{< office365-email-logger >}}
