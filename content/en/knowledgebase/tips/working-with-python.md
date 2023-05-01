---
author: Maria Salter
title: Working with Python
description: Using python for ETL Transformation and automation
draft: false
tags: ['Knowledgebase', 'Python']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Preparation

Download and install python from https://www.python.org/downloads

{{< alert color="secondary" >}}To avoid issues install it for all users{{< /alert >}}

## Python Version

- Our software automatically detects the version of python installed, and loads relevant DLL.
- 32-bit version of our software uses the 32-bit version of python and
- 64-bit version of our software uses the 64-bit version of python

## Tranforming data using Python

Here is a very basic example where we are converting a string into the upper case using python

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythontranformation1.png" title="Python Tranformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythontranformation2.png" title="Python Tranformation" >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythontranformation3.png" title="Python Tranformation" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythontranformation4.png" title="Python Tranformation" >}}
\
Using scripts is the slowest way to transform the data and it should be avoided.
If you do not know how to transform the data ask the question here and we will help you.

## Using Python inside package

The script checks a number of the day and shows an appropriate message

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythonscript.png" title="Python Script" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/pythonscript2.png" title="Python Script" >}}

## Execution Result

The execution result is determined by Result.Value, Result.Value=1 means success and Result.Value=0 means failure

## etltools package

"etltools" package provides a way of communication between python and our software.\\
It is only available when python is run from our software.

### Supported functions:

```python
etltools.GetVariable('<VariableName>')\
etltools.SetVariable('<VariableName>','Important Value')\
etltools.WriteToLog('Important Message')\
etltools.ExecuteObject(ObjectID)
```

Use ExecuteObject to execute object from the script inside the package

It returns the result of the package/transformation execution that was called.

- 0 = success
- 1 = failure

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/using-command-line-interface.png" title="UDsing Command Line Interface" >}}

## More Examples

- [Extracting text from PDF file]({{<ref "extracting-text-from-pdf-file" >}})
- [Extracting data from PDF tables]({{<ref "extracting-data-from-pdf-tables" >}})
- [Extracting Information from MSG Files]({{<ref "extracting-information-from-msg-files" >}})

{{< aetl >}}
