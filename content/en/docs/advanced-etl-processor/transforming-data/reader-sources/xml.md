---
author: Peter Jonson
title: XML Reader
description: XML Reader
draft: false
tags: ['Reader', 'XML']
date: 2022-09-17
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## About XML

Extensible Markup Language (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. It is defined in the XML 1.0 Specification produced by the W3C, and several other related specifications, all gratis open standards.

The design goals of XML emphasize simplicity, generality, and usability over the Internet. It is a textual data format with strong support via Unicode for the languages of the world. Although the design of XML focuses on documents, it is widely used for the representation of arbitrary data structures, for example in web services.

Source: [Wikipedia](https://en.wikipedia.org/wiki/XML)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml.png" title="XML Editor" >}}

## XML Editor

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-editor.png" title="XML Editor" >}}

## Simple XML file example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-simple.png" title="Simple XML file example" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-ignore-tags-is-checked.png" title="XML ignore tag is checked" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-simple-data.png" title="Simple XML data example" >}}

**Note:**
[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)will also bring in all data between table and row tag if Ignore tags is not checked. For complex XML files it is also possible to apply XSLT transformations (Transform XML Checked)

## More Complex XML file example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-complex.png" title="More Complex XML file example" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-ignore-tags-is-not-checked.png" title="XML ignore tag is not checked" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-complex-data.png" title="More Complex XML file example" >}}

## Complex XML file example

XML is very flexible format but the flexibility makes XML difficult to work. For example some xml tags might me missing or be in deferent order. XSLT is used to address this issue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-complex-example.png" title="Complex XML file example" >}}

## About XSLT

XSLT (Extensible Stylesheet Language Transformations) is a language for transforming XML documents into other XML documents, or other objects such as HTML for web pages, plain text or into XSL Formatting Objects which can then be converted to PDF, PostScript and PNG.

Typically, input documents are XML files, but anything from which the processor can build an XQuery and XPath Data Model can be used, for example relational database tables, or geographical information systems.

Source: [Wikipedia](https://en.wikipedia.org/wiki/XSLT)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-reader-properties.png" title="XSLT" >}}

## Data Without Transformation

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-data-without-transformation.png" title="Data Without Transformation" >}}

## XSLT Transformation

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-xslt-transformation.png" title="XSLT Transformation" >}}

## Result of XSLT Transformation

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/xml-xslt-transformation-result.png" title="Result of XSLT Transformation" >}}

- [Advantages and disadvantages of working with XML]({{<ref "/knowledgebase/tips/adnvantages-and-disadvantages-of-working-with-xml" >}})
- [XML and HTML Transformation Functions]({{<ref "/docs/advanced-etl-processor/transformation-functions/xml-and-html" >}})
