---
author: Mike Rewnick
title: Troubleshooting
description: URL Logger Troubleshooting
draft: false
tags: ['URL Logger', 'Event Loggers']
date: 2022-04-03
menu: url-logger
group: url-logger
layout: docs
---

## Windows

- Stop ETL-Tools.com URL Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\URL Logger\url_logger.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-url-logger
cd /opt/etl-tools.com/url-logger
sudo ./url_logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/url-logger/url-logger-error.png" title="Error" >}}

{{< url-logger >}}
