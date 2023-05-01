---
author: Mike Rewnick
title: Pages
description: Page is the main starting point of a Deep Bin application. Every user has a default page assigned. The page consists of some content and a toolbar.
tags: ['Deep Bin', 'Pages']
date: 2022-05-04
menu: deep-bin
group: deep-bin
layout: docs
---

Page is the main starting point of a Deep Bin application. Every user has a default page assigned. The page consists of some content and a toolbar. The toolbar can be hidden if necessary. The front page is usually centred vertically. One of the major benefits of using Deep bin is that everything is user-definable. The users can change the text, color, font and even embed other objects like cards, tabs, grids or workflows

{{< image class="mx-auto d-block"  src="/images/deep-bin/deep-bin-page-overview.png" title="Page Overview" >}}

## Creating New Page

{{< image class="mx-auto d-block"  src="/images/deep-bin/creating-new-page-1.png" title="Creating New Page" >}}

Note: Code is a unique key, it is used as a part of the link access page

{{< image class="mx-auto d-block"  src="/images/deep-bin/page-code.png" title="Page Code" >}}

## Page Designer

{{< image class="mx-auto d-block"  src="/images/deep-bin/creating-new-page-2.png" title="Page Designer" >}}

{{< image class="mx-auto d-block"  src="/images/deep-bin/creating-new-page-3.png" title="Page Designer" >}}

### Title

Web page title

### Hide toolbar

This option hides the toolbar at the top. Most of the time it is used when page has embedded components. The toolbar provides a convenient way of accessing Deep bin components

[Toolbar Designer]({{<ref "toolbar" >}})

### Center

Centres content of the page horizontally

### Editing Page in RAW JSON Format

Note: The result of page design is stored in JSON format in the database or file system. It is possible to edit JSON directly using RAW editor

{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-raw-1.png" title="Page in RAW JSON Format" >}}
\
{{< image class="mx-auto d-block"  src="/images/deep-bin/edit-raw-2.png" title="Page in RAW JSON Format" >}}

## Page Content Objects

- [Rows]({{<ref "pages/rows" >}})
- [Cards]({{<ref "pages/cards" >}})
- [Tabs]({{<ref "pages/tabs" >}})
- [Html]({{<ref "pages/html" >}})

{{< deep-bin >}}
