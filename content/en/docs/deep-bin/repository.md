---
author: Mike Rewnick
title: Repository
description: Deep Bin Repository Tables
draft: false
tags: ['Deep Bin', 'Repository']
date: 2022-05-12
menu: deep-bin
group: deep-bin
layout: docs
---

The default repository type is SQLite, it works very well with a small amount of data. For high-load systems, we recommend using different database type

## Supported Repository Database Types

- SQLite
- Postgres
- MySQL
- MariaDB
- Microsoft SQL Server
- Oracle

## Changing Repository Type

- Set ENABLE_SECURITY=0
- Set RUN_SQL_SCRIPTS=1
- Set Set CONNECTION_TYPE, DB_USER, DB_PASS, DB_NAME, DB_HOST, DB_PORT, DB_INSTANCE to appropriate values
- Restart Deep Bin
- Recreate/Enable Groups
- Recreate/Enable Users
- Set ENABLE_SECURITY=1
- Restart Deep Bin

## Repository Tables

The tables can be grouped into two categories Metadata tables and User data tables

The Meta tables hold definitions of deep bin objects and information about users.

User data tables are used to store the data created by the users.

**Extra fields**

Most of the tables have fields which are not being used by default, for example users table has date_field_01..date_field_20, char_field_01..char_field_20, boolean_field_01..boolean_field_20, numeric_field_01..numeric_field_20 fields. They can be used to store additional data.
One of the benefits of using Deep Bin is that it allows for overwriting default forms for example the user may decide to create a custom registration form and include additional fields into it.

### user

Metadata table which holds the list of Users

{{< table "table-striped table-bordered" >}}

| Field Name                         | Type          | PK    | Nullable |
| ---------------------------------- | ------------- | ----- | -------- |
| id                                 | Number        | True  | False    |
| email                              | Varchar       | False | False    |
| password                           | Varchar       | False | True     |
| title                              | Varchar       | False | True     |
| first_name                         | Varchar       | False | True     |
| last_name                          | Varchar       | False | True     |
| work_phone                         | Varchar       | False | True     |
| mobile_phone                       | Varchar       | False | True     |
| last_logged_in                     | Date          | False | True     |
| failed_login_attempts              | Number        | False | False    |
| front_page                         | Varchar       | False | False    |
| locked                             | Boolean       | False | True     |
| enabled                            | Boolean       | False | True     |
| code                               | Varchar       | False | False    |
| name                               | Varchar       | False | True     |
| description                        | Varchar       | False | True     |
| category                           | Varchar       | False | True     |
| date_field_01..date_field_20       | Date          | False | True     |
| char_field_01..char_field_20       | Varchar       | False | True     |
| boolean_field_01..boolean_field_20 | Boolean       | False | True     |
| numeric_field_01..numeric_field_20 | Decimal(18,4) | False | True     |
| notes                              | Text          | False | True     |
| created_at                         | Date          | False | True     |
| created_by                         | Varchar       | False | False    |
| updated_at                         | Date          | False | True     |
| updated_by                         | Varchar       | False | False    |

{{< /table >}}

### group

Metadata table which holds the list of Groups

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### group_members

Metadata table which holds the link between Groups and Users

{{< table "table-striped table-bordered" >}}

| Field Name | Type   | PK   | Nullable |
| ---------- | ------ | ---- | -------- |
| group_id   | Number | True | False    |
| user_id    | Number | True | False    |

{{< /table >}}

### login_log

Metadata table which holds the list of failed login attempts

{{< table "table-striped table-bordered" >}}

| Field Name | Type    | PK    | Nullable |
| ---------- | ------- | ----- | -------- |
| id         | Number  | True  | False    |
| email      | Varchar | False | True     |
| status     | Varchar | False | True     |
| ip         | Varchar | False | True     |
| logged_in  | Date    | False | True     |

{{< /table >}}

### form

Metadata table which holds the forms' definitions

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| model       | Varchar | False | True     |
| definition  | Text    | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### grid

Metadata table which holds the grids' definitions

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| definition  | Text    | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### workflow

Metadata table which holds the workflows' definitions

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| definition  | Text    | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### page

Metadata table which holds the pages' definitions

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| definition  | Text    | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### select

Metadata table which holds the selects' definitions

{{< table "table-striped table-bordered" >}}

| Field Name    | Type    | PK    | Nullable |
| ------------- | ------- | ----- | -------- |
| id            | Number  | True  | False    |
| locked        | Boolean | False | True     |
| enabled       | Boolean | False | True     |
| code          | Varchar | False | False    |
| name          | Varchar | False | True     |
| description   | Varchar | False | True     |
| category      | Varchar | False | True     |
| use_default   | Boolean | False | True     |
| default_key   | Varchar | False | True     |
| default_value | Varchar | False | True     |
| sql           | Text    | False | False    |
| notes         | Text    | False | True     |
| created_at    | Date    | False | True     |
| created_by    | Varchar | False | False    |
| updated_at    | Date    | False | True     |
| updated_by    | Varchar | False | False    |

{{< /table >}}

### data

User data table, linked to data_values table

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### data_value

User data table usually used to store data values

{{< table "table-striped table-bordered" >}}

| Field Name                         | Type          | PK    | Nullable |
| ---------------------------------- | ------------- | ----- | -------- |
| id                                 | Number        | True  | False    |
| data_id                            | Number        | False | False    |
| locked                             | Boolean       | False | True     |
| enabled                            | Boolean       | False | True     |
| code                               | Varchar       | False | False    |
| name                               | Varchar       | False | True     |
| description                        | Varchar       | False | True     |
| category                           | Varchar       | False | True     |
| date_field_01..date_field_20       | Date          | False | True     |
| char_field_01..char_field_20       | Varchar       | False | True     |
| boolean_field_01..boolean_field_20 | Boolean       | False | True     |
| numeric_field_01..numeric_field_20 | Decimal(18,4) | False | True     |
| notes                              | Text          | False | True     |
| created_at                         | Date          | False | True     |
| created_by                         | Varchar       | False | False    |
| updated_at                         | Date          | False | True     |
| updated_by                         | Varchar       | False | False    |

{{< /table >}}

### lookup

User data table, linked to lookup_values table

{{< table "table-striped table-bordered" >}}

| Field Name  | Type    | PK    | Nullable |
| ----------- | ------- | ----- | -------- |
| id          | Number  | True  | False    |
| locked      | Boolean | False | True     |
| enabled     | Boolean | False | True     |
| code        | Varchar | False | False    |
| name        | Varchar | False | True     |
| description | Varchar | False | True     |
| category    | Varchar | False | True     |
| notes       | Text    | False | True     |
| created_at  | Date    | False | True     |
| created_by  | Varchar | False | False    |
| updated_at  | Date    | False | True     |
| updated_by  | Varchar | False | False    |

{{< /table >}}

### lookup_value

User data table usually used to store lookup values

{{< table "table-striped table-bordered" >}}

| Field Name                         | Type          | PK    | Nullable |
| ---------------------------------- | ------------- | ----- | -------- |
| id                                 | Number        | True  | False    |
| lookup_id                          | Number        | False | False    |
| locked                             | Boolean       | False | True     |
| enabled                            | Boolean       | False | True     |
| code                               | Varchar       | False | False    |
| name                               | Varchar       | False | True     |
| description                        | Varchar       | False | True     |
| category                           | Varchar       | False | True     |
| date_field_01..date_field_20       | Date          | False | True     |
| char_field_01..char_field_20       | Varchar       | False | True     |
| boolean_field_01..boolean_field_20 | Boolean       | False | True     |
| numeric_field_01..numeric_field_20 | Decimal(18,4) | False | True     |
| notes                              | Text          | False | True     |
| created_at                         | Date          | False | True     |
| created_by                         | Varchar       | False | False    |
| updated_at                         | Date          | False | True     |
| updated_by                         | Varchar       | False | False    |

{{< /table >}}

### meta_data

A basic User data table

{{< table "table-striped table-bordered" >}}

| Field Name                         | Type          | PK    | Nullable |
| ---------------------------------- | ------------- | ----- | -------- |
| id                                 | Number        | True  | False    |
| object_id                          | Number        | False | False    |
| meta_id                            | Number        | False | False    |
| locked                             | Boolean       | False | True     |
| enabled                            | Boolean       | False | True     |
| code                               | Varchar       | False | False    |
| name                               | Varchar       | False | True     |
| description                        | Varchar       | False | True     |
| category                           | Varchar       | False | True     |
| date_field_01..date_field_20       | Date          | False | True     |
| char_field_01..char_field_20       | Varchar       | False | True     |
| boolean_field_01..boolean_field_20 | Boolean       | False | True     |
| numeric_field_01..numeric_field_20 | Decimal(18,4) | False | True     |
| password                           | Varchar       | False | True     |
| notes                              | Text          | False | True     |
| created_at                         | Date          | False | True     |
| created_by                         | Varchar       | False | False    |
| updated_at                         | Date          | False | True     |
| updated_by                         | Varchar       | False | False    |

{{< /table >}}

{{< deep-bin >}}
