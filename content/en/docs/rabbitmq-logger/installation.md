---
author: Mike Rewnick
title: Installation
description: RabbitMQ Logger Installation
draft: false
tags: ['RabbitMQ Logger', 'Event Loggers']
date: 2022-05-19
menu: rabbitmq-logger
group: rabbitmq-logger
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/rabbitmq-logger/rabbitmq-logger-setup.png" title="RabbitMQ Logger Event log Setup Wizard" >}}

## Linux

Download the software and run the following commands

{{< command >}}
sudo apt install ./rabbitmq-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-rabbitmq-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-rabbitmq-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-rabbitmq-logger
{{< /command >}}

(Use this command to stop the server)

Once started open the following URL in the browser

http://localhost:3333<

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}
\
If it does not work try changing the port

[Settings]({{<ref "settings" >}})

{{< rabbitmq-logger >}}
