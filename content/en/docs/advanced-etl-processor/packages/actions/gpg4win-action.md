---
author: Peter Jonson
title: GPG4WIN Action
description: GPG4WIN package action is used to encrypt/decrypt files using OpenPGP
draft: false
tags: ['Package', 'Action', 'GPG4WIN', 'Encryption', 'Decryption', 'OpenPGP']
date: 2023-03-18
group: advanced-etl-processor-enterprise-package-actions
menu: advanced-etl-processor-enterprise
layout: docs
---

**GPG4WIN** package action is used to encrypt/decrypt files using OpenPGP.

## About Gpg4win

Gpg4win enables users to securely transport emails and files with the help of encryption and digital signatures. Encryption protects the contents against an unwanted party reading it. Digital signatures make sure that it was not modified and come from a specific sender.

Gpg4win supports both relevant cryptography standards, OpenPGP and S/MIME (X.509), and is the official GnuPG distribution for Windows. It is maintained by the developers of GnuPG. Gpg4win and the software included with Gpg4win are Free Software (Open Source; among other things free of charge for all commercial and non-commercial purposes).

Source: http://www.gpg4win.org

Gpg4Win must be installed before using Gpg4Win action.

## Workflow tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/gpg4win-action-workflow-1.png" title="Workflow tab" >}}

## Advanced tab

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/gpg4win-action-advanced-2.png" title="Advanced tab" >}}

## After execution tab

Specifies which variables will be set once action execution is completed
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/gpg4-variables.png" title="After execution tab" >}}

{{< aetl >}}
