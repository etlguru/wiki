---
author: Maria Salter
title: Working with Repository
description: This Article describes configuring Repository
draft: false
tags: ['Knowledgebase', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 1
---

## Why it is important to know how to work with the repository?

The repository database stores all the information about connections, transformations, packages, SQL scripts, reports and execution logging. This is where the results of ETL designer hard work is stored and obviously, no one wants to lose it.

## Default Repository

The default repository is MS Access. This type of repository works fine for development and for a small production environment. From time to time we recommend performing “compact and repair” using MS Access. For heavy production environments for example, when we want to run packages every minute in parallel we recommend using something else like MS SQL Server or Oracle.

## Provider Not Found Error Message

The user may receive the message above after installing 64 version of our ETL Software. This is because by default 64 bit OLE driver for MS Access is not installed on windows. Although it is possible to install a 64 bit OLE driver for MS Access by using our software we strongly recommend against it. The best course of action is to use a proper database as repositories such as MS SQL Server or Oracle.

## Installing MS Access Runtime

During setup, our software will install Access runtime if selected

{{< image class="mx-auto d-block"  src="/images/knowledgebase/access.png" title="Installing MS Access Runtime" >}}

Installing 64-bit Access runtime on the computer where the 32-bit version of MS Office is already installed will lead to problems working with MS office (Repairing MS Office installation error message).

{{< image class="mx-auto d-block"  src="/images/knowledgebase/working-with-repository-1.png" title="Working with Repository" >}}

{{< alert color="secondary">}}Information about current repository connection can be seen in the window header{{< /alert >}}

## Creating Repository

The repository can be created by running a script or by using the repository creation wizard.\\
They are located in C:\Users\Public\Documents\DBSL\Repository Scripts.

To create a new MS Access repository copy\
C:\Users\Public\Documents\DBSL\Repository Scripts\Repository\Repository.mdb into the different directory and connect to it.

## Default Repository Connections

When software is installed default repository connections are created such as MS Access, Oracle, SQL Server, MySQL, PostgreSQL. When the application first starts it connects to the default MS Access repository.

## Connecting to different Repository

- Click Maintain tab
- Select the desired connection from the drop-down box
- Click reconnect.

Provided that you are using default settings all open objects will be saved and the application will connect to a different repository.

## Creating new Repository

- Click Maintain tab
- Click create new
- Follow the wizard steps
- Once the repository is created connect to it

## Creating new Repository connection

If you want to create a new connection to the existing repository:

- Click Maintain tab
- Click options
- Click plus
- Fill in all necessary details
- Test connection
- Click OK

{{< alert color="secondary">}}Same dialogue can be used to amend exiting repository connections.{{< /alert >}}

## Backing up Repository

- Click Maintain tab
- Click backup
- Select the file to save data into
- Done

## Restoring Repository

- Click Maintain tab
- Click restore
- Select the file to restore data from
- Done

## To copy repository data from development to production environment

- Connect to the development environment
- Backup repository
- Connect to the production environment
- Restore repository

## To copy single project from development to production environment

- Connect to the development environment
- Backup repository
- Connect to the production environment
- Right-click on the object tree and restore the project
- Select the project to restore and click OK

{{< image class="mx-auto d-block"  src="/images/knowledgebase/restore-project1.png" title="Restore Project" >}}

{{< image class="mx-auto d-block"  src="/images/knowledgebase/restore-repositiry-dialogue.png" title="Restore Repository Dialogue" >}}

## Repository objects synchronization

- Run Repository Synchronization Wizard
- Select source repository or repository backup
- Select target repository
- Drug and drop source repository objects on top of target repository objects to update target object
- Drug and drop source repository objects in the target category to add a new object
- Connect to target repository and update connections if necessary

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-1.png" title="Synchronization Wizard" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-2.png" title="Synchronization Wizard" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-3.png" title="Synchronization Wizard" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-4.png" title="Synchronization Wizard" >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/repository-database/syncronisation-wizard-5.png" title="Synchronization Wizard" >}}

## Controlling size of Repository

While executing scheduled tasks the size of the repository is constantly growing. From time to time it might become necessary to clear execution log tables otherwise it might have a negative impact on performance.

- Click the Execution Log tab
- Click the clear log button

{{< image class="mx-auto d-block"  src="/images/knowledgebase/clear-log-2.png" title="Clear Log" >}}

{{< alert color="secondary">}}Information above is relevant to both (Advanced ETL Processor)[https://www.etl-tools.com/advanced-etl-processor/overview.html] and (Visual Importer ETL)[https://www.etl-tools.com/visual-importer-etl-enterprise/overview.html and some of of it to [Active Table Editor](https://www.etl-tools.com/active-table-editor/overview.html) {{< /alert >}}

## Unable to connect to the Repository error

The default repository is MS Access. The 64-bit setup offers the option to install the 64-bit version of access drivers. Without them, the 64-bit version of our software will not be able to work with access or use it as a repository. We do not recommend using MS access as a repository in a production environment. The important thing to understand that the 32-bit version uses 32-bit version drivers and it cannot use 64-bit drivers. The same applies to the 64-bit version. Before installing the 64-bit version you have to make sure that relevant 64-bit drivers, ODBC Drivers, OleDB Providers and Clients are installed.

## Video Tutorials

{{< youtube id="6lRcz7NsU0w" class="ratio ratio-16x9" >}}
\
{{< youtube id="iYFj0d5-Jmw" class="ratio ratio-16x9" >}}
\
{{< youtube id="KgP-TKBsvDc" class="ratio ratio-16x9" >}}
\
{{< youtube id="Kb1rFoh9hng" class="ratio ratio-16x9" >}}

{{< aetl >}}
