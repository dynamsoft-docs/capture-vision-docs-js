---
layout: default-layout
title: interface DSRect - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface DSRect in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRect

The interface DSRect represents a rectangle in 2D space. It contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

```js
export interface DSRect {
                left: number;
                right: number;
                top: number;
                bottom: number;
                isMeasuredInPercentage: boolean;
            }
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`left`](#left) | *number* |
| [`right`](#right) | *number* |
| [`top`](#top) | *number* |
| [`bottom`](#bottom) | *number* |
| [`isMeasuredInPercentage`](#isMeasuredInPercentage) | *boolean* |

### left

The left edge of the rectangle.

```js
bytes: Uint8Array;
```

### right

The right edge of the rectangle.

```js
width: number;
```

### top

The top edge of the rectangle.

```js
height: number;
```

### bottom

The bottom edge of the rectangle.

```js
stride: number;
```

### isMeasuredInPercentage

Whether to use a percentage measurement for this DSRect.

```js
isMeasuredInPercentage: boolean;
```
