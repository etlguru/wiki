---
author: Maria Salter
title: Extracting Text from PDF File
description: Learn how to extract Text from PDF File
draft: false
tags: ['Knowledgebase', 'PDF', 'Python']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Preparation##

Download and install python from https://www.python.org/downloads

open command prompt and run:

{{< command >}}
pip install pdfminer
{{< /command >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pdfminer.png" title="PDF Miner" >}}

This will install PDFMiner python library for working with PDF files

PDFMiner is a tool for extracting information from PDF documents. Unlike other PDF-related tools, it focuses entirely on getting and analyzing text data. PDFMiner allows obtaining the exact location of texts in a page, as well as other information such as fonts or lines. It includes a PDF converter that can transform PDF files into other text formats (such as HTML). It has an extensible PDF parser that can be used for other purposes instead of text analysis.

https://pypi.python.org/pypi/pdfminer/

## Extracting data

PDFMiner has a very useful script called pdf2txt.py

It can be used to convert data into Text, XML or HTML.

This command will extract text information from PDF file:

{{< command >}}
python C:\Python27\Scripts\pdf2txt.py -o test.txt -t text test.pdf
{{< /command >}}

## Running python scripts from package

Is done by using "External application" Package Action:

{{< image class="mx-auto d-block"  src="/images/knowledgebase/externalapplication.png" title="External application" >}}

## Dealing with Encrypted PDF files

QPDF.exe is here to help

{{< command >}}
qpdf -password= --decrypt test.pdf test1.pdf
{{< /command >}}

{{< alert color="secondary" >}}Note: Some pdf files are actually encrypted with empty passwords{{< /alert >}}

{{< aetl >}}
