---
author: Peter Jonson
title: Package
description: Package combines various actions together
draft: false
tags: ['Package']
date: 2022-09-17
group: advanced-etl-processor-enterprise-package
menu: advanced-etl-processor-enterprise
layout: docs
weight: 1
---

Package combines various actions together. Every package has a starting point. Package actions executed sequentially starting from the starting point. Package action execution status can be success of failure. Depending of execution status next action is executed.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/basic-package.png" title="Basic Package" >}}

## Action Execution

Action execution consist of three stages

**1 Preparation**

Action parameters are calculated and variables are replaced with actual values

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-prepare.png" title="Package Action Preparation" >}}

**2 Execution**

**3 Assigning variables selected on after execution tab**

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-assign-variables.png" title="After execution tab" >}}

## Package Example

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/example-of-data-warehouse-workflow.png" title="Package Example" >}}

## Creating New Package

- To create a new Package select a Package group from the objects tree and click New
- Dialog box will appear
- Fill in the Description edit box with the name of the Package you are about to create
- Fill in a comment if required
- Click OK to finish the creation of the Package

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-properties.png" title="Package Action Variables" >}}

## Package Screen Overview

Every package must have a starting point (Action on the left of the picture). Action execution state defines which action is executed next. The Blue line is a success and the Orange Line is a failure.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-screen-overview-1.png" title="Package Screen Overview" >}}

## Setting Starting Point

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-starting-point-2.png" title="Setting Starting Point" >}}

## Joining Actions

Objects can be joined to other objects as shown here. This is achieved by simple “drag” and “drop” of the items from one to another. To remove the link repeat the process.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/joining-actions.png" title="Joining Actions" >}}

## Catch All Actions

Catch-All Actions provide a way of reducing the complexity of a package

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-action.png" title="Catch All Actions" >}}

### On Error

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/on-error.png" title="On Error" >}}

### On Success

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/on-success.png" title="On Success" >}}

## Package Tool bar

The package toolbar provides all the tools you need in order to create and manipulate objects. It is also possible to change how objects are viewed in the interface.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/packages/package-tool-bar.png" title="Package Tool bar" >}}

1. Packages Properties
1. Open Package from file
1. Save Package to file
1. Save to the Repository
1. Print
1. Print Preview
1. Cut
1. Copy
1. Paste
1. Delete selected Action(s)
1. Clear all
1. Undo
1. Redo
1. Search
1. Align Left
1. Arrange Vertically
1. Align Right
1. Align Bottom
1. Arrange Horizontally
1. Align Top
1. Space Horizontally
1. Space Vertically
1. Snap to grid/show grid
1. Manage Versions
1. Add Version
1. Revert to previous version
1. Make Package Read Only
1. Show/Hide execution log
1. Open execution log directory
1. Schedule Package for Execution
1. View Execution Log (When executed by agent/scheduler)
1. Debug package
1. Continue execution
1. Execute Package using agent/Integrated Scheduler
1. Stop package execution
1. Zoom In
1. Zoom Out
1. Zoom back to 100%

## Automatic Version Control

Every time the user presses the save button package is automatically added to the version control

## Notes Dialogue

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/notes-dialogues.png" title="Notes Dialogue" >}}

## Useful links

- [Debugging Package]({{<relref "docs/advanced-etl-processor/packages/debugging" >}})
- [Using Variables]({{<relref "docs/advanced-etl-processor/packages/variables" >}})
- [Working with Filenames and Directories]({{<relref "docs/advanced-etl-processor/packages/file-names-and-directories" >}})
- [List of actions]({{<relref "docs/advanced-etl-processor/packages/actions" >}})

## Video Tutorial

{{< youtube id="XRaNITMpxP8" class="ratio ratio-16x9" >}}

{{< aetl >}}
