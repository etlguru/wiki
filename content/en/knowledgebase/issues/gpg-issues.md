---
author: Maria Salter
title: Investigating Gpg4win Issues
description: This article describes how to investigate Gpg4win Issues
draft: false
tags: ['Knowledgebase', 'Gpg4win', 'Gpg']
date: 2022-04-26
group: knowledgebase-issues
layout: docs
---

## Problem

When running gpg.exe from windows service it might fail for no obvious reason.

## Logging

The easiest way to understand what is wrong is to enable logging:

- Run Cleopatra
- Click Settings => configure Cleopatra
- Select GnuPG System tab
- Set debugging level to verbose
- Set log file name

{{< image class="mx-auto d-block"  src="/images/knowledgebase/gpg4win-how-to-enable-logging.png" title="Gpg4win How To Enable Logging" >}}

## Log Example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/gpg4win-log-example.png" title="Gpg4win Log Example" >}}

{{< aetl >}}
