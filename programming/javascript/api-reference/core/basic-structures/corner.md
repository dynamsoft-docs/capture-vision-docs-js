---
layout: default-layout
title: Interface Corner - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the class Corner in Dynamsoft Core Module.
keywords: corner, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Corner

The `Corner` interface represents a corner, typically where two line segments meet.

```typescript
interface Corner {
    type: EnumCornerType;
    intersection: Point;
    line1: LineSegment;
    line2: LineSegment;
} 
```

## type

The type of the corner, represented by the enumeration [EnumCornerType]({{ site.enums }}core/corner-type.html?lang=js).

## intersection

The point of intersection of the two lines forming the corner.

## line1

The first line segment forming the corner.

## line2

The second line connected to the corner.
