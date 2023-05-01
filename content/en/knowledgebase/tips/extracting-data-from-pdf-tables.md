---
author: Maria Salter
title: Extracting Text from PDF table
description: Learn how to extract Text from PDF Table
draft: false
tags: ['Knowledgebase', 'PDF', 'PDF Table']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Preparation

Download and install python from https://www.python.org/downloads

open command prompt and run:

{{< command >}}
pip install pdfminer
{{< /command >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pdfminer.png" title="PDF Miner" >}}

This will install PDFMiner python library for working with PDF files

PDFMiner is a tool for extracting information from PDF documents. Unlike other PDF-related tools, it focuses entirely on getting and analyzing text data. PDFMiner allows obtaining the exact location of texts on a page, as well as other information such as fonts or lines. It includes a PDF converter that can transform PDF files into other text formats (such as HTML). It has an extensible PDF parser that can be used for other purposes instead of text analysis.

https://pypi.python.org/pypi/pdfminer/

## Extracting data from PDF tables

With the help of [stackoverflow](https://stackoverflow.com/questions/36902496/python-pdfminer-pdf-to-csv) we created pdftable2csv.py python script which can be downloaded from [here](https://www.etl-tools.com/dmdocuments/pdftable2csv.zip)

This command will convert PDF tables into csv file:

{{< command >}}
python C:\Python27\Scripts\pdftable2csv.py 2 CDE-Report1.pdf CDE-Report1.csv
{{< /command >}}

Where "2" is the distance multiplier after which a character is considered part of a new word/column/block. Usually, 1.5 works quite well

## Running python scripts from package

Is done by using "External application" Package Action:

{{< image class="mx-auto d-block"  src="/images/knowledgebase/pdftables1.png" title=" PDF tables" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/pdftables2.png" title=" PDF tables" >}}

## Dealing with Encrypted PDF files

QPDF.exe is here to help

{{< command >}}
qpdf -password= --decrypt test.pdf test1.pdf
{{< /command >}}

{{< alert color="secondary" >}}Note: Some pdf files are actually encrypted with empty passwords{{< /alert >}}

{{< aetl >}}
