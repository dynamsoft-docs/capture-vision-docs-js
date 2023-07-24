---
layout: default-layout
title: interface Rect - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Rect in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
---

# Rect

The interface Rect represents a rectangle in 2D space. It contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

```typescript
interface Rect {
                x: number;
                y: number;
                width: number;
                height: number;
                isMeasuredInPercentage?: boolean;
            }
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`x`](#x) | *number* |
| [`y`](#y) | *number* |
| [`width`](#width) | *number* |
| [`height`](#height) | *number* |
| [`isMeasuredInPercentage`](#isMeasuredInPercentage) | *boolean* |

### x

The x coordinate of the upper left corner point of the rectangle.

```typescript
x: number,
```

### y

The y coordinate of the upper left corner point of the rectangle.

```typescript
y: number,
```

### width

The width of the rectangle.

```typescript
width: number,
```

### height

The height of the rectangle.

```typescript
height: number;
```

### isMeasuredInPercentage

Whether to use a percentage measurement for this Rect.

```typescript
isMeasuredInPercentage: boolean;
```