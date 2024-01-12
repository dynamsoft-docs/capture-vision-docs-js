---
layout: default-layout
title: Interface CapturedResultItem - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResultItem in Dynamsoft Core Module.
keywords: captured result item, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` interface provides a common structure for representing different types of captured results. Each specific captured result item type will have its own implementation and additional properties specific to that type.

```typescript
interface CapturedResultItem {
    readonly type: EnumCapturedResultItemType;
    readonly referencedItem: CapturedResultItem;
}
```

| Properties                      | Type                         |
| ------------------------------- | ---------------------------- |
| [type](#type)                   | *EnumCapturedResultItemType* |
| [referencedItem](#referenceditem) | *CapturedResultItem*         |

## type

A property of type `EnumCapturedResultItemType` that specifies the type of the captured result item.

```typescript
readonly type: EnumCapturedResultItemType;
```

## referencedItem

A property of type `CapturedResultItem` that represents a reference to another captured result item.

```typescript
readonly referencedItem: CapturedResultItem;
```