---
author: Peter Jonson
title: Change Encoding Action
description: Change Encoding Action provides a convenient way of conversing between more 100 character sets
draft: false
tags: ['Package', 'Action', 'Encoding']
date: 2023-03-18

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

Change Encoding Action provides a convenient way of conversing between more 100 character sets including

## Full Unicode

- UTF-8
- UCS-2, UCS-2BE, UCS-2LE
- UCS-4, UCS-4BE, UCS-4LE
- UTF-16, UTF-16BE, UTF-16LE
- UTF-32, UTF-32BE, UTF-32LE
- UTF-7

## European Languages

- ASCII
- ISO-8859-{1, 2, 3, 4, 5, 7, 9, 10, 13, 14, 15, 16}
- KOI8-R, KOI8-U, KOI8-RU
- Windows-{1250, 1251, 1252, 1253, 1254, 1257, 1131}
- CP{437, 737, 775, 850, 852, 853, 855, 857, 858, 860, 861, 863, 865, 866, 869, 1125}
- Mac{Roman, CentralEurope, Iceland, Croatian, RomaniaCyrillic, Ukraine, Greek, Turkish}

## Semitic Languages

- ISO-8859-{6, 8}
- CP{255, 1256}
- CP{862, 864}
- Mac{Hebrew, Arabic}

## Japanese

- EUC-JP
- SHIFT_JIS
- P932
- ISO-2022-JP, ISO-2022-JP-1, ISO-2022-JP-2, ISO-2022-JP-3
- EUC-JISX0213
- Shift_JISX0213

## Chinese

- EUC-CN
- HZ, GBK
- GBK, CP936
- GB18030
- EUC-TW
- BIG5, BIG5-HKSCS, BIG5-HKSCS:2004, BIG5-HKSCS:1999, BIG5-HKSCS:2001, BIG5-2003 (experimental)
- CP950
- ISO-2022-CN, ISO-2022-CN-EXT

## Korean

- EUC-KR
- CP949
- ISO-2022-KR
- JOHAB

## Armenian

- ARMSCII-8

## Georgian

- Georgian-Academy
- Georgian-PS

## Tajik

- KOI8-T

## Kazakh

- PT154
- RK1048

## Thai

- ISO-8859-11
- TIS-620
- CP874
- MacThai

## Laotian

- MuleLao-1
- CP1133

## Vietnamese

- VISCII
- TCVN
- CP1258

## Platform specifics

- ATARIST
- HP-ROMAN8
- NEXTSTEP
- RISCOS-LATIN1

## Turkmen

- TDS565

## Other

- C99
- JAVA

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/change-file-encoding-1.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/change-file-encoding-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/change-file-encoding-3.png" title="After execution tab" >}}

{{< aetl >}}
