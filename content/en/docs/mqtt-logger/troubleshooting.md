---
author: Mike Rewnick
title: Troubleshooting
description: MQTT Logger Troubleshooting
draft: false
tags: ['MQTT Logger', 'Troubleshooting']
date: 2022-04-16
menu: mqtt-logger
group: mqtt-logger
layout: docs
---

### Windows

- Stop ETL-Tools.com MQTT Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\MQTT Logger\mqtt-logger.exe

### Linux

{{< command >}}
sudo systemctl stop etl-tools-mqtt-logger
cd /opt/etl-tools.com/mqtt-logger
sudo ./mqtt-logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/mqtt-logger/mqtt-logger-error.png" title="MQTT Logger Error" >}}

{{< mqtt-logger >}}
