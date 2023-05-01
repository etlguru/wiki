---
author: Peter Jonson
title: HTTP Form Action
description: HTTP Form package action is used to post data using HTTP. Files can be posted as well
draft: false
tags: ['Package', 'Action', 'HTTP', 'Form', 'Post']
date: 2023-03-18

group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

**HTTP Form** package action is used to post data using HTTP. Files can be posted as well

```
<form name="input" action="http://localhost:8000/html-form-submit.html" method="post" enctype="multipart/form-data">
<p>Simple Post Form Example</p>
Name: <input type="text" name="user">
<br>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car
<br>
<textarea name="area" rows="10" cols="30">
The cat was playing in the garden.
</textarea>
<br>
<input type="submit" value="Submit">
</form>
```

{{< alert color="secondary">}}The form above is just for information and it is not required for this action.\
The action below will submit exactly the same information using the URL provided{{< /alert >}}

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/http-form-action-workflow-1.png" title="Workflow tab" >}}

## HTTP Form items tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/http-form-action-advanced-2.png" title="HTTP Form items tab" >}}

## HTTP Form headers tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/http-form-action-workflow-11.png" title="HTTP Form headers tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/http-form-action-variables.png" title="After execution tab" >}}

{{< aetl >}}
