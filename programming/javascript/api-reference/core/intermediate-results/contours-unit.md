---
layout: default-layout
title: interface ContoursUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ContoursUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ContoursUnit

The `ContoursUnit` interface represents a unit that contains contours as part of intermediate results.It extends the IntermediateResultUnit interface.

## Definition

```typescript
interface ContoursUnit extends IntermediateResultUnit {
    contours: Array<Core.BasicStructures.Contour>;
}
```

| Properties               | Type |
|----------------------|-------------|
| [`contours`](#contours) | *Array<Core.BasicStructures.Contour>* |

### contours

An array of contours stored in the unit.

```typescript
contours: Array<Core.BasicStructures.Contour>;
```
