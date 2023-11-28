---
layout: default-layout
title: interface LineSegmentsUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interfaace LineSegmentsUnit in Dynamsoft Core Module.
keywords: line segments, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` interface extends the IntermediateResultUnit interface and represents a unit of intermediate result specifically for line segments. It includes additional properties that provide information about the line segments.

## Definition

```typescript
interface LineSegmentsUnit extends IntermediateResultUnit {
    lineSegments: Array<Core.LineSegment>;
}
```

| Properties               | Type |
|----------------------|-------------|
| [lineSegments](#linesegments) | *Array\<Core.LineSegment>* |

### lineSegments

Gets the specified line segment from the collection.

```typescript
lineSegments: Array<Core.LineSegment>;
```