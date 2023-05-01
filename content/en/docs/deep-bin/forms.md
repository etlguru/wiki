---
author: Mike Rewnick
title: Form Designer
description: Deep Bin Forms provide a flexible way of editing data. The look and feel are fully customizable. The inputs can be grouped using cards or tabs.
draft: false
tags: ['Deep Bin', 'Input Form Designer']
date: 2022-05-09
menu: deep-bin
group: deep-bin
layout: docs
---

Forms provide a flexible way of editing data. The look and feel are fully customizable. The inputs can be grouped using cards or tabs.

{{< image class="mx-auto d-block"  src="/images/deep-bin/deep-bin-form-overview.png" title="Deep Bin Input Form" >}}

## Creating New Form

{{< image class="mx-auto d-block"  src="/images/deep-bin/creating-new-form-1.png" title="Creating New Form" >}}

Note: Code is a unique key, it is used as a part of the link to access the form

{{< image class="mx-auto d-block"  src="/images/deep-bin/form-code.png" title="Form Code" >}}

## Form Designer

{{< image class="mx-auto d-block"  src="/images/deep-bin/form-designer.png" title="Form Designer" >}}

### Model

Mode is an object representation of a database table. The models are designed to give maximum flexibility to the user. They are able to store almost any data. Every grid is based on a single model

### Title

Web page title

### Url

The URL is used when the user presses the cancel, delete or save buttons

### Hide toolbar

This option hides the toolbar at the top. The toolbar provides a convenient way of accessing Deep bin components

[Toolbar Designer]({{<ref "toolbar" >}})

### Hide save as

Hides save as new button

### Hide delete

Hides delete button

### Read Only

Makes all objects inside the form read-only and hides the save button

### Editing Form in RAW JSON Format

Note: The result of the form design is stored in JSON format in the database or file system. It is possible to edit JSON directly using the RAW editor

{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-form-raw-1.png" title="Editing Form in RAW JSON Format" >}}
\
{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-form-raw-2.png" title="Editing Form in RAW JSON Format" >}}

## Forms Objects

- [Rows]({{<ref "forms/rows" >}})
- [Cards]({{<ref "forms/cards" >}})
- [Tabs]({{<ref "forms/tabs" >}})
- [Text]({{<ref "forms/text" >}})
- [Input]({{<ref "forms/input" >}})
- [Text Area]({{<ref "forms/text-area" >}})
- [Check Box]({{<ref "forms/check-box" >}})
- [Select]({{<ref "forms/select" >}})
- [Editor]({{<ref "forms/editor" >}})
- [Hidden]({{<ref "forms/hidden" >}})
- [Dual List]({{<ref "forms/dual-list" >}})
- [Form Designer]({{<ref "forms/form-designer" >}})
- [Grid Designer]({{<ref "forms/grid-designer" >}})
- [Page Designer]({{<ref "forms/page-designer" >}})
- [Workflow Designer]({{<ref "forms/workflow-designer" >}})

{{< deep-bin >}}
