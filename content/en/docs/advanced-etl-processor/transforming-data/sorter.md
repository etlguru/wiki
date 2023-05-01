---
author: Peter Jonson
title: Working with Sorter
description: Working with Sorter
draft: false
tags: ['Transformation', 'Sorter']
date: 2022-09-17
group: advanced-etl-processor-transformation
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/sorter.png" title="Sorter" >}}

## About Sorting

In computer science and mathematics, a sorting algorithm is an algorithm that puts elements of a list in a certain order. All sorting algorithms are very well documented and it is hard to invent something new or much faster that existing algorithm. To achieve the best performance is important to load all the data into the memory which is not possible for large amount of data. [Advanced ETL Processor](https://www.etl-tools.com/advanced-etl-processor/overview.html)uses combination of Quicksort and Merge sort. Portion of Data is loaded in the memory and sorted using Quicksort algorithm than data is saved into temporary file. Once all portions are sorted temporary files merged together using Merge sort algorithm.

## Quicksort

Quicksort is a divide and conquer algorithm which relies on a partition operation: to partition an array, we choose an element, called a pivot, move all smaller elements before the pivot, and move all greater elements after it. This can be done efficiently in linear time and in-place. We then recursively sort the lesser and greater sublists. Efficient implementations of quicksort (with in-place partitioning) are typically unstable sorts and somewhat complex, but are among the fastest sorting algorithms in practice. Together with its modest O(log n) space usage, this makes quicksort one of the most popular sorting algorithms, available in many standard libraries. The most complex issue in quicksort is choosing a good pivot element; consistently poor choices of pivots can result in drastically slower (O(n²)) performance, but if at each step we choose the median as the pivot then it works in O(n log n).

## Merge sort

Merge sort takes advantage of the ease of merging already sorted lists into a new sorted list. It starts by comparing every two elements (i.e., 1 with 2, then 3 with 4...) and swapping them if the first should come after the second. It then merges each of the resulting lists of two into lists of four, then merges those lists of four, and so on; until at last two lists are merged into the final sorted list. Of the algorithms described here, this is the first that scales well to very large lists, because its worst-case running time is O(n log n).

To change Sorter properties double click on the object. Tick sort, select field order and sort order. Field order must be unique for sort field. Data is loaded in the memory first than sorted and passed to the next object. Buffer size specifies number of records loaded into memory.

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/sorter-properties.png" title="Merge sort" >}}

{{< aetl >}}
