---
author: Mike Rewnick
title: Troubleshooting
description: RabbitMQ Logger Troubleshooting
draft: false
tags: ['RabbitMQ Logger', 'Event Loggers']
date: 2022-05-20
menu: rabbitmq-logger
group: rabbitmq-logger
layout: docs
---

## Windows

- Stop ETL-Tools.com RabbitMQ Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\RabbitMQ Logger\rabbitmq-logger.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-rabbitmq-logger
cd /opt/etl-tools.com/rabbitmq-logger
sudo ./rabbitmq-logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/rabbitmq-logger/rabbitmq-logger-error.png" title="RabbitMQ Logger Event log" >}}

{{< rabbitmq-logger >}}
