---
author: Peter Jonson
title: Date formats
description: Date formats
draft: false
tags: ['Date formats']
date: 2022-09-17
group: advanced-etl-processor-enterprise
menu: advanced-etl-processor-enterprise
layout: docs
---

Date/Time format strings control the conversion of strings into date time type.

Date/Time format strings are composed from specifiers which describe values to be converted into the date time value.

In the following table, specifiers are given in lower cases. Case is ignored in formats, except for the "am/pm" and "a/p" specifiers.
{{< table "table-striped table-bordered" >}}

| Specifier | Description                                                                                                                  |
| --------- | ---------------------------------------------------------------------------------------------------------------------------- |
| d         | Day as a number without a leading zero (1-31).                                                                               |
| dd        | Day as a number with a leading zero (01-31).                                                                                 |
| m         | Month as a number without a leading zero (1-12).                                                                             |
| mm        | Month as a number with a leading zero (01-12).                                                                               |
| mmm       | Month as an abbreviation (Jan-Dec).                                                                                          |
| mmmm      | Month as a full name (January-December).                                                                                     |
| yy        | Year as a two-digit number (00-99).                                                                                          |
| yyyy      | Year as a four-digit number (0000-9999).                                                                                     |
| h         | Hour without a leading zero (0-23).                                                                                          |
| hh        | Hour with a leading zero (00-23).                                                                                            |
| n         | Minute without a leading zero (0-59).                                                                                        |
| nn        | Minute with a leading zero (00-59).                                                                                          |
| s         | Second without a leading zero (0-59).                                                                                        |
| ss        | Second with a leading zero (00-59).                                                                                          |
| fff       | Fraction of Second with a leading zero (000-999). (Works only for oracle time stamp fileds)                                  |
| tt        | Uses the 12-hour clock for the preceding h or hh specifier, 'am' for any hour before noon, and 'pm' for any hour after noon. |

{{< /table >}}

Important thing is to understand that this format has nothing to do with your target database.
This is the format of the source data. It is there to help to covert string into date time type
inside of the software, so it can be loaded later into date or timestamp field

So if source data is:

- 16/08/2009 than the format is DD/MM/YYYY
- 1/31/2009 than the format is M/D/YYYY
- 2006-05-23 22:34:42.096 than the format is YYYY-MM-DD HH:NN:SS.FFF
- 1992/mar/12 00:00 than the format is YYYY/MMM/DD HH:NN

**Performance**

- Applying date/time format is a very processor intensive operation,
- Shorter formats are faster,
- Formats with no months names are faster as well,
- dd/mm/yyyy is faster than d/m/yy.

{{< aetl >}}
