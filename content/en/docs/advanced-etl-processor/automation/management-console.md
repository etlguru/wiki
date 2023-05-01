---
author: Peter Jonson
title: Management Console
description: Manage schedule, view execution logs and monitor ETL server nodes
draft: false
tags: ['Automation', 'Monitor']
date: 2022-09-28
group: advanced-etl-processor-enterprise-execution-automation
menu: advanced-etl-processor-enterprise
layout: docs
---

Management Console is a Microsoft Windows service which helps users to monitor the execution of **Advanced ETL Processor** and **Visual Import ETL** objects.

{{< alert color="secondary" >}}
Management Console is only available with Enterprise Version.
{{< /alert >}}

## Installing Management Console

Management Console service is automatically installed during setup but not configured.

The Management Console is installed using the command line.

{{< command >}}
amc.exe /INSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vmc.exe /INSTALL
{{< /command >}}

for Visual Importer ETL

To uninstall the Management Console as a Windows service you must run the Management Console with the /UNINSTALL switch as follows

{{< command >}}
amc.exe /UNINSTALL
{{< /command >}}

for Advanced ETL Processor

{{< command >}}
vmc.exe /UNINSTALL
{{< /command >}}

for Visual Importer ETL

Once service is installed and running open internet explorer and run

[http://localhost:8080/index.html](http://localhost:8080/index.html)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/management-console.png" title="About Management Console" >}}\
\
{{< alert color="secondary" >}}
We recommended running the management console service using the same user you use to design actions.\
Default Username and password are Administrator/Administrator.\
A list of users is stored in the repository\
The default port is 8080, to change the port edit port.ini file in the settings folder
{{< /alert >}}

## Video Tutorial

{{< youtube id="Q814WexRfDs" class="ratio ratio-16x9" >}}

{{< aetl >}}
