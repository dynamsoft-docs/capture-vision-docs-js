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

The `DSRect` interface represents a rectangle, similar to [CRect](https://www.dynamsoft.com/capture-vision/docs/server/programming/cplusplus/api-reference/core/basic-structures/rect.html) in C++, with an added feature for measurement in percentages.

> If measured in percentage, the value range for left/right/top/bottom is 0~100.

```typescript
interface DSRect {
    left: number;
    right: number;
    top: number;
    bottom: number;
    isMeasuredInPercentage: boolean;
}
```

## left

The left coordinate of the rectangle.

## right

The right coordinate of the rectangle.

## top

The top coordinate of the rectangle.

## bottom

The bottom coordinate of the rectangle.

## isMeasuredInPercentage

Indicates if the rectangle's measurements are in percentages.
