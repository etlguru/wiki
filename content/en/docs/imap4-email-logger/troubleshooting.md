---
author: Mike Rewnick
title: Troubleshooting
description: IMAP4 EMail Logger Troubleshooting
draft: false
tags: ['IMAP4 EMail Logger', 'Troubleshooting']
date: 2022-04-07
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

### Windows

- Stop ETL-Tools.com IMAP4 Email Logger (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\IMAP4 Email Logger\imap4-logger.exe

### Linux

{{< command >}}
sudo systemctl stop etl-tools-imap4-logger
cd /opt/etl-tools.com/imap4-logger
sudo ./imap4-logger
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-email-logger-error.png" title="Error" >}}

{{< imap4-email-logger >}}
