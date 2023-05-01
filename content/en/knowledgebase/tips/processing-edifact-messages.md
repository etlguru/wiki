---
author: Maria Salter
title: Processing EDIFACT Messages
description: Learn how to transform EDI/EDIFACT messages
draft: false
tags: ['Knowledgebase', 'EDIFACT', 'EDI']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## What is EDI/EDIFACT message?

EDI provides a technical basis for commercial "conversations" between two entities, either internal or external. EDI constitutes the entire electronic data interchange paradigm, including the transmission, message flow, document format, and software used to interpret the documents. EDI standards describe the rigorous format of electronic documents.

In essence, an EDI message is just a small text file that can be sent via email, HTTP or FTP

## Message Example

```
UNH+199700001+INVOIC:D:93A:UN:EAN007'
BGM+380+424876'
DTM+137:199701111045:203'RFF+ON:334411'
RFF+AAK:23149'
NAD+BY+7080001000004::9++Hans Hansen AS+Storgata 1+TRONDHEIM++7005'
NAD+SU+7080000366767::9++Børsterud AS+Industriveien 1+OSLO++0580'
FII+RH+60731108042'
RFF+VA:FORETAKSREGISTERET NO123456789MVA'
CTA+AD+Lise Hansen'
NAD+IV+7080001000011::9++Hans Hansen Øst AS+Grenseveien 1+HEBEKK++1406'
NAD+DP+7080001000028::9++Hans Hansen Midt AS+Heggeveien 1+HEIMDAL++7080'
NAD+SF+7080000000065::9++Børsterud AS, Vareutlevering+Industriveien 1+OSLO++0580'
PAT+1'
DTM+7:19970110:102'
PAT+3'
DTM+13:19970630:102'
TOD+3++EXW'
LIN+1++7030432630011:EN'
PIA+1+7200018:SA::91'
IMD+FL++:::RULLESYSTEM'
IMD+C++TU'
QTY+47:100'
QTY+59:12'
ALI---6'
MOA+66:25000,00'
MOA+203:22000,00'
PRI+AAB:250,00'
PRI+AAA:220,00'
PAC---CT:KARTONG'
TAX+7+VAT---:::23+S'
ALC+A---+PAD:::TILBUDSRABATT'
PCD+3:10'
MOA+8:2500,00'
ALC+A---+PDE:::PALLERABATT'
MOA+8:500,00'
RTE+1:5,00'
LIN+2++7030439770710:EN'
PIA+1+2844001:SA::91'
IMD+FL++:::BØRSTER'
IMD+C++TU'
QTY+47:200'
QTY+59:36'
ALI---6'
MOA+66:2000000'
MOA+203:17900,00'
PRI+AAB:100,00'
PRI+AAA:89,50'
PAC---CT:KARTONG'
ALC+A---+PAD:::TILBUDSRABATT'
PCD+3:10'MOA+8:2000,00'
ALC+A---+QD:::KVANTUMSRABATT'
QTY+1:50'
PCD+3:2,0'
MOA+8:100,00'
UNS+S'
CNT+2:2'
MOA+66:45000,00'
MOA+203:39900,00'
MOA+260:5100,00'
MOA+131:5100,00'
MOA+NET:39900,00'
MOA+125:39900,00'
MOA+150:9177,00'
MOA+86:49077,00'
MOA+129:39900,00'
TAX+7+VAT++39900,00+:::23+S'
MOA+176:9177,00'
ALC+A---+PAD:::TILBUDSRABATT'
MOA+8:4500,00'
ALC+A---+PDE:::PALLERABATT'
MOA+8:500,00'
ALC+A---+QD:::KVANTUMSRABATT'
MOA+8:100,00'
UNT+76+199700001'
```

## Message format

{{< table "table-striped table-bordered" >}}
| EDIFACT File | Description |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| UNA:+.? | |
| UNB+UNOA:1+9377778760643:ZZ+9399700000001:ZZ+050322:1237+000000001 | Message header, with sender GLN, addressee GLN, date, time & interchange number |
| UNH+00000000000459+ORDERS:D:96A:UN:EAN008 | Message Beginning |
| BGM+220+10910220+92 | Purchase Order Number |
| DTM+137:20050322:102 | Order Date |
| DTM+2:20050322:102 | Requested Delivery Date |
| NAD+SU+1217::92 | JB Supplier Code |
| NAD+ST+304::92 | Ship to Store Code |
| NAD+IV+304::92 | Invoice to Store Code |
| LIN+1 | Item Line Number |
| PIA+5+711719347521:VN::91 | Product Identifier |
| QTY+21:10.0000:EA | Quantity |
| PRI+AAA:40.0000::TU | Price Ex GST |
| UNS+S | Message trailer |
| CNT+2:1 | Control Total (total number of item lines) |
| UNT+14+00000000000459 | Message Trailer |
| UNZ+1+000000001 | Message End |

{{< /table >}}

{{< alert color="secondary" >}}Every data part is delimited by a single quote and prefixed with some characters and they indicate which kind of data it is. For example, LIN indicates line number{{< /alert >}}

## Processing EDI Data

In order to load data into the database, we need to transfer data into a more readable format

{{< image class="mx-auto d-block"  src="/images/knowledgebase/processing-edi-messages.png" title="Processing EDI Messages" >}}

### Data reader

- We can't use fixed-width format because message lengths vary
- Better option to use delimited format but use the wrong delimiter so the entire line is read and passed to the next step

{{< alert color="secondary" >}}We can also use File System as reader connection type{{< /alert >}}

### Next step is to turn the data so every part will be in a separate record

UNH+199700001+INVOIC:D:93A:UN:EAN007'BGM+380+424876'DTM+137:199701111045:203' to

UNH+199700001+INVOIC:D:93A:UN:EAN007 [Record 1]\
BGM+380+424876'DTM+137:199701111045:203 [Record 2]

Once data is rotated we want the UNH part to go into the UNH field, BGM into the BGM field and so on.\
Since we have so many fields we will be using sub-transformation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/sub-transformation.png" title="Sub Transformation" >}}

### The logic

When field value starts with UNH+\
We pass to the next step value after UNH+\
if not we pass null\
Keep value transformation allow us to fill in holes in the data\

EG it converts:

Value1
nul
Value2
Null

into:

Value1
Value1
Value2
Value2

### Getting rid of empty values

{{< image class="mx-auto d-block"  src="/images/knowledgebase/validation-3.png" title="Remove empty values" >}}

### And duplicate the data

{{< image class="mx-auto d-block"  src="/images/knowledgebase/deduplicator-4.png" title="Data Deduplication" >}}

### Deduplication result

{{< image class="mx-auto d-block"  src="/images/knowledgebase/transformation-5.png" title="Result of deduplication" >}}

Here we can convert our data even further if we wish using various transformations

[Download sample](https://www.etl-tools.com/images/EDI/EDI.zip)

{{< aetl >}}
