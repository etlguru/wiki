---
author: Peter Jonson
title: Syslog Reader
description: Syslog Reader
draft: false
tags: ['Reader', 'Syslog']
date: 2022-05-11
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About

Syslog is a standard for sending and receiving notification messages–in a particular format–from various network devices. The messages include time stamps, event messages, severity, host IP addresses, diagnostics and more. In terms of its built-in severity level, it can communicate a range between level 0, an Emergency, level 5, a Warning, System Unstable, critical and level 6 and 7 which are Informational and Debugging.

## Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/syslog_example.png" title="Syslog example" >}}
\
Syslog is just an Utf8 text file with LF as end of line delimiter. Advanced ETL Processor can read Syslog files using dedicated reader. For more complex files text reader gives more flexibility.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/processing_syslog.png" title="Processing Syslog" >}}
