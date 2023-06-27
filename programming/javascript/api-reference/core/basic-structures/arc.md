---
layout: default-layout
title: interface Arc - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Arc in Dynamsoft Core Module.
keywords: image data, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Arc

The Arc class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

```js
export interface Arc {
                x: number;
                y: number;
                radius: number;
                startAngle: number;
                endAngle: number;
            } 
```

## Attributes Summary

| Attribute            | Type |
|----------------------|-------------|
| [`x`](#x) | *number* |
| [`y`](#y) | *number* |
| [`radius`](#radius) | *number* |
| [`startAngle`](#startAngle) | *number* |
| [`endAngle`](#endAngle) | *number* |

### x

The x-coordinate of the center point of the arc.

```js
x: number;
```

### y

The y-coordinate of the center point of the arc.

```js
y: number;
```

### radius

The radius of the arc.

```js
radius: number;
```

### startAngle

The starting angle of the arc in radians.

```js
startAngle: number;
```

### endAngle

The ending angle of the arc in radians.

```js
endAngle: number;
```
