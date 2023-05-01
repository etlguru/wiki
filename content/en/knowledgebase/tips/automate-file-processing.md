---
author: Maria Salter
title: Automate File Processing
description: Learn how to automate text file transformation
draft: false
tags: ['Knowledgebase', 'Text', 'Automation', 'File']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## A Question from the Customer

- An external PLC generates txt files and those must be downloaded and converted into an SQL DB.
- The PLC generates 4 files each day, at a size of 5MB pr. File = 20MB a day.
- The file name is date and time named like this: 14022719.txt, the syntax is YYMMDDHH
- The files are generated at the same 4 hours each day, 01, 07, 13, 19
- In the files, the first data row is a time stamp YYMMDDHHMMSS
- It is important that one record with a specific date/time is written only once in the SQL.
- The files would always be the same size.

## ETL Job

Each day, The ETL converter should copy the file to a local directory via FTP; convert the file to SQL, then delete the file from the local dir. It could be 4 times a day, maybe one hour after the txt file is completed on the PLC.\
We can not delete the file from the PLC, since others should also have access to the data.\
The data on the PLC will be deleted after 10 days using FIFO

## The Problem

How do I keep track of which files I have copied ?\
Could create a TXT file on the local drive and write the file names, compare with what's on the FTP drive ?\
But how do we do this? That is file comparison..can ETL do this ?\
Is there any other way to do this ?\
Keep in mind, it could be that the internet connection is offline for a day or 2, the server could be down,
The PLC could be down. In some situations you will need to copy 4 files, sometimes 6 files..depends..
Or you could have gaps in the timestamps of the file names from the PLC if it has been down for a while.
I know we would then also have gaps in the SQL, but that is OK.

## The Solution

**There are several ways of performing this task**

First of all, you need to speak with the company which provides the files.
It takes time to upload files and you need to make sure that you are not downloading files while they are being uploaded.
For example, you can ask them to put additional files once the process is completed.
If the file is there the process completed and you can download the files.

The next step is to load data into the database. That is easy, there are several tutorials about it.

**Avoiding loading the same data twice.**

First of all, we need to get the source file name, this can be done by using a metadata transformation object

{{< image class="mx-auto d-block"  src="/images/knowledgebase/metadata-transformation.png" title="Metadata" >}}

Then we need to check if the file was loaded before, we can use Validator "In List object" for that

{{< image class="mx-auto d-block"  src="/images/knowledgebase/inlist-2.png" title="In List object" >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/inlist-2-1-3.png" title="In List object" >}}

and the last step to load the data into the table and load the list of processed files into a separate table

{{< image class="mx-auto d-block"  src="/images/knowledgebase/writers.png" title="Data Writer" >}}

**Overall logic as follows**

- Download data from the FTP server using mask into the local folder
- Run transformation from the folder using mask at same time populating a list of processed files and checking if the file was not processed before
- Copy processed files into a separate folder

{{< image class="mx-auto d-block"  src="/images/knowledgebase/file-processing.png" title="File Processing" >}}

{{< aetl >}}
