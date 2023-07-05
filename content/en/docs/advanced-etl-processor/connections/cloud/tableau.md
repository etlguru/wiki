---
author: Peter Jonson
title: Tableau Connection
description: Tableau Connection
draft: false
tags: ['Connection', 'Cloud', 'Tableau']
date: 2023-07-04
group: 'advanced-etl-processor-enterprise-cloud-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

## About Tableau

Tableau is a powerful and popular data visualization software that enables individuals and organizations to analyze, visualize, and share data in a user-friendly and interactive manner. It provides a range of tools and features that help users explore data, create insightful visualizations, and generate meaningful reports and dashboards.

## Connection

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/cloud/tableau-connection.png" title="Tableau Connection" >}}

## Comments

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/cloud/tableau-connection-comments.png" title="Tableau Comments" >}}

## User fields

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/cloud/tableau-connection-user-fields.png" title="Tableau User Fields" >}}
\
{{< alert color="secondary" >}}
**Note:** User fields provide a convenient way of storing additional data
{{< /alert >}}

**contentUrl**

To determine the value to use for the contentUrl attribute, sign in to Tableau Server or Tableau Online and examine the value that appears after /site/ in the URL. For example, in the following URLs, the content URL is MarketingTeam:

(Tableau Server) http://MyServer/#/site/MarketingTeam/projects

(Tableau Online) https://online.tableau.com/#/site/MarketingTeam/workbooks

Leave it blank to connect to the default site of Tableau Server

{{< aetl >}}
