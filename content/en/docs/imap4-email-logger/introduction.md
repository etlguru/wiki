---
author: Mike Rewnick
title: Introduction
description: IMAP4 Email Logger processes email messages using the scheduler. Basic information about the message is saved into the repository database, msg files and attachments are saved on the disk
draft: false
tags: ['IMAP4 EMail Logger', 'Introduction']
date: 2022-04-17
menu: imap4-email-logger
group: imap4-email-logger
layout: docs
---

IMAP4 Email Logger processes email messages using the scheduler. Basic information about the message is saved into the repository database, msg files and attachments are saved on the disk

## About IMAP4 Protocol

In computing, the Internet Message Access Protocol (IMAP) is an Internet standard protocol used by email clients to retrieve email messages from a mail server over a TCP/IP connection. IMAP is defined by RFC 9051.

IMAP was designed with the goal of permitting complete management of an email box by multiple email clients, therefore clients generally leave messages on the server until the user explicitly deletes them. An IMAP server typically listens on port number 143. IMAP over SSL/TLS (IMAPS) is assigned the port number 993

Virtually all modern e-mail clients and servers support IMAP, which along with the earlier POP3 (Post Office Protocol) are the two most prevalent standard protocols for email retrieval. Many webmail service providers such as Gmail and Outlook.com also provide support for both IMAP and POP3.

Source: [Wikipedia](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol)

## Usage Example

{{< image class="mx-auto d-block"  src="/images/event-loggers/imap4-email-logger/imap4-email-logger-data-flow.png" title="Usage Example" >}}
\
{{< alert color="secondary" >}}
IMAP4 Email Logger works on both Windows and Linux. Please contact us if you want to run IMAP4 Email Logger on a different OS. We will create a special build for you.
{{< /alert >}}

{{< imap4-email-logger >}}
