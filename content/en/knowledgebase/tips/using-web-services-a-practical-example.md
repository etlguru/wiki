---
author: Maria Salter
title: Using web services a practical example
description: This article provides an example of working with Web services
draft: false
tags: ['Knowledgebase', 'webhook', 'Web Services', 'SOAP', 'XML', 'REST']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Based on the customer feedback in the latest version of Advanced ETL Processor we have introduced support for the web services

## What are the web services.

The simplest way to describe it is a way of communicating with the web servers. The application sends a request to the webserver using XML and receives back a reply as XML. One of the examples would be converting Fahrenheit to Celsius or getting the current currency exchange rate. A lot of modern websites such as eBay, Amazon is using web services as a standard API for developers.

## Converting Fahrenheit to Celsius

In order to communicate with temperature conversion web service we need to build HTTP Request Header and HTTP Request Body dynamically, There are several ways of doing it the easiest way is to use "In Place Replace transformation" function

## Generating HTTP Request Header

{{< image class="mx-auto d-block"  src="/images/knowledgebase/http-request-header.png" title="Generating HTTP Request Header" >}}
\
{{< alert color="secondary" >}}During execution #value# is replaced with body length{{< /alert >}}

## HTTP Request Body

{{< image class="mx-auto d-block"  src="/images/knowledgebase/http-request-body.png" title="HTTP Request Body" >}}
\
{{< alert color="secondary" >}}During execution #value# is replaced with temperature{{< /alert >}}

## Web Service URL

{{< image class="mx-auto d-block"  src="/images/knowledgebase/web-service-lookup-properties.png" title="Web Service URL" >}}

## Transformation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/transformation1-4.png" title="Transformation" >}}
\
{{< alert color="secondary" >}}There is a detailed example in the default repository{{< /alert >}}

{{< aetl >}}
