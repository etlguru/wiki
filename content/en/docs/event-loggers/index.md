---
author: Mike Rewnick
title: Event Loggers
description: An event logger is an application that reacts to predefined events and writes event information into the database..
date: 2023-03-15
tags: ['Event logger']
layout: minimal
---

An event logger is an application that reacts to predefined events and writes event information into the database.

{{< image class="mx-auto d-block"  src="/images//event-loggers/event-logger-data-flow.png"  title="Event Logger Data Flow" >}}

The simplest example of an event is the Rest API call. Most popular order processing systems allow the seller to define the URL called upon order completion. The information provided can be used to generate an email notification or provide the user with the license keys.

The typical event logger consists of an event handler, filter and the repository database where everything is stored

### A list of available Event Loggers

- [File System Event Logger]({{<ref "/docs/file-system-event-logger/introduction" >}})
- [URL Logger]({{<ref "/docs/url-logger/introduction" >}})
- [Apache Kafka Logger]({{<ref "/docs/apache-kafka-logger/introduction" >}})
- [MQTT Logger]({{<ref "/docs/mqtt-logger/introduction" >}})
- [Rabbit MQ Logger]({{<ref "/docs/rabbitmq-logger/introduction" >}})
- [HL7 Logger]({{<ref "/docs/hl7-logger/introduction" >}})
- [Office 365 Email Logger]({{<ref "/docs/office365-email-logger/introduction" >}})
- [IMAP4 Email Logger]({{<ref "/docs/imap4-email-logger/introduction" >}})
