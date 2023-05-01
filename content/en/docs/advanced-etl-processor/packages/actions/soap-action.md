---
author: Peter Jonson
title: SOAP Action
description: SOAP Package Action
draft: false
tags: ['Package', 'Action', 'SOAP']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

## About SOAP

SOAP stands for the Simple Object Access Protocol is a protocol that allows the exchange of structured XML data
The SOAP protocol is fully described at http://www.w3.org/TR/SOAP.

## Using SOAP

The basic principle workflow is very simple:

The software submits XML (or JSON) using the HTTP POST method to a certain address and gets a response which is saved into the file

## SOAP Action Properties

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-package-action.png" title="SOAP Action Properties" >}}

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-1.png" title="Workflow tab" >}}

## Soap content tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-2.png" title="Soap content tab" >}}

## Soap parameters tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-3.png" title="Soap parameters tab" >}}

## HTTP headers tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-6.png" title="HTTP headers tab" >}}

## Execution result tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-4.png" title="Execution result tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/soap-action-5.png" title="After execution tab" >}}

{{< aetl >}}
