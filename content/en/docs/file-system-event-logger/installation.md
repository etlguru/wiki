---
author: Mike Rewnick
title: Installation
description: File System Event Logger Installation
draft: false
tags: ['File System Event Logger', 'Installation']
date: 2022-04-04
menu: file-system-event-logger
group: file-system-event-logger
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/file-system-logger/file-system-event-logger-setup.png"  title="File System Event Logger Setup Wizard" >}}

## Linux

Download the software and run the following commands
{{< command >}}
sudo apt install ./file-system-event-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-file-system-event-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-file-system-event-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-file-system-event-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}

If it does not work try changing the port

[Settings]({{<relref "docs/file-system-event-logger/settings" >}})

{{< file-system-event-logger >}}
