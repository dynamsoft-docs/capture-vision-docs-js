---
layout: default-layout
title: Interface LineSegment - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface LineSegment in Dynamsoft Core Module.
keywords: line segment, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LineSegment

The `LineSegment` interface defines a "line" shape in 2-dimensional space.

## Definition

```typescript
interface LineSegment {
    startPoint: Point;
    endPoint: Point;
} 
```

| Properties | Type |
|---------- | ---- |
| [startPoint](#startpoint) | *Point* |
| [endPoint](#endpoint) | *Point* |

### startPoint

The start point of the line segment.

```typescript
startPoint: Point;
```

### endPoint

The end point of the line segment.

```typescript
endPoint: Point;
```