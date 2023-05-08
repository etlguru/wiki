---
author: Mike Rewnick
title: Installation
description: HL7 Logger Installation
draft: false
tags: ['HL7 Event Logger', 'Installation']
date: 2022-04-17
menu: hl7-logger
group: hl7-logger
layout: docs
---

### Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/hl7-logger/hl7-logger-setup.png" title="HL7 Event Setup Dialogue" >}}

### Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./hl7-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-hl7-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-hl7-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-hl7-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<relref "docs/hl7-logger/settings" >}})

{{< hl7-event-logger >}}
