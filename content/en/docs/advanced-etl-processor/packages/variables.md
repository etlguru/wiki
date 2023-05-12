---
author: Peter Jonson
title: Using Variables
description: Using Advanced ETL Processor Variables
draft: false
tags: ['Package', 'Variables']
date: 2022-09-26
group: advanced-etl-processor-enterprise-package
menu: advanced-etl-processor-enterprise
layout: docs
weight: 4
---

Variables are used to pass information between objects. For example, SQL script has failed and you would like to email the SQL to the developer. Insert <sql>
Into email message and it will be replaced with actual SQL

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/using-variables-1.png" title="Using Variables" >}}

## Variables Inside loops

Before any object is executed the variable is replaced with the actual value

"Before any object is executed the variable is replaced with the actual value", this statement is essential.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-package.png" title="Variables Inside loops" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-sql.png" title="Variables Inside loops" >}}

When execution starts variable \<Email> does not exist

When the "select \'<Email>' as Email" is executed the first time everything works as expected, the email is sent ETC.

However, when it is executed the second time\ '<Email>' is replaced with an actual variable value.
(remember "before any object is executed the variables are replaced with the actual value")

so instead of "select \'<Email>' as Email"

"select 'VariableValue' as Email" is executed

The solution to this problem is straightforward.
Put another set variable after "Send an email action" and set \<Email> to \<Email>

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable.png" title="Variables Inside loops" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/set-variable-1.png" title="Variables Inside loops" >}}

## Creating Variables

There are several ways to create variables

- Using script action
- Using transformation action
- Using calculation object within transformation action
- Using Set Variable Action
- Using Global Variables

## Predefined Variables List

```
<username>
<computername>
<datetime>

<Project Name>
<Project ID>
<Package Name>
<Package ID>
<Package Group>
<Package Item Log Name>
<Current Package Item Name>
<Actual Execution Status>
<Execution Status>

<Main Package Log Name>
<Package Item Log Name>
<Rejected Records File Name>

<LAST EMAIL>

<QUEUE_ID>
<SuccessfulActionsCount>
<FailedActionsCount>

<CommonDocumentsDir>
<CommonAppDataDir>
<LocalAppDataDir>
<AppDataDir>

<Version>
<Repository Connection String>

<LicenseRegisteredOwner>
<LicenseCreated>
<LicenseValidUntil>
<LicenseType>
<LicenseIsTrial>
<LicenseSupportExpired>
<LicenseDaysLeft>
```

## Package Action Variables

Every Action has a predefined set of variables

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/smtp-action-variables.png" title="Package Action Variables" >}}
\
Once action execution is completed values are assigned to enabled variables

## Video Tutorial

{{< youtube id="W86a9GIOGEA" class="ratio ratio-16x9" >}}
\
{{< youtube id="QDsw7aP4wlg" class="ratio ratio-16x9" >}}

{{< aetl >}}
