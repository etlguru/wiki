---
author: Maria Salter
title: Switching from Production to Development environment
description: This article describes how to use Global Variables to switch from Production to Development environment
draft: false
tags: ['Knowledgebase', 'Global Variables', 'Variables']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

The **Global Variables** are stored in the options.ini file, this allows to use different settings on different computers.

**Here is a very simple example: two computers sharing the same repository using a different server for transformations**

{{< image class="mx-auto d-block"  src="/images/knowledgebase/production-environment.png" title="Production Environment" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/development-environment.png" title="Development Environment" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/database-options.png" title="Database Options" >}}

{{< alert color="secondary" >}}Please be very careful with this option it is very easy to make a mistake and run transformation against the wrong database {{< /alert >}}

{{< aetl >}}
