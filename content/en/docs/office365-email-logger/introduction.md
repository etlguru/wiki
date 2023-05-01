---
author: Mike Rewnick
title: Introduction
description: Office365 Email Logger uses Microsoft Graph API processes email messages using the scheduler. Basic information about the message is saved into the repository database, msg files and attachments are saved on the disk
draft: false
tags: ['Office365 Email Logger', 'Introduction']
date: 2022-04-17
menu: office365-email-logger
group: office365-email-logger
layout: docs
---

Office365 Email Logger uses Microsoft Graph API processes email messages using the scheduler. Basic information about the message is saved into the repository database, msg files and attachments are saved on the disk

## About Microsoft Graph API

Microsoft Graph is the gateway to data and intelligence in Microsoft 365. It provides a unified programmability model that you can use to access the tremendous amount of data in Microsoft 365, Windows 10, and Enterprise Mobility + Security. Use the wealth of data in Microsoft Graph to build apps for organizations and consumers that interact with millions of users.

**More information**\
https://docs.microsoft.com/en-us/graph/overview

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/office365-email-logger/office365-email-logger-data-flow.png" title="Usage Example" >}}
\
{{< alert color="secondary" >}}
Office365 Email Logger works on both Windows and Linux. Please contact us if you want to run Office365 Email Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< office365-email-logger >}}
