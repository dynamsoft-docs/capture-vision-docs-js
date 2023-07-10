---
layout: default-layout
title: interface LineSegment - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface LineSegment in Dynamsoft Core Module.
keywords: line segment, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineSegment

The LineSegment interface represents a line segment in 2D space. It contains two Point objects, which represent the start point and end point of the line.

## Definition

```ts
export interface LineSegment {
                startPoint: Point;
                endPoint: Point;
            } 
```

## Attributes Summary

| Attribute | Type |
|---------- | ---- |
| [`startPoint`](#startPoint) | *Point* |
| [`endPoint`](#endPoint) | *Point* |

### startPoint

The start point of the line segment.

### endPoint

The end point of the line segment.
