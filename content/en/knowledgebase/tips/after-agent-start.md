---
author: Maria Salter
title: After Agent Start
description: This option allows to start object execution immediately after Agent Start, it is especially useful for continually working packages and transformations
draft: false
tags: ['Knowledgebase', 'Scheduler', 'Agent']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

**After Agent Start**

This option allows to start object execution immediately after Agent Start, it is especially useful for continually working packages and transformations

{{< image class="mx-auto d-block"  src="/images/knowledgebase/schedule.png" title="Schedule" >}}

{{< alert color="secondary" >}}From time to time we have to install windows patches and reboot the server.\
After that, we have to start manually our HL7 transformation tasks using run once\
They are continually listening to the TCP/IP port.\
With these options, we are able to avoid manual intervention.\
Tom{{< /alert >}}

{{< aetl >}}
