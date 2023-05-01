---
author: Maria Salter
title: ETL and XSLT
description: Lean how to transform XML data using XSLT
draft: false
tags: ['Knowledgebase', 'XSLT', 'XML']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Here is an XML data example

{{< image class="mx-auto d-block"  src="/images/knowledgebase/xml-with-attributes.png" title="XML data example" >}}

To load it all we need to do is to set the data source type to XML and select appropriate XML tags for "Table Tag" and "Record Tag"

## Data reader settings

{{< image class="mx-auto d-block"  src="/images/knowledgebase/xml-with-attributes-datareader.png" title="Data reader settings" >}}
\
{{< alert color="secondary" >}}"Ignore Tags" is checked{{< /alert >}}

**There is no data in the grid because we have to transform XML into a more readable format first, using XSLT.**

{{< image class="mx-auto d-block"  src="/images/knowledgebase/xml-with-attributes-data.png" title="XML With Attributes" >}}

## About XSLT

XSLT (Extensible Stylesheet Language Transformations) is a language for transforming XML documents into other XML documents, or other objects such as HTML for web pages, plain text or into XSL Formatting Objects which can then be converted to PDF, PostScript and PNG.

Typically, input documents are XML files, but anything from which the processor can build an XQuery and XPath Data Model can be used, for example, relational database tables, or geographical information systems.

Source: Wikipedia

### XSLT

{{< image class="mx-auto d-block"  src="/images/knowledgebase/xslt-transformation.png" title="XSLT Transformation" >}}
\
{{< alert color="secondary" >}}To get to this dialog: open data reader properties, click XML file, check transform XML and click Magnifying glass button{{< /alert >}}

### Result of the XSLT transformation

{{< image class="mx-auto d-block"  src="/images/knowledgebase/xslt-result.png" title="XSLT Transformation result" >}}
\
{{< alert color="secondary" >}}More information about XSLT can be found [here](http://www.w3schools.com/xsl/xsl-transformation.asp){{< /alert >}}

{{< aetl >}}
