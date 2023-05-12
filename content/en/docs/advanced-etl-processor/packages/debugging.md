---
author: Peter Jonson
title: Debugging Package
description: Trouble Shooting and Debugging Advanced ETL Processor Packages
draft: false
tags: ['Package', 'Debugging']
date: 2022-09-17
group: advanced-etl-processor-enterprise-package
menu: advanced-etl-processor-enterprise
layout: docs
weight: 2
---

It is possible to run individual actions within the package or debug entire package. It is also possible to set breakpoints.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-break-point-1.png" title="Break Point" >}}

Breakpoints are highlighted in orange.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-backup-logs-2.png" title="Break Point" >}}

To start debugging click green arrow.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-start-debug-3.png" title="Start Debugging" >}}

Action in blue is being currently executed.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-create-tmp-4.png" title="Debugging Package" >}}

Read arrow continues execution of package after the breakpoint

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-red-arrow-5.png" title="Debugging Package" >}}

Click to show execution log {{< image src="/images/etl/advanced-etl-processor/packages/debugging-package-exe-log-icon-6.png" title="Execution log" >}}

Execution log provides additional information about the package actions

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-exe-log-debugging-7.png" title="Execution log" >}}

More detailed information

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-log-viewer-8.png" title="More detailed information" >}}

Another important point is the current state of variables

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/debugging-package-variables-9.png" title="Package Variables" >}}

{{< aetl >}}
