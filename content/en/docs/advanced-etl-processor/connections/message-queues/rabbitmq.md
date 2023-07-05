---
author: Peter Jonson
title: RabbitMQ Connection
description: RabbitMQ Connection
draft: false
tags: ['Connection', 'RabbitMQ']
date: 2023-07-04
group: advanced-etl-processor-enterprise-message-queues
menu: advanced-etl-processor-enterprise
layout: docs
---

## About RabbitMQ

RabbitMQ is an open-source message-broker software (sometimes called message-oriented middleware) that originally implemented the Advanced Message Queuing Protocol (AMQP) and has since been extended with a plug-in architecture to support Streaming Text Oriented Messaging Protocol (STOMP), MQ Telemetry Transport (MQTT), and other protocols

Source: Wikipedia

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/rabbitmq-connection.png" title="RabbitMQ Connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/rabbitmq-connection-comments.png" title="RabbitMQ Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/rabbitmq-connection-user-fields.png" title="RabbitMQ User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

- [How to obtain RabbitMQ Exchange name and Routing key]({{<relref "/knowledgebase/connections/connecting-to-rabbitmq">}})

{{< alert color="secondary">}}RabbitMQ is a trademark of VMware, Inc. in the U.S. and other countries{{< /alert >}}

{{< aetl >}}
