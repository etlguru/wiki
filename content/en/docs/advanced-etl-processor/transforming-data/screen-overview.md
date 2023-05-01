---
author: Peter Jonson
title: Mapping Screen Overview
description: Transformation Screen Overview
draft: false
tags: ['Transformation', 'Mapping']
date: 2022-08-01
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

The transformation screen is used to create and modify data transformation processes.

The default transformation consists of a reader, validator, transformer and writer.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/mapping-screen-overview.png" title="Screen Overview" >}}

## Main tool bar

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformation-main-toolbar-1.png" title="Main Tool bar" >}}
\
{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformation-main-toolbar-2.png" title="Main Tool bar" >}}

1. Transformation Properties
2. Notes
3. New Transformation
4. Load Transformation From the file
5. Saves Transformation to the file
6. Saves Transformation under the new name
7. Saves Transformation to the Repository
8. Cut
9. Copy
10. Paste
11. Delete
12. Undo
13. Redo
14. Align Left
15. Arrange Vertically
16. Align Right
17. Align Bottom
18. Arrange Horizontally
19. Align Top
20. Space Horizontally
21. Space Vertically
22. Snap to grid/show grid
23. Prints Transformation
24. Print Preview Transformation
25. Search Objects
26. Manage Versions
27. Add Version
28. Revert to the previous version
29. Make Transformation Read Only
30. Process Data
31. Schedule for Execution
32. View Execution Log (When executed within the package or by agent/scheduler)
33. Zoom In
34. Zoom Out
35. Zoom 100%

## Transformation properties dialogue

- Default Date format applies to all templates.
- It is used for new Date related validation and transformation functions such as Is Date, Is Date between ETC

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformation-properties-object-id.png" title="Transformation Properties" >}}
\
{{< alert color="secondary">}}Object ID is used to [execute transformation from command line]({{<relref "docs/advanced-etl-processor/automation/command-line-interface" >}}){{< /alert >}}

## Template tab

The template shows the actual transformation script source.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/template-tab.png" title="Template Tab" >}}
\
{{< alert color="secondary">}}By default template tab is hidden, it can be enabled by using [options dialogue]({{<relref "docs/advanced-etl-processor/options-list/hide-template-tab" >}}){{< /alert >}}

## Execution log tab

The execution log provides information about the [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html) and the actions it took during its operations. This is useful when you wish to analyze the activities of individual processes during their execution.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/execution-log-tab.png" title="Execution Log Tab" >}}
\
{{< alert color="secondary">}}Logging takes time, it can be disabled using [options dialogue]({{<relref "docs/advanced-etl-processor/options-list/write-log" >}}){{< /alert >}}

## Rejected records tab

Occasionally, records will be rejected by the processor. This may be due to things like corrupt records which have been read in a format not expected by the processor. The rejected records tab allows the user to see a list of all the rejected records and other information about the nature of the rejection and where this occurred in the process.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/rejected-records-tab.png" title="Rejected Records Tab" >}}

\
{{< alert color="secondary">}}Writing rejected records can be disabled using [options dialogue]({{<relref "docs/advanced-etl-processor/options-list/create-rejected-records-file" >}}){{< /alert >}}

## Working with objects

The new transformation consists of Reader, Validator, Transformer and Writer. You may add a new object at any time by dragging it from the Objects panel.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-working-with-objects.png" title="Creating New Transformation and Working with Objects" >}}

To join two objects together, first click on the source Output button then drag it on to the Input button.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformer-joining-objects.png" title="joining two objects together" >}}

To remove the link, repeat the same procedure again.

## Object popup menu options

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/object-popup-menu-options.png" title="Deleting Object" >}}
\
To change object properties double click on it.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/transformation-editor.png" title="To change object properties double click on it" >}}

## Automatic Version Control

Every time the user presses the save button transformation is automatically added to the version control

## Notes Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/notes-dialogues.png" title="Notes Dialogue" >}}

## Incremental search

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/incremental-search.png" title="Incremental Search" >}}

The incremental search dialogue provides a convenient way of locating transformation objects to the end-user within complex data mappings.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/incremental-search-dialogue.png" title="Incremental Search" >}}

## Video Tutorials:

{{< youtube id="Wd58pvMkpVY" class="ratio ratio-16x9" >}}
\
{{< youtube id="j-sNUMrUn30" class="ratio ratio-16x9" >}}

{{< aetl >}}
