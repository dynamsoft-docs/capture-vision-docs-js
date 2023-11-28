---
layout: default-layout
title: Interface DSRect - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSRect in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# DSRect

The `DSRect` interface defines the shape of a rectangle in 2D space.

## Definition

```typescript
interface DSRect {
    left: number;
    right: number;
    top: number;
    bottom: number;
    isMeasuredInPercentage: boolean;
}
```

| Properties            | Type |
|----------------------|-------------|
| [left](#left) | *number* |
| [right](#right) | *number* |
| [top](#top) | *number* |
| [bottom](#bottom) | *number* |
| [isMeasuredInPercentage](#ismeasuredinpercentage) | *boolean* |

### left

The left edge of the rectangle.

```typescript
left: number;
```

### right

The right edge of the rectangle.

```typescript
right: number;
```

### top

The top edge of the rectangle.

```typescript
top: number;
```

### bottom

The bottom edge of the rectangle.

```typescript
bottom: number;
```

### isMeasuredInPercentage

Whether to use a percentage measurement for this DSRect.

```typescript
isMeasuredInPercentage: boolean;
```
