---
author: Maria Salter
title: Repository Tables
description: This Article provides a list of the repository tables
draft: false
tags: ['Knowledgebase', 'Repository']
date: 2023-03-14
group: knowledgebase-repository
layout: docs
weight: 1
---

## Repository Tables List

Below is a list of tables used by [etl-tools.com](https://www.etl-tools.com/) [products](https://www.etl-tools.com/products/etl-tools-overview.html)

{{< table "table-striped table-bordered" >}}

| Table Name            | Usage                                                                                                                                      | Visual Importer ETL | Advanced ETL Processor | Active Table Editor | Database Browser |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------- | ---------------------- | ------------------- | ---------------- |
| TEMPLATES             | Library of objects                                                                                                                         | X                   | X                      |                     |                  |
| ID-GENERATOR          | PK Generators                                                                                                                              | X                   | X                      | X                   | X                |
| CONNECTIONS           | Connection details                                                                                                                         | X                   | X                      | X                   | X                |
| OBJECT-TYPES          | Object Types Lookup                                                                                                                        | X                   | X                      | X                   | X                |
| OBJECTS               | Holds objects data: SQL, Forms, Transformations Mappings, Packages and Reports                                                             | X                   | X                      | X                   |                  |
| OBJECTS-HISTORY       | Version Control                                                                                                                            | X                   | X                      |                     |                  |
| OBJECTS-TREE          | Objects Tree                                                                                                                               | X                   | X                      |                     |                  |
| QUEUE                 | List of objects being executed right now or waiting to be executed, once execution is completed records are moved into QUEUE-HISTORY table | X                   | X                      |                     |                  |
| QUEUE-ACTIONS         | Current execution details, once execution is completed records are moved into QUEUE-ACTIONS-HISTORY table                                  | X                   | X                      |                     |                  |
| QUEUE-HISTORY         | Object Execution History                                                                                                                   | X                   | X                      |                     |                  |
| QUEUE-ACTIONS-HISTORY | Object Actions Execution History                                                                                                           | X                   | X                      |                     |                  |
| SCHEDULE              | Execution schedule                                                                                                                         | X                   | X                      |                     |                  |
| USERS                 | List of users                                                                                                                              |                     |                        | X                   |                  |
| GROUPS                | List of groups                                                                                                                             |                     |                        | X                   |                  |
| ACCESS-RIGHTS         | Access Rights                                                                                                                              |                     |                        | X                   |                  |
| GROUP-MEMBERS         | List of groups members                                                                                                                     |                     |                        | X                   |                  |
| NODES                 | Holds computer metadata                                                                                                                    | X                   | X                      |                     |                  |
| NODE-STATUS           | Holds information about software installed                                                                                                 | X                   | X                      |                     |                  |
| APPLICATION-SETTINGS  | Application settings                                                                                                                       | X                   | X                      |                     |                  |
| SQL-EXECUTION-HISTORY | History of SQL execution                                                                                                                   | X                   | X                      | X                   | X                |
| MENUS                 | User menus                                                                                                                                 |                     |                        | X                   |                  |

{{< /table >}}

## Repository Schema

{{< image src="/images/knowledgebase/repository-schema-1.png" >}}
\
{{< image src="/images/knowledgebase/repository-schema-2.png" >}}
\
{{< image src="/images/knowledgebase/repository-schema-3.png" >}}

{{< aetl >}}
