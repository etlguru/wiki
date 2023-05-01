---
author: Mike Rewnick
title: Troubleshooting
description: Deep Bin Troubleshooting.
draft: false
tags: ['Deep Bin', 'Troubleshooting']
date: 2022-04-21
menu: deep-bin
group: deep-bin
layout: docs
---

## Windows

- Stop ETL-Tools.com Deep Bin (64bit) windows service
- execute C:\Program Files\DB Software Laboratory\Deep Bin\deep_bin.exe

## Linux

{{< command >}}
sudo systemctl stop etl-tools-deep-bin
cd /opt/etl-tools.com/deep-bin
sudo ./deep_bin
{{< /command >}}

Refresh the page\
Check the output

{{< image class="mx-auto d-block"  src="/images/deep-bin/deep-bin-error.png" title="Error" >}}

{{< deep-bin >}}
