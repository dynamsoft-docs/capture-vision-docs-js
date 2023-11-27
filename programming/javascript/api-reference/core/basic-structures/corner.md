---
layout: default-layout
title: interface Corner - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the class Corner in Dynamsoft Core Module.
keywords: corner, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Corner

The `Corner` interface defines the structure of a "Corner" object which consists of two lines and the intersection point in 2-dimensional space.

## Definition

```typescript
interface Corner {
    type: EnumCornerType;
    intersection: Point;
    line1: LineSegment;
    Line2: LineSegment;
} 
```
  
| Properties | Type |
|---------- | ---- |
| [type](#type) | *EnumCornerType* |
| [intersection](#intersection) | *Point* |
| [line1](#line1) | *LineSegment* |
| [line2](#line2) | *LineSegment* |

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
