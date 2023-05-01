---
author: Mike Rewnick
title: Troubleshooting
description: File System Event Logger Troubleshooting
draft: false
tags: ['File System Event Logger', 'Troubleshooting']
date: 2022-04-05
menu: file-system-event-logger
group: file-system-event-logger
layout: docs
---

## Windows

- Stop ETL-Tools.com File System Event Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\File System Event Logger\file-system-event-logger.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-file-system-event-logger
cd /opt/etl-tools.com/file-system-event-logger
sudo ./file-system-event-logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/file-system-logger/file-system-event-logger-error.png"  title="File System Event Logger Error" >}}

{{< file-system-event-logger >}}
