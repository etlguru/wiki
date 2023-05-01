---
author: Maria Salter
title: Advantages and disadvantages of working with XML
description: Advantages and disadvantages of working with XML
draft: false
tags: ['Knowledgebase', 'XML', 'XSLT', 'ETL']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

Loading data from XML can be a very complex task, but the complexity of this task depends on people who design XML in the first place. In this article, we will provide you with some examples of loading data from XML files and transforming it. We will also talk about things to avoid and how to make the life of developers easier.

## What is XML anyway?

Extensible Markup Language (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. It is defined in the XML 1.0 Specification produced by the W3C, and several other related specifications, all gratis open standards.
The design goals of XML emphasize simplicity, generality, and usability over the Internet. It is a textual data format with strong support via Unicode for the languages of the world. Although the design of XML focuses on documents, it is widely used for the representation of arbitrary data structures, for example in web services.

Source: Wikipedia

XML is incredibly flexible, but it has some disadvantages as well.

**For example:**

```xml
<CustomerOrderMessage>
<OrderNumber>1</OrderNumber>
</CustomerOrderMessage>
```

The XML above has only one byte of information the rest of it is metadata. Using too much metadata requires more processor power and increase network traffic(Which is great news for hardware vendors, but bad news for the people who have to pay for it)

The flexibility of XML can lead to unnecessary complexity and it can make it hard for developers to understand, therefore lead to mistakes and development time and cost increases.

In some of the cases, it can be necessary to convert XML into a simplified format so it can be loaded into the database.
This XML can be loaded by most of the ETL tools.

{{< alert color="secondary" >}}CustomerTable is a "Table tag" and CustomerRecord is a "Record Tag"{{< /alert >}}

```xml
  <CustomerTable>
  <CustomerRecord>
  <CustomerID>1</CustomerID>
  <CustomerName>Peter Jones</CustomerName>
  </CustomerRecord>
  <CustomerRecord>
  <CustomerID>2</CustomerID>
  <CustomerName>Bill Watson</CustomerName>
  </CustomerRecord>
  </CustomerTable>
```

This XML may need to be transformed in the format above so it can be loaded into the database later:

```xml
  <CustomerTable>
  <CustomerRecord CustomerID="1" CustomerName="Peter Jones"/>
  <CustomerRecord CustomerID="2" CustomerName="Bill Watson"/>
  </CustomerTable>
```

And as a Conclusion here is some basic XML design tips:

- Use XML when it is necessary
- Too much metadata is a bad thing
- Keep tags short
- Keep it simple and clean
- Check ETL documentation and design XML in such a way so it can be loaded without conversion

{{< aetl >}}
