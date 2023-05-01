---
author: Maria Salter
title: Switching from 32bit to 64bit version
description: This article describes how to switch from 32 bit to 64 bit version of ETL Software
draft: false
tags: ['Knowledgebase', '32bit', '64bit']
date: 2022-09-17
group: knowledgebase-tips
layout: docs
---

The terms 32-bit and 64-bit refer to the way a computer's processor (also called a CPU), handles information. The 64-bit version handles large amounts of random access memory (RAM) more effectively than a 32-bit version.

## What steps shall I do in order to prepare for 64 bit version installation

The important thing to understand that the 32-bit version uses 32-bit version drivers and it cannot use 64-bit drivers. Same apply for the 64-bit version.
Before installing the 64-bit version you have to make sure that relevant 64-bit drivers, ODBC Drivers, OleDB Providers and Clients are installed.

For example to make sure that 64-bit version works with Oracle Database you would need to install the 64-bit version of Oracle Client

## How about performance?

During our tests, the performance of 64-bit version was very similar to 32 bit.

## When would you recommend to switch to 64 bit version?

If you are:

- Using a lot of memory
- Sorting large amounts of data
- Creating and reading very large QVD files.
- Working with large Lookup transformations

## Which version would you recommend for beginners.

Use the 32-bit version, It is easier to install and configure

{{< aetl >}}
