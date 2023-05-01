---
author: Peter Jonson
title: Compare Files Action
description: This Compare files object performs a validation check against two sets of files by comparing their properties
draft: false
tags: ['Package', 'Action', 'Check', 'File']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

This Compare files object performs a validation check against two sets of files by comparing their properties, via a “check sum”. The comparison can be done via the creation date as the comparison factor, or it can check to ensure that the MD5 checksums match. The files are successfully compared when the comparisons of both files are the same.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/compare-files-action.png" title="Workflow tab" >}}

## Advanced tab

The files to be compared are specified in the dialogue boxes as shown:

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/compare-files-action-advanced.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/compare-files-action-variables.png" title="After execution tab" >}}

{{< aetl >}}
