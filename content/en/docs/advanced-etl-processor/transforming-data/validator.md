---
author: Peter Jonson
title: Working with Validator
description: Data Validator guarantees to your application database that every data value is correct and accurate.
draft: false
tags: ['Transformation', 'Validator']
date: 2023-05-30
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

[Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) Data Validator guarantees to your application database that every data value is correct and accurate. It checks the data against a set of user-defined rules and constraints and identifies any errors or inconsistencies that may be present. This helps organizations avoid problems such as incorrect data being loaded into their systems, or data being lost or corrupted during the ETL process

## Validation Types

There are several types of data validation.

- Data type validation
- Range checking
- Code checking
- Complex validation
- Pattern checking

One of the simplest forms of data validation is verifying the data type. Data type validation answers such simple questions as "Is the string alphabetic?" and "Is the number valid?"

As an extension of simple type validation, range checking ensures that the provided value is within allowable minimums and maximums. For example, a character data type service code may only allow the alphabetic letters A through Z. All other characters would not be valid.

Code checking is a bit more complicated, typically requiring a lookup table. For example, maybe your application calculates sales tax for only certain state codes. You would need to create a lookup object to hold the authorized, taxable state codes.

Pattern checking when you checking the structure of the data field for example social security number format or car registration number. Regular expressions used quite often for pattern checks.

It does not matter which business you are in sooner or later you will discover that there is something wrong with the data and it has to be validated. Here when [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) Validation can help.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator.png" title="Validator Processed Records" >}}

**Note:**

- Records can also be rejected by the Server.
- If there are several validation rules and one of them rejects the record and another discards it, the record will be discarded

## Validator Screen

To change Validator properties double click on it

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-properties.png" title="Validator properties" >}}
\
**Tip:**

If no data is present in the grid check the previous step execution log.

**About input and output fields:**

- List of Output fields is always the same as Inputs.
- List of Input fields is taken from the previous object

## Validator Toolbar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-toolbar-1.png" title="Validator Toolbar" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-toolbar-2.png" title="Validator Toolbar" >}}

1. Properties
1. Create new tab
1. Cut
1. Copy
1. Paste
1. Delete
1. Redo
1. Undo
1. Align Left
1. Arrange Vertically
1. Align Right
1. Align Bottom
1. Arrange Horizontally
1. Align Top
1. Space Horizontally
1. Space Vertically
1. Snap to grid/show grid
1. Prints Mapping
1. Print Preview Mapping
1. Automap data
1. Delete All objects
1. Delete All Links
1. Search Objects
1. Process Data
1. First Record
1. Previous Record
1. Next Record
1. Last Record
1. Show Objects Panel
1. Zoom In
1. Zoom Out
1. Zoom back to 100%

**Note:**

We recommend giving the Validator name, it makes it easier to identify problems later.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-name.png" title="Validator name" >}}

### Debugging Validation

To start debugging validation press the Process Data button {{< image src="/images/etl/advanced-etl-processor/transforming-data/debugging-icon.png" title="Debugging Validation" >}}. To test data edit it in the Data grid.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-debugger.png" title="Debugging Validation" >}}
\
To Change Validation Rule properties double click on it (or right click and select properties)

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-validation-rule-properties.png" title="Validation Rule Properties" >}}

**Note:**

Use \<value> to include actual value into default value

To add a new Validation rule drag and drop it from the Validation rules panel

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-add-validation-rule.png" title="Adding new Validation rule" >}}

It is also possible to apply several validation rules to the Input field by joining them

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/debugging-input-field.png" title="Debugging Input Field" >}}
\
{{< alert color="secondary">}}Data is considered validated when all validation rules are succeeded.{{< /alert >}}

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/validator-data-flow.png" title="Debugging Validated Data" >}}
\
{{< alert color="secondary">}}If you have several validation rules and one of them rejects the record and another discards it, the record will be discarded{{< /alert >}}

## Validation Rules

- [Validating Strings]({{<relref "docs/advanced-etl-processor/validation-rules/strings" >}})
- [Validating Numbers]({{<relref "docs/advanced-etl-processor/validation-rules/numbers" >}})
- [Validating Dates]({{<relref "docs/advanced-etl-processor/validation-rules/dates" >}})
- [Validating Times]({{<relref "docs/advanced-etl-processor/validation-rules/times" >}})
- [Miscellaneous Validations]({{<relref "docs/advanced-etl-processor/validation-rules/miscellaneous" >}})
- [Validating Data using Regular Expressions]({{<relref "docs/advanced-etl-processor/validation-rules/regular-expressions" >}})

## Video Tutorial

{{< youtube id="Hh-SZ_RQW0k" class="ratio ratio-16x9" >}}

{{< aetl >}}
