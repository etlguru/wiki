---
author: Mike Rewnick
title: Introduction
description: RabbitMQ Logger Installation
draft: false
tags: ['RabbitMQ Logger', 'Event Loggers']
date: 2022-05-19
menu: rabbitmq-logger
group: rabbitmq-logger
layout: docs
---

Rabbit MQ Logger writes Rabbit MQ messages into the database.

## About Rabbit MQ

RabbitMQ is an open-source message-broker software (sometimes called message-oriented middleware) that originally implemented the Advanced Message Queuing Protocol (AMQP) and has since been extended with a plug-in architecture to support Streaming Text Oriented Messaging Protocol (STOMP), MQ Telemetry Transport (MQTT), and other protocols.

Written in Erlang, the RabbitMQ server is built on the Open Telecom Platform framework for clustering and failover. Client libraries to interface with the broker are available for all major programming languages. The source code is released under the Mozilla Public License.

Source: [Wikipedia](https://en.wikipedia.org/wiki/RabbitMQ)

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/rabbitmq-logger/rabbitmq-logger-data-flow.png" title="RabbitMQ Logger Usage Example" >}}
\
{{< alert color="secondary" >}}
RabbitMQ Logger works on both Windows and Linux. Please contact us if you want to run RabbitMQ Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< rabbitmq-logger >}}
