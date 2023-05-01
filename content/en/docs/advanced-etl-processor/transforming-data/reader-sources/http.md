---
author: Peter Jonson
title: HTTP Reader
description: HTTP Reader
draft: false
tags: ['Reader', 'HTTP', 'Webhook']
date: 2022-09-17
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

When Data source type is HTTP [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) acts as HTTP server designed to process HTML forms. Both Post and Get methods are supported. It is also possible to upload files.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/http.png" title="Data source is HTTP" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/http-file-post-form.png" title="Data source is HTTP" >}}

## Get Form Example

```html
<form name="input" action="https://localhost:8000/html_form_submit.html" method="get">
  <p>Simple Get Form Example</p>
  Name: <input type="text" name="user" />
  <br />
  <input type="checkbox" name="vehicle" value="Bike" />I have a bike<br />
  <input type="checkbox" name="vehicle" value="Car" />I have a car
  <br />
  <textarea name="area" rows="10" cols="30">
  The cat was playing in the garden.
  </textarea>
  <br />
  <input type="submit" value="Submit" />
</form>
```

## Post Form Example

```html
<form name="input" action="https://localhost:8000/html_form_submit.html" method="post" enctype="multipart/form-data">
  <p>Simple Post Form Example</p>
  Name: <input type="text" name="user" />
  <br />
  <input type="checkbox" name="vehicle" value="Bike" />I have a bike<br />
  <input type="checkbox" name="vehicle" value="Car" />I have a car
  <br />
  <textarea name="area" rows="10" cols="30">
  The cat was playing in the garden.
  </textarea>
  <br />
  <input type="submit" value="Submit" />
</form>
```

## File Upload Example (Post)

```html
<form name="input" action="https://localhost:8000/html_form_action.asp" method="post" enctype="multipart/form-data">
  <p>Simple File Post Form Example</p>
  Name: <input type="text" name="user" />
  <br />
  <input type="checkbox" name="vehicle" value="Bike" />I have a bike<br />
  <input type="checkbox" name="vehicle" value="Car" />I have a car
  <br />
  <textarea name="area" rows="10" cols="30">
  The cat was playing in the garden.
  </textarea>
  <br />
  <input type="file" name="somename" size="chars" />
  <br />
  <input type="submit" value="Submit" />
</form>
```

## Fields List

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/http-fields-list.png" title="Fields List" >}}
