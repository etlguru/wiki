---
author: Mike Rewnick
title: Grids
description: Deep Bin Grids provide a flexible way of presenting the data. The list of fields is fully customizable. The users can easily add new fields, rename existing ones, change sorting order and apply filters. It is also possible to page data, show first N records or show all data.
draft: false
tags: ['Deep Bin', 'Grid Designer']
date: 2022-05-04
menu: deep-bin
group: deep-bin
layout: docs
---

Grids provide a flexible way of presenting the data. The list of fields is fully customisable. The users can easily add new fields, rename existing ones, change sorting order and apply filters. It is also possible to page data, show first N records or show all data.

{{< image class="mx-auto d-block"  src="/images/deep-bin/deep-bin-grid-overview.png" title="Deep Bin Grid Overview" >}}

## Creating New Grid

{{< image class="mx-auto d-block"  src="/images/deep-bin/creating-new-grid-1.png" title="Creating New Grid" >}}

Note: Code is a unique key, it is used as a part of the link to access the grid

{{< image class="mx-auto d-block"  src="/images/deep-bin/grid-code.png" title="Grid Code" >}}

## Grid Designer

{{< image class="mx-auto d-block"  src="/images/deep-bin/grid-designer.png" title="Grid Designer" >}}

### Model

Mode is an object representation of a database table. The models are designed to give maximum flexibility to the user. They are able to store almost any data. Every grid is based on a single model

### Title

Web page title

### What to show

Possible options are:

- All Records
- First N Records
- All Records with paging

Note: Search only works for currently selected page

### Hide toolbar

The toolbar provides a convenient way of accessing Deep bin components

[Toolbar Designer]({{<ref "toolbar" >}})

### Hide search

Hide search box at the top of the screen

### Hide clear

This option allows the user to delete all data from the grid

### Grid Fields

{{< image class="mx-auto d-block"  src="/images/deep-bin/grid-colums.png" title="Grid Fields" >}}

Name of the model field\

Data model field label

Use drug and drop to rearrange fields

### Row actions

Row actions are usually linked to the data entry forms. It is possible to have multiple actions. The first action is used as the default action.

{{< image class="mx-auto d-block"  src="/images/deep-bin/row-actions.png" title="Grid Row Actions" >}}

:id is used to pass the record id to the data entry form.

### Data filters

{{< image class="mx-auto d-block"  src="/images/deep-bin/data-filters.png" title="Data Filters" >}}

When multiple filters are defined they are "anded".

### Data sorts

{{< image class="mx-auto d-block"  src="/images/deep-bin/data-sorts.png" title="Data Sorts" >}}

The sorts are applied in order of definition

## Editing Grid in RAW JSON Format

Note: The result of grid design is stored in JSON format in the database or file system. It is possible to edit JSON directly using RAW editor

{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-grid-raw-1.png" title="RAW JSON Editor" >}}
\
{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-grid-raw-2.png" title="RAW JSON Editor" >}}

{{< deep-bin >}}
