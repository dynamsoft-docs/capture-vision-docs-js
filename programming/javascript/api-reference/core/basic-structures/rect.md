---
layout: default-layout
title: Interface Rect - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Rect in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Rect

The `Rect` interface extends the `IntermediateResultUnit` interface and represents a rectangle in a 2D space, providing a JavaScript equivalent of [DSRect](./ds-rect.md).

> If measured in percentage, the value range for x/y/width/height is 0~1.

```typescript
interface Rect {
    x: number;
    y: number;
    width: number;
    height: number;
    isMeasuredInPercentage?: boolean;
}
```

## x

The x-coordinate of the rectangle's top-left corner.

## y

The y-coordinate of the rectangle's top-left corner.

## width

The width of the rectangle.

## height

The height of the rectangle.

## isMeasuredInPercentage

Optional. Indicates if the rectangle's measurements are in percentages.
