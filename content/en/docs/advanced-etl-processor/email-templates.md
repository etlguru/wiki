---
author: Peter Jonson
title: Email Templates
description: Email Templates
draft: false
tags: ['Email', 'SMTP', 'POP3', 'IMAP4']
date: 2022-09-09
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

Email templates is a library of the most often used email texts. These can be used when automating processes such as when a set of transformations have taken place. Individual emails can then be set for various departments or management. For example, most of the packages will have notification email to the administrator.

For instance, if a package fails it will be necessary to inform about the fact. An email template allows specific variables and information to be provided relating to the package failure. In addition, email templates can be used to attach the actual execution log relating to the specific problem occurrence. For instance, a typical message about this sent in an email might be:

“Package has failed please find attached execution log.”

One of the advantages of the approach of using email templates is that they save a lot of time designing and sending emails individually. Another factor is that the email system reports incidents as they occur, and are not sent on after the event has finished.

## Template

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/email-templates-1.png" title="Email templates" >}}

In the example, email template below you can see that certain variables have been defined. These variables are replaced by “actual” values at runtime, or when the incident occurs.

## Email Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/email-templates-2.png" title="Email templates" >}}

Email templates can be used to indicate incidents, end of processes, commencement of processes, the results of processes and a variety of other business uses.

{{< aetl >}}
