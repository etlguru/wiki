---
author: Mike Rewnick
title: Introduction
description: HL7 Logger captures HL7 messages and stores them into the database.
draft: false
tags: ['HL7 Event Logger', 'Introduction']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

HL7 Logger captures HL7 messages and stores them into the database.

## About HL7 Protocol

Health Level Seven or HL7 refers to a set of international standards for the transfer of clinical and administrative data between software applications used by various healthcare providers. These standards focus on the application layer, which is "layer 7" in the OSI model. The HL7 standards are produced by Health Level Seven International, an international standards organization, and are adopted by other standards issuing bodies such as American National Standards Institute and International Organization for Standardization.

Hospitals and other healthcare provider organizations typically have many different computer systems used for everything from billing records to patient tracking. All of these systems should communicate with each other (or "interface") when they receive new information, or when they wish to retrieve information, but not all do so.

HL7 International specifies the number of flexible standards, guidelines, and methodologies by which various healthcare systems can communicate with each other. Such guidelines or data standards are a set of rules that allow information to be shared and processed in a uniform and consistent manner. These data standards are meant to allow healthcare organizations to easily share clinical information. Theoretically, this ability to exchange information should help to minimize the tendency for medical care to be geographically isolated and highly variable.

Source: [Wikipedia](https://en.wikipedia.org/wiki/Health_Level_7)

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/hl7-logger/hl7-logger-data-flow.png" title="Usage Example" >}}
\
{{< alert color="secondary" >}}
HL7 Logger works on both Windows and Linux. Please contact us if you want to run HL7 Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< hl7-event-logger >}}
