---
layout: default-layout
title: interface Polygon - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Polygon in Dynamsoft Core Module.
keywords: Polygon, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Polygon

The interface Polygon represents a Polygon in 2D space. It contains of an array storing Point objects to represent the coordinates of the Polygon.

## Definition

```js
export interface Polygon {
                points: Array<Core.BasicStructures.Point>;
            }
```

## Attributes Summary

| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *Array* |

### points

An array that stores many points.

```js
points: Array<Core.BasicStructures.Point>;
```
