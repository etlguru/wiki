---
author: Maria Salter
title: Connecting to Dropbox
description: This Article describes how to get Dropbox OAuth App id and key secret
draft: false
tags: ['Knowledgebase', 'Connection', 'Dropbox', 'Cloud']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

To use Dropbox, you need first to obtain the App key and app secret by completing the following steps using Google Chrome:

**Procedure:**

1. Go to the Dropbox developer Portal.

When prompted, sign in with your account credentials.

https://www.dropbox.com/developers/apps/create

2. Choose Dropbox API.

3. Select Full Dropbox.

4. Enter app's name, for example, AETL and click Create application.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-dropbox-1.png" title="Connecting to Dropbox" >}}

5. Add redirect URI.

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-dropbox-2.png" title="Connecting to Dropbox" >}}

6. Use “App Id” as “key” and “App Secret” as “secret”

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-dropbox-3.png" title="Connecting to Dropbox" >}}

9. Click authorize and enter credentials if necessary

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-dropbox-4.png" title="Connecting to Dropbox" >}}

10. Click Allow

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-dropbox-5.png" title="Connecting to Dropbox" >}}

{{< aetl >}}
