---
author: Mike Rewnick
title: Installation
description: Licensing Server Software Installation
draft: false
tags: ['Licensing Server']
date: 2022-04-03
menu: licensing-server
group: licensing-server
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/licensing-server/licensing-server-setup.png" title="Licensing Server Setup Wizard" >}}

## Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./licensing-server.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-licensing-server
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-licensing-server
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-licensing-server
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<relref "settings" >}})

{{< ls >}}
