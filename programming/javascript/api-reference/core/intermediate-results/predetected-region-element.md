---
layout: default-layout
title: interface PredetectedRegionElement - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interfaace PredetectedRegionElement in Dynamsoft Core Module.
keywords: line segments, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionElement

The PredetectedRegionElement interface extends the RegionObjectElement interface and represents a predetected region element.

## Definition

```ts
export interface PredetectedRegionElement extends RegionObjectElement {
                modeName: string;
}
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`modeName`](#modename) | *String* |

### modeName

Gets the specified region pre-detection mode name

```ts
modeName: string;
```