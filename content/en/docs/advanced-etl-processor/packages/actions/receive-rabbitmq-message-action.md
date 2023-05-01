---
author: Peter Jonson
title: Receive RabbitMQ Message Action
description: Receive RabbitMQ Message Action
draft: false
tags: ['Package', 'Action', 'Message', 'RabbitMQ']
date: 2022-01-13
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

RabbitMQ is the most widely deployed open-source message broker.

With tens of thousands of users, RabbitMQ is one of the most popular open-source message brokers. From T-Mobile to Runtastic, RabbitMQ is used worldwide at small startups and large enterprises.
RabbitMQ is lightweight and easy to deploy on-premises and in the cloud. It supports multiple messaging protocols. RabbitMQ can be deployed in distributed and federated configurations to meet high-scale, high-availability requirements.
RabbitMQ runs on many operating systems and cloud environments and provides a wide range of developer tools for the most popular languages.

More information: https://www.rabbitmq.com

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/receive-rabbitmq-message-properties-1.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/receive-rabbitmq-message-properties-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/receive-rabbitmq-message-properties-3.png" title="After execution tab" >}}

- [How to obtain RabbitMQ Exchange name and Routing key]({{<relref "/knowledgebase/connections/connecting-to-rabbitmq" >}})

{{< alert color="secondary">}}RabbitMQ is a trademark of VMware, Inc. in the U.S. and other countries{{< /alert >}}

{{< aetl >}}
