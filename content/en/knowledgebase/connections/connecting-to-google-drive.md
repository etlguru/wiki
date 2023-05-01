---
author: Maria Salter
title: Connecting to Google Drive
description: This Article describes how to get Google Drive OAuth client id and client key
draft: false
tags: ['Knowledgebase', 'Connection', 'Google', 'Google Drive']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

**Procedure:**

1. Go to the Google API Console and select an existing project or create a new one. In this example, we create a new project called "ETLProject".

https://console.developers.google.com

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-1.png" title="Connecting to Google Drive" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-2.png" title="Connecting to Google Drive" >}}

2. Once the project is created click on the library and select google drive API

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-3.png" title="Connecting to Google Drive" >}}

3. Click Enable

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-4.png" title="Connecting to Google Drive" >}}

4. Click credentials and click create a credential

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-5.png" title="Connecting to Google Drive" >}}

5. Enter a name

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-6.png" title="Connecting to Google Drive" >}}

6. Select google drive API and another UI. click "What credentials do I need?"

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-7.png" title="Connecting to Google Drive" >}}

7. Select an email address and click continue

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-8.png" title="Connecting to Google Drive" >}}

8. Click Done

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-9.png" title="Connecting to Google Drive" >}}

9. Click edit credentials

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-10.png" title="Connecting to Google Drive" >}}

10. Click edit credentials

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-11.png" title="Connecting to Google Drive" >}}

11. Use "client id" as "key" and "client secret" as "secret"

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/cloud/cloud-storage-connection.png" title="Connecting to Google Drive" >}}

13. Click authorize and select the account

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-12.png" title="Connecting to Google Drive" >}}

14. Click Allow

{{< image class="mx-auto d-block"  src="/images/knowledgebase/connecting-to-google-drive-13.png" title="Connecting to Google Drive" >}}

{{< aetl >}}
