---
author: Maria Salter
title: Connecting to Amazon S3 Storage
description: Connecting to Amazon S3 Storage
draft: false
tags: ['Knowledgebase', 'Connection', 'Amazon', 'S3']
date: 2023-03-14
group: knowledgebase-connections
layout: docs
---

To use Amazon S3 Storage, you need first to obtain the Account Name and Account Key by completing the following steps:

**Procedure:**

1. Go to the AWS Management Console.

When prompted, sign in with your account credentials.

2.  Click on your user name and select My Security Credentials

{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-connection1.png" title="Connecting to Amazon S3 Storage" >}}

3. Expand access keys

{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-connection2.png" title="Connecting to Amazon S3 Storage" >}}

4. Click create a new access key

{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-connection3.png" title="Connecting to Amazon S3 Storage" >}}

5. Download the key file

6. Use AWSAccessKeyId and AWSSecretKey to login

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/connections/cloud/amazon-connection.png" title="AWSAccessKeyId and AWSSecretKey" >}}

7. Create a new S3 basket enter the name and leave the rest of the options as they are

{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-s3-basket.png" title="Amazon S3 Basket" >}}
\
{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-s3-basket-2.png" title="Amazon S3 Basket" >}}

8. Create a new package, add Amazon S3 Action and click connect

{{< image class="mx-auto d-block"  src="/images/knowledgebase/amazon-s3-action.png" title="Amazon S3 Basket" >}}

**Endpoint**

In some situations, it might be necessary to change the endpoint the full list of endpoints can be found here:

https://docs.aws.amazon.com/general/latest/gr/s3.html

{{< aetl >}}
