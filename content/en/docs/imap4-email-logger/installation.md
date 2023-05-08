---
author: Mike Rewnick
title: Installation
description: IMAP4 EMail Logger Installation
draft: false
tags: ['IMAP4 EMail Logger', 'Installation']
date: 2022-04-06
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

### Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-email-logger-setup.png" title="Setup wizard" >}}

### Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./imap4-email-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-imap4-email-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-imap4-email-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-imap4-email-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png" title="Login" >}}
\
If it does not work try changing the port

[Settings]({{<relref "docs/imap4-email-logger/settings" >}})

{{< imap4-email-logger >}}
