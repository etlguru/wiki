---
author: Maria Salter
title: Data Quality
description: What is data quality and why it is important
draft: false
tags: ['Knowledgebase', 'Data Quality', 'Validator']
date: 2023-03-14
group: knowledgebase-tips
layout: docs
---

## About Data Quality and why it is important?

It is a measure of how well business data practices satisfy standards. Good and reliable data can be used to increase efficiency, support decision making, and skyrocket profitability.

## Importantnce of Data Quality

Poor data quality leads to wasting time, working with conflicting information resulting in bad decisions and a massive decrease in efficiency.

Many organizations implement strict data controls at the point of entry. However quite often it is not enough. For example, when data is loaded into the data warehouse or moved from one application to another additional validation and transformation rules must be applied.

## Data Quality Strategy

The primary objective of any data integration solution is to assemble data from one or more data sources validate and transform it into a standard format.

There are three major steps in implementing data quality strategy:

- **Profiling** - helps you to check if a source data file or table extract meets the format such as file encoding fields format and order
- **Cleansing** - Once data successfully satisfies profiling standards, it still necessary to cleanse the data, for example, remove empty values or irrelevant information
- **Auditing** - one of the most important parts of data integration. It gives IT departments the history of data transformation, profiling and cleansing which can be used in importer failure investigations.

## Advanced ETL Processor Data validator

[Advanced ETL Processor](https://www.etl-tools.com/etl-tools/advanced-etl-processor-professional/overview.html) is able to check any data including date formats, postcodes, phone numbers, validating against a list of values etc. It has more than 190 data validation functions, plus it can be extended by using regular expressions. It is an enterprise data integration solution that lets you quickly validate and process large volumes of data while preserving and enhancing data quality.

### Validation Editor

{{< image class="mx-auto d-block"  src="/images/knowledgebase/validation_editor_1.gif" title="Validation Editor" >}}

### Data cleansing rule

{{< image class="mx-auto d-block"  src="/images/knowledgebase/simple_data_validation_rule_2.gif" title="Simple data cleansing rule" >}}

[Working with Validator]({{<relref "docs/advanced-etl-processor/transforming-data/validator" >}})

{{< aetl >}}