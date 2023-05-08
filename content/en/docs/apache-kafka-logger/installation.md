---
author: Mike Rewnick
title: Installation
description: Installation of Apache Kafka Logger
date: 2023-03-07
draft: false
tags: ['Apache Kafka Logger', 'Installation']
menu: apache-kafka-logger
group: apache-kafka-logger
layout: docs
---

## Windows

Run setup and follow the wizard steps

{{< image class="mx-auto d-block"  src="/images/event-loggers/apache-kafka-logger/apache-kafka-logger-setup.png"  title="Apache Kafka Logger Setup wizard" >}}

## Linux

Download the software and run the following commands
{{< command >}}
sudo apt install ./apache-kafka-logger-amd64.deb
{{< /command >}}
(This will install the software)

{{< command >}}
sudo systemctl enable etl-tools-apache-kafka-logger
{{< /command >}}
(This will enable the server)

{{< command >}}
sudo systemctl start etl-tools-apache-kafka-logger
{{< /command >}}
(This will start the server)

{{< command >}}
sudo systemctl stop etl-tools-apache-kafka-logger
{{< /command >}}
(Use this command to stop the server)

Once started open the following URL in the browser

[http://localhost:3333](http://localhost:3333)

The default user name is: welcome@etl-tools.com and the password is Welcome

{{< image class="mx-auto d-block"  src="/images/licensing-server/login.png"  title="Login Screen" >}}

If it does not work try changing the port
\
[Settings]({{<relref "docs/apache-kafka-logger/settings" >}})

{{< apache-kafka-logger >}}
