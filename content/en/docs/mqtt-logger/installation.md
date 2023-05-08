---
author: Mike Rewnick
title: Installation
description: MQTT Logger Installation
draft: false
tags: ['MQTT Logger', 'Installation']
date: 2022-04-12
menu: mqtt-logger
group: mqtt-logger
layout: docs
---

### Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/mqtt-logger/mqtt-logger-setup.png" title="MQTT Logger Setup Wizard" >}}

### Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./mqtt-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-mqtt-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-mqtt-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-mqtt-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<relref "docs/mqtt-logger/settings" >}})

{{< mqtt-logger >}}
