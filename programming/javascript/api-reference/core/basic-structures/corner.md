---
layout: default-layout
title: interface Corner - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the class Corner in Dynamsoft Core Module.
keywords: corner, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Corner

Corner is a structure in an image consisting of two line segments and intersection point. A Corner represents a point at which the image's brightness or color sharply changes.

## Definition

```typescript
interface Corner {
                type: EnumCornerType;
                intersection: Point;
                line1: LineSegment;
                Line2: LineSegment;
            } 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`type`](#type) | *EnumCornerType* |
| [`intersection`](#intersection) | *Point* |
| [`line1`](#line1) | *LineSegment* |
| [`line2`](#line2) | *LineSegment* |

### type

The type of the corner.

```typescript
type: EnumCornerType;
```

### intersection

The intersection point of the corner.

```typescript
intersection: Point;
```

### line1

The first line connected to the corner.

```typescript
line1: LineSegment;
```

### line2

The second line connected to the corner.

```typescript
Line2: LineSegment;
```
