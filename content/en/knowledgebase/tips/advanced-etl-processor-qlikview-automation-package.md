---
author: Maria Salter
title: Advanced ETL Processor QlikView automation package
description: Advanced ETL Processor QlikView automation package
draft: false
tags: ['Knowledgebase', 'QlikView', 'Automation', 'Qlik']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

## Problem

We have a scenario where we have a large datasource that is currently used to produce a single QVW. What we would like to do is produce a number of smaller QVWs using e.g. Publisher - however, we would like to define the reload schedule and destination folders that these smaller QVWs end up in from an external MySQL table (or config file or similar), rather than through the Publisher GUI. Has anyone done anything similar, or got any recommendations on how to approach this?

## Solution

Package is executed from the lef to the right starting from "Init Variables" object

{{< image class="mx-auto d-block"  src="/images/knowledgebase/package-1.png" title="Package" >}}

First of all we've created the following table to store parameters, it can be extended if necessary

{{< image class="mx-auto d-block"  src="/images/knowledgebase/table-2.png" title="Table" >}}

**Table data:**

{{< image class="mx-auto d-block"  src="/images/knowledgebase/tabledetails-3.png" title="Table Details" >}}

### Step 1: Init variables

Variables are used to replace one string with another, for example anywhere in the package where \<RootDirectory> is found it will be replaced with C:\Customers.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/variables1-4.png" title="Init variables" >}}

### Step 2: Inc

This script ins increasing variable \<loop variable> by one (two times)

{{< image class="mx-auto d-block"  src="/images/knowledgebase/script-5.png" title="Script" >}}

### Step 3: Get Variables

This step executes the following SQL to get variables form the databases, before execution \<loop variable> is replaced with actual value

{{< image class="mx-auto d-block"  src="/images/knowledgebase/lookup-6.png" title="Lookup" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/set-variables.png" title="Set Variables" >}}

### Step 4: Create directory

This step creates directory if it does not exists

{{< image class="mx-auto d-block"  src="/images/knowledgebase/create-directory.png" title="Create Directory" >}}

### Step 5: Copy dashboard

This step copies Dashboard to just created directory, so it is easy to distribute updates

{{< image class="mx-auto d-block"  src="/images/knowledgebase/copy-dashboard.png" title="Copy Dashboard" >}}

### Step 6: Generate QVD files

This step is used to create QVD file, if it necessary to create several files we can just add more Export steps or for complex cases we can use transformation object to create QVD files

{{< image class="mx-auto d-block"  src="/images/knowledgebase/export1-10.png" title="Export" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/export2-11.png" title="Export" >}}

### Step 7: Refresh Dashboard

This step is used to Refresh QlikView dashboard, data is loaded from the same directory where Dashboard is stored

{{< image class="mx-auto d-block"  src="/images/knowledgebase/refresh-dashboard.png" title="Refresh Dashboard" >}}

### Step 8: Compress Dashboard

{{< image class="mx-auto d-block"  src="/images/knowledgebase/compressdashboard-13.png" title="Compress Dashboard" >}}

### Step 9: Email Dashboard

{{< image class="mx-auto d-block"  src="/images/knowledgebase/email-14.png" title="Email" >}}
\
{{< alert color="secondary" >}}We did spend 40 minutes designing this package, so can you{{< /alert >}}

{{< aetl >}}
