---
author: Maria Salter
title: Loading data files from different operating systems
description: This article describes solutions to common problems of loading data into the database from different operating systems
draft: false
tags: ['Knowledgebase', 'Text', 'Encoding']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

**This article describes common problems of loading data into the database from different operating systems.**

## Typical situation:

You have a sales data warehouse. Every day there are hundreds of small files to process. They come from various locations.
ETL tool downloads the files into one folder then loads them into the Data warehouse using a mask.

One morning you get a call from the Manager saying that the load failed and there several thousands of files to process...

{{< image class="mx-auto d-block"  src="/images/knowledgebase/loading-data-files-from-different-operating-systems.png" title="Loading text files from different operating systems" >}}

## So what could be the problem?

- Maybe the file format has changed.
- You open the file in the notepad and looks the same...

{{< alert color="secondary" >}}Most likely the format is different but you just can't see the difference{{< /alert >}}

**There are only two possible causes.**

*Different encoding for example UTF8 instead of ASCI
*Different end of line characters for example LF instead of CR+LF

Data is coming from different data sources some users use Windows, some use MAC, some use UNIX/Linux

Systems based on ASCII or a compatible character set use either LF (Line feed, '\n', 0x0A, 10 in decimal) or CR (Carriage return, '\r', 0x0D, 13 in decimal) individually, or CR followed by LF (CR+LF, 0x0D 0x0A). Some rare systems, such as QNX before version 4, used the ASCII RS (record separator, 0x1E, 30 in decimal) character as the newline character.

**LF**: Multics, Unix and Unix-like systems (GNU/Linux, AIX, Xenix, Mac OS X, FreeBSD, etc.), BeOS, Amiga, RISC OS, and others\
**CR+LF**: DEC RT-11 and most other early non-Unix, non-IBM OSes, CP/M, MP/M, DOS (MS-DOS, PC-DOS, etc.), OS/2, Microsoft Windows, Symbian OS, Palm OS\
**CR**: Commodore 8-bit machines, TRS-80, Apple II family, Mac OS up to version 9 and OS-9\
**RS**: QNX pre-POSIX implementation.

The Unicode standard defines a large number of characters that conforming applications should recognize as line terminators:

**LF**: Line Feed, U+000A\
**FF**: Form Feed, U+000C\
**CR**: Carriage Return, U+000D\
**CR+LF**: CR (U+000D) followed by LF (U+000A)\
**NEL**: Next Line, U+0085\
**LS**: Line Separator, U+2028\
**PS**: Paragraph Separator, U+2029

## The Solution

[Use Advanced ETL Processor](https://www.etl-tools.com/etl-tools/advanced-etl-processor/overview.html)

{{< alert color="success" >}}Latest Version of [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor//overview.html) and [Visual Importer ETL](https://www.etl-tools.com/visual-importer-etl-enterprise/overview.html) can automatically determine source file encoding and works with multiple Line Terminators{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/data-reader-properties-2.png" title="Data Reader Properties" >}}

{{< aetl >}}
