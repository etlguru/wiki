---
author: Maria Salter
title: Extracting Information from MSG files
description: Learn how to extract data from MSG files
draft: false
tags: ['Knowledgebase', 'MSG', 'Python', 'EMail']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

## Preparation

Download and install python from https://www.python.org/downloads

open command prompt and run:

{{< command >}}
pip install https://github.com/mattgwwalker/msg-extractor/zipball/master
{{< /command >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/extract-msg.png" title="Extract data from MSG file" >}}
\
This will install msg-extractor python library for working with MSG files

The python script ExtractMsg.py automates the extraction of key email data (from, to, cc, date, subject, body) and the email's attachments.

https://github.com/mattgwwalker/msg-extractor/

## Running python scripts from package

Is done by using "Script" Package Action:

{{< image class="mx-auto d-block"  src="/images/knowledgebase/extract-data-from-msg-file.png" title="Script Package Action" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/set-file-name.png" title="Set File Name" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/extract-data-from-msg-file-script.png" title="Script to extract data from MSG file" >}}

## Python script

```python
import ExtractMsg,os,etltools

msg = ExtractMsg.Message(etltools.GetVariable('<FileName>'))
etltools.SetVariable('<MessageSender>',msg.sender)
etltools.SetVariable('<MessageSentDate>',msg.date)
etltools.SetVariable('<MessageSubject>',msg.subject)
etltools.SetVariable('<MessageBody>',msg.body)

oldDir = os.getcwd()

os.chdir(etltools.GetVariable('<DirectoryName>'))

for attachment in msg.attachments:
attachment.save()

os.chdir(oldDir)

Result.Value = 1
```

{{< aetl >}}
