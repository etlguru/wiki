---
author: Maria Salter
title: Using Variables
description: This article describes using variables for ETL automation
draft: false
tags: ['Knowledgebase', 'Variables', 'Agent']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## What are the variables?

Variable has a name and a value. During execution, the variable name is replaced with a value.
Variables provide a convenient way of passing parameters between various objects. They also can be used to store settings between sessions.

### Global Variables

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-ael-properties.png" title="Global Variables" >}}

### Usage Example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-bde-connection.png" title="BDE Connection using Global Variable" >}}

## Using variables to loop through the list of directories

### Package Example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-package.png" title="Working With Variables Package" >}}
\
Lists files in directories and saves it into the file.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-file-operation.png" title="Working With Variables File Operation" >}}
\
The file name is saved into the variable.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-file-operation-variables.png" title="File Operation Variables" >}}
\
Loop loads list of files and loops through the list one by one

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-loop-properties.png" title="Loop Properties" >}}
\
Script sets variable \<BDEDIR> to directory path

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-variables-script-properties.png" title="Script Properties" >}}
\
Transformation loads the data

## Video Tutorial

{{< youtube id="W86a9GIOGEA" class="ratio ratio-16x9" >}}
\
{{< youtube id="QDsw7aP4wlg" class="ratio ratio-16x9" >}}

{{< aetl >}}
