---
author: Maria Salter
title: Loading data from HTML tables
description: This article demonstrates loading data from HTML tables
draft: false
tags: ['Knowledgebase', 'HTML', 'XSLT', 'XML']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

The problem with HTML that although it looks like XML it is not properly formatted.

Here is more information:

http://xml.silmaril.ie/conversion.html.

Likely there is a very useful utility called Tidy:

http://tidy.sourceforge.net

It allows converting HTML to proper XML format.

**Usage example:**

tidy -config config.txt -f errs.txt -m "my-html-file.html"

**Sample config file for HTML tidy**

```
indent: auto
indent-spaces: 2
wrap: 72
markup: yes
output-xml: yes
input-xml: no
show-warnings: yes
numeric-entities: yes
quote-marks: yes
quote-nbsp: yes
quote-ampersand: no
break-before-br: no
uppercase-tags: no
uppercase-attributes: no
char-encoding: latin1
new-inline-tags: cfif, cfelse, math, mroot,
mrow, mi, mn, mo, msqrt, mfrac, msubsup, munderover,
munder, mover, mmultiscripts, msup, msub, mtext,
mprescripts, mtable, mtr, mtd, mth
new-blocklevel-tags: cfoutput, cfquery
new-empty-tags: cfelse
```

Once HTML is converted into XML format you can use XSLT to extract the data you need.

**Here is an example:**

- [ETL and Xslt]({{<ref "etl-and-xslt" >}})

https://www.etl-tools.com/wiki/knowledgebase:etl_and_xslt

**Further reading:**
https://www.w3.org/People/Raggett/tidy/

**It is also possible to convert HTML using scripts:**

https://www.etl-tools.com/forum/visual-importer/8535-processing-html-pages-as-input.html

{{< aetl >}}
