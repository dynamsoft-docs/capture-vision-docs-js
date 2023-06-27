---
layout: default-layout
title: interface CapturedResultItem - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResultItem in Dynamsoft Core Module.
keywords: captured result item, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` interface provides a common structure for representing different types of captured results. Each specific captured result item type will have its own implementation and additional properties specific to that type.

## Definition

```js
export interface CapturedResultItem {
                readonly type: EnumCapturedResultItemType;
                readonly referenceItem: CapturedResultItem;
            }
```

## Attributes Summary

| Attribute                         | Type|
|--------------------------------|------------|
| [`type`](#type)              | *EnumCapturedResultItemType*          |
| [`referenceItem`](#referenceItem)    | *CapturedResultItem*          |

### type

A property of type `EnumCapturedResultItemType` that specifies the type of the captured result item.

```js
readonly type: EnumCapturedResultItemType;
```

### referenceItem

A property of type `CapturedResultItem` that represents a reference to another captured result item.

```js
readonly referenceItem: CapturedResultItem;
```