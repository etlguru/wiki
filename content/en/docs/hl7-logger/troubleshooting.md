---
author: Mike Rewnick
title: Troubleshooting
description: HL7 Logger Troubleshooting
draft: false
tags: ['HL7 Event Logger', 'Troubleshooting']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

### Windows

- Stop ETL-Tools.com HL7 Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\HL7 Logger\hl7_logger.exe

### Linux

{{< command >}}
sudo systemctl stop etl-tools-hl7-logger
cd /opt/etl-tools.com/hl7-logger
sudo ./hl7_logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/hl7-logger/hl7-logger-error.png" title="HL7 Logger Error" >}}

{{< hl7-event-logger >}}
