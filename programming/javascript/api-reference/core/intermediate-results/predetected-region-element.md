---
layout: default-layout
title: interface PredetectedRegionElement - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interfaace PredetectedRegionElement in Dynamsoft Core Module.
keywords: line segments, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionElement

The `PredetectedRegionElement` interface extends the RegionObjectElement interface and represents a predetected region element.

## Definition

```typescript
interface PredetectedRegionElement extends RegionObjectElement {
    modeName: string;
}
```

| Properties               | Type |
|----------------------|-------------|
| [`modeName`](#modename) | *String* |

### modeName

Gets the specified region pre-detection mode name

```typescript
modeName: string;
```