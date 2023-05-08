---
author: Mike Rewnick
title: Installation
description: Office365 Email Installation
draft: false
tags: ['Office365 Email Logger', 'Installation']
date: 2022-04-10
menu: office365-email-logger
group: office365-email-logger
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/office365-email-logger/office365-email-logger-setup.png" title="Setup Wizard" >}}

## Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./office365-email-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-office365-email-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-office365-email-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-office365-email-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<relref "docs/office365-email-logger/settings" >}})

{{< office365-email-logger >}}
