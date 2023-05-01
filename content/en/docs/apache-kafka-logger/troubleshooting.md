---
author: Mike Rewnick
title: Troubleshooting
description: Apache Kafka Logger Troubleshooting
date: 2023-03-07
draft: false
tags: ['Apache Kafka Logger', 'Troubleshooting']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

## Windows

- Stop ETL-Tools.com Apache Kafka Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\Apache Kafka Logger\apache-kafka-logger.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-apache-kafka-logger
cd /opt/etl-tools.com/apache-kafka-logger
sudo ./apache-kafka-logger
{{< /command >}}

Refresh the page
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/apache-kafka-logger/apache-kafka-logger-error.png" title="Apache Kafka Logger Error" >}}

{{< apache-kafka-logger >}}
