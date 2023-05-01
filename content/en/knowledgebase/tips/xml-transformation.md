---
author: Maria Salter
title: XML Transformation
description: Transforming XML data using XSLT
draft: false
tags: ['Knowledgebase', 'XML', 'XSLT']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Here is an XML example it is very well structured therefore there not need to perform additional transformations.

```xml
<Table>
<Record>
<ID>1</ID>
<Company>James Bond Production</Company>
<Amount>13</Amount>
</Record>
<Record>
<ID>2</ID>
<Company>Green Cloud</Company>
<Amount>14</Amount>
</Record>
</Table>
```

XML is a very flexible format and there is no guarantee that the next file received will have an exactly the same structure

**Shifted XML Tags**

This XML has different tags order

```xml
<Table>
<Record>
<Company>James Bond Production</Company>
<ID>1</ID>
<Amount>13</Amount>
</Record>
<Record>
<ID>2</ID>
<Company>Green Cloud</Company>
<Amount>14</Amount>
</Record>
</Table>
```

**Additional XML Tags**

This XML has an additional **YEAR** tag

```xml
<Table>
<Record>
<ID>1</ID>
<Company>James Bond Production</Company>
<Year>1956</Year>
<Amount>13</Amount>
</Record>
<Record>
<ID>2</ID>
<Company>Green Cloud</Company>
<Amount>14</Amount>
</Record>
</Table>
```

**XSLT Transformation**

XSLT is a way of transforming XML into a different format

```xml
<?xml version="1.0" encoding="UTF-8"?>

<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
<xsl:output method="xml" indent="yes" version="1.0"/>\
<xsl:template match="Table">

<Table>
<xsl:for-each select="Record">
<Record>
<ID><xsl:value-of select="ID"/></ID>
<Company><xsl:value-of select="Company"/></Company>
<Amount><xsl:value-of select="Amount"/></Amount>
</Record>
</xsl:for-each>
</Table>
</xsl:template>
</xsl:stylesheet>
```

{{< aetl >}}
