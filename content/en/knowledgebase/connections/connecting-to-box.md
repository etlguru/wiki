---
author: Maria Salter
title: Connecting to Box
description: This Article describes how to get Box cloud storage client id and client secret
draft: false
tags: ['Knowledgebase', 'Connection', 'Box', 'Cloud']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

To use Box cloud storage, you need first to obtain the client id and client secret by completing the following steps using Google Chrome:

**Procedure:**

1. Go to the box developer console.

When prompted, sign in with your account credentials.

https://app.box.com/developers/console

2. Click create a new app.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-1.png" title="Create a new Box app" >}}

3. Select Custom app.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-2.png" title="Select Custom app" >}}

4. Select Standard OAuth 2.0.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-3.png" title="Select Standard OAuth 2.0." >}}

5. Enter the app's name, for example, AETL and click Create application.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-4.png" title="Enter the app's name, for example, AETL and click Create application." >}}

6. Make sure that URI is correct

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-5.png" title="Connecting to box" >}}

6. Use “Client Id” as “key” and “Client Secret” as “secret”

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-6.png" title="Connecting to box" >}}

9. Enter credentials and click authorize

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-7.png" title="Connecting to box" >}}

10. Click Grant access to Box

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-box-8.png" title="Connecting to box" >}}

{{< aetl >}}
