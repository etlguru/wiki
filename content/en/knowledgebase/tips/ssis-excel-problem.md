---
author: Maria Salter
title: SSIS Excel Problem
description: Why IMEX=1 will not solve SSIS problems with loading data from Excel
draft: false
tags: ['Knowledgebase', 'SSIS', 'Excel', 'IMEX=1']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## Solving SSIS problems with loading data from Excel

We have the following situation:

Imagine that you are working for a large finance organization and would like to load the year-end balances into the SQL Server database. The excel file looks like this.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/excel-file.png" title="Excel File" >}}
\
So we create a simple SSIS package using Excel connector and Ole DB destination, before loading the data we hit the preview button.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/preview-result-2.png" title="Preview Result" >}}
\
For some reason last 3 lines have null values, This is because our connection string has not got IMEX=1

**Provider=Microsoft.ACE.OLEDB.12.0;;Data Source=C:\DEMO\Excel\mixed_data_types.xls;Extended Properties="EXCEL 8.0;HDR=YES";**

We correct it

**Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\DEMO\Excel\mixed_data_types.xls;Extended Properties="EXCEL 8.0;HDR=YES;IMEX=1";**

{{< image class="mx-auto d-block"  src="/images/knowledgebase/preview-result2-3.png" title="Preview Result" >}}
\
That looks much better so we load the data. Later the same day, the finance manager says that the balance is wrong you look at the data and there are some null values again.

## Why we have null in the database?

{{< alert color="success" >}}**It is a common problem:** trying to load the data from Excel file half of the data is coming as nulls, or columns with more than 255 characters are truncated{{< /alert >}}

## The logic behind Excel mixed data types

Our source file has mixed data types some account codes have only numbers and some have characters as well. We have more cells with numbers only so Excel ODBC/Jet assumes the field type is numeric and shows the rest of it as nulls.

Setting IMEX=1 tells the driver to use Import mode. In this state, the registry setting ImportMixedTypes=Text will be noticed. This forces mixed data to be converted into text. For this to work reliably, you may also have to modify the registry setting, TypeGuessRows=8. The ISAM driver by default looks at the first eight rows and from that sampling determines the datatype. **If this eight-row sampling is all numeric, then setting IMEX=1 will not convert the default datatype to Text; it will remain numeric.**

As partially explained [here](https://docs.microsoft.com/en-us/office/client-developer/access/desktop-database-reference/initializing-the-microsoft-excel-driver?tabs=office-2016)

ODBC/MS Jet scans first TypeGuessRows to determine field type

### Here how Excel ODBC/MS Jet works

(TypeGuessRows=8 IMEX=1)

In your eight (8) scanned rows, if the column contains five (5) numeric values and three (3) text values, the provider returns five (5) numbers and three (3) null values.

In your eight (8) scanned rows, if the column contains three (3) numeric values and five (5) text values, the provider returns three (3) null values and five (5) text values.

In your eight (8) scanned rows, if the column contains four (4) numeric values and four (4) text values, the provider returns four (4) numbers and four (4) null values.

In your eight (8) scanned rows all of them less than 255 characters the provider will truncate all data to 255 characters

In your eight (8) scanned rows, if the column contains five (5) values with more length than 255 the provider will return more than 255 characters

### What else can we do?

We can change TypeGuessRows and set it to 0. This works very well for files up to 16384 lines.

The valid range of values for the TypeGuessRows key is 0 to 16. However, if the value is 0, the number of source rows scanned is 16384.\\

For larger files, it may not work again, so the best solution to the problem is not to use excel as a data source but use text files instead. But this may bring another problem if user open CSV after it was exported it may lose leading zeros.

### The only way to make import from Excel work is

- Set IMEX=1 in the connection string
- Close any programs that are running.
- On the Start menu, click Run. Type Regedit and click OK.
- In the Registry Editor, expand the following key depending on the version of Excel that you are running:
- Excel 97 (64bit) \\ HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Jet\3.5\Engines\Excel
- Excel 2000 (64bit) \\ HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Jet\4.0\Engines\Excel
- Excel 2007 (64bit) \\ HKEY_LOCAL_MACHINE\Software\Microsoft\Office\12.0\Access Connectivity Engine\Engines\Excel
- Excel 2010 (64bit) \\ HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Access Connectivity Engine\Engines\Excel
- Excel 2013 (64bit) \\ HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel
- Excel 2016 (64bit) \\ HKEY_LOCAL_MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel
- Excel 97 (32bit) \\ HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Jet\3.5\Engines\Excel
- Excel 2000 (32bit) \\ HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Jet\4.0\Engines\Excel
- Excel 2007 (32bit) \\ HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\Office\12.0\Access Connectivity Engine\Engines\Excel
- Excel 2010 (32bit) \\ HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\Office\14.0\Access Connectivity Engine\Engines\Excel
- Excel 2013 (32bit) \\ HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel
- Excel 2016 (32bit) \\ HKEY_LOCAL_MACHINE\Software\WOW6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel
- Select TypeGuessRows and on the Edit menu click Modify.
- In the Edit DWORD Value dialogue box, click Decimal under Base.
- Set the value to 1
- Open Excel file
- Make sure that the cells in the first line of the table have relevant data for example
- mixed numbers and text characters for text fields
- only numbers for numeric fields
- If some of the data will be longer than 255 characters make sure that the first line cell has more than 255 characters otherwise it will be truncated

{{< alert color="secondary" >}}This solution applies to all versions of MS Excel ODBC driver, Ole DB, MS Jet, .NET, DTS and SSIS{{< /alert >}}

We have spent an enormous amount of time trying to get it fixed. So far we were not able to find a better solution.

The way Excel import works make it not possible to automate it. You have to modify most of excel files manually in order to load them.

This is why we are no longer using ODBC/OleDB/Ms Jet for Excel connections. Our [ETL solutions](https://www.etl-tools.com/products/etl-tools-overview.html) work correctly with Excel all the time. [Try it yourself now](https://www.etl-tools.com/products/etl-tools-overview.html).

{{< image class="mx-auto d-block"  src="/images/knowledgebase/advanced-etl-processor-working-with-excel.png" title="Advanced ETL Processor Working With Excel" >}}

- Works directly with all Excel versions
- No ODBC, OleDB or MS Jet Required
- Works correctly with mixed data types
- Works correctly with cells with more than 255 characters
- No need for IMEX=1, HDR=Yes or Registry hacks (TypeGuessRows)
- Loads data correctly all the time + no need to edit Excel file
- Can create Excel files in Excel 3.0-2016 format
- Can insert data starting from a specific cell
- Can clear area before adding data into Excel
- Can add headers
- Can format data
- Supports Calculations

{{< alert color="success" >}}This is a very old article, but today (2021) it is still relevant{{< /alert >}}

{{< aetl >}}
