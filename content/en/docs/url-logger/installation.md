---
author: Mike Rewnick
title: Installation
description: URL Logger Installation
draft: false
tags: ['URL Logger', 'Event Loggers']
date: 2022-04-21
menu: url-logger
group: url-logger
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/url-logger/url-logger-setup.png" title="Setup wizard" >}}

## Linux

Download the software and run the following commands
{{< command >}}
sudo apt install ./url-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-url-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-url-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-url-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

http://localhost:3333

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<relref "/docs/url-logger/settings" >}})

{{< url-logger >}}
