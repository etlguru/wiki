---
author: Peter Jonson
title: Tableau Connection
description: Tableau Connection
draft: false
tags: ['Connection', 'Cloud', 'Tableau']
date: 2022-09-17
group: 'advanced-etl-processor-enterprise-cloud-connections'
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block" src="/images/etl/advanced-etl-processor/connections/cloud/tableau-connection.png" title="Tableau Connection" >}}

**contentUrl**

To determine the value to use for the contentUrl attribute, sign in to Tableau Server or Tableau Online and examine the value that appears after /site/ in the URL. For example, in the following URLs, the content URL is MarketingTeam:

(Tableau Server) http://MyServer/#/site/MarketingTeam/projects

(Tableau Online) https://online.tableau.com/#/site/MarketingTeam/workbooks

Leave it blank to connect to the default site of Tableau Server

{{< aetl >}}
