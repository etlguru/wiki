---
author: Peter Jonson
title: Active Directory Reader
description: Active Directory Reader
draft: false
tags: ['Reader', 'Active Directory']
date: 2022-11-14
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

## Data Source is Active Directory

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/active_directory.png" title="Data Source is Active Directory" >}}

When no username/password is provided current user is used

We do recommend using a filter during design to reduce the pressure on the server

## Supported sources

## Users

- DistinguishedName
- ccn
- csn
- instanceType
- objectCategory
- objectClass
- objectSid
- sAMAccountName
- sAMAccountType
- title
- initials
- name
- givenName
- displayName
- distinguisedName
- UserPrincipalName
- description
- mail
- mailNickname
- physicaldeliveryofficename
- telephoneNumber
- facsimileTelephoneNumber
- mobile
- Pager
- company
- department
- useraccountcontrol
- showInAddressBook
- publicDelegates
- scriptPath
- lastLogon
- pwdLastSet
- whenCreated
- whenChanged
- ExtensionAttribute1-15

## Groups

- distinguishedName
- cn
- groupType
- instanceType
- objectCategory
- objectClass
- objectSid
- sAMAccountName
- description
- whenCreated
- whenChanged

## Computers

- distinguishedName
- cn
- instanceType
- objectCategory
- objectClass
- objectSid
- sAMAccountName
- description
- useraccountcontrol
- operatingSystem
- lastLogon
- whenCreated
- whenChanged

## User(s) groups

- Group
- User

## Group(s) members

- Group
- User

(More Information about Active Directory Fields)[http://edocs.mitel.com/UG/Apps-Solutions/MiCollab%207.1/MiCollab%20Client/Admin_WebHelp7.1/uca/common_ad_ldap_field_mappings.htm]

If you are having any problems please contact support and we will do our best to help you
