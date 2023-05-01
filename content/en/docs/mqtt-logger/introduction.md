---
author: Mike Rewnick
title: Introduction
description: MQTT Logger captures MQTT messages and saves them into the database
draft: false
tags: ['MQTT Logger', 'Introduction']
date: 2022-04-17
menu: mqtt-logger
group: mqtt-logger
layout: docs
---

MQTT Logger captures MQTT messages and saves them into the database.

### MQTT Protocol

MQTT (originally an initialism of MQ Telemetry Transport) is a lightweight, publish-subscribe network protocol that transports messages between devices. The protocol usually runs over TCP/IP, however, any network protocol that provides ordered, lossless, bi-directional connections can support MQTT. It is designed for connections with remote locations where resource constraints exist or the network bandwidth is limited.

Source: [Wikipedia](https://en.wikipedia.org/wiki/MQTT)

### Usage Example

MQTT is used for communication between IoT devices such as smart switches or lamps. MQTT is also used for smart home management.

{{< image class="mx-auto d-block"  src="/images/event-loggers/mqtt-logger/mqtt-logger-data-flow.png" title="Usage Example" >}}
\
{{< alert color="secondary" >}}
MQTT Logger works on both Windows and Linux. Please contact us if you want to run MQTT Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< mqtt-logger >}}
