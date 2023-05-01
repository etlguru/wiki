---
author: Maria Salter
title: Email Notifications
description: This article describes how to use email to report problems with agent repository connection and execution issues
draft: false
tags: ['Knowledgebase', 'Email', 'Notifications', 'Agent']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/knowledgebase/email-notifications.png" title="Email Notifications" >}}

When this option enabled email is sent when action execution fails or when an agent fails to connect to the repository

## Example of Execution Failure Email

Automated Email from Application Name;
Execution of : Action failed
Computer Name: COMPUTER
User Name: bill
Os Version: Windows 10. (Version 6.3, Build 9600, 64-bit Edition)
App Version: 8.4.2.0
www.etl-tools.com

## Repository Connection Errors

For example, the support team may decide to reboot the database server where the repository is hosted or the server may run of disk space.

When the agent is up and running it is constantly checking repository connection, In case of failure, it will send an email notification and abort all tasks currently being executed.

Once the connection to the repository is reestablished agent will send another email and start executing scheduled tasks

## Example of Error Email

Error Message: [DBNETLIB][connectionwrite (send()).]
General network error. Check your network documentation
Computer Name: COMPUTER
User Name: bill
Os Version: Windows 8.1 (Version 6.3, Build 9600, 64-bit Edition)
Number Of Threads: 11
Repository: MS Sql Server Repository
Type: MS Sql Server
Server: COMPUTER\SQLEXPRESS2008
Database: REPOSITORY
User: sa

## Example of Reconnection Email

Error Message: Reconnected!
Computer Name: COMPUTER
User Name: bill
Os Version: Windows 8.1 (Version 6.3, Build 9600, 64-bit Edition)
Number Of Threads: 11
Repository: MS Sql Server Repository
Type: MS Sql Server
Server: COMPUTER\SQLEXPRESS2008
Database: REPOSITORY
User: sa

## Example of Agent Log

Agent log is located in the same folder as the agent itself

{{< image class="mx-auto d-block"  src="/images/knowledgebase/aetlagent-connection-failure.png" title="Example of Agent Log" >}}

{{< aetl >}}
