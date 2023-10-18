---
layout: default-layout
title: interface Edge - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface Edge in Dynamsoft Core Module.
keywords: edge, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Edge

The `Edge` interface defines a shape that is composed of two `Corner` points in 2-dimensional space.

## Definition

```typescript
interface Edge {
    startCorner: Corner;
    endCorner: Corner;
}
```

## Attributes
  
| Properties | Type |
|---------- | ---- |
| [`startCorner`](#startcorner) | *Corner* |
| [`endCorner`](#endcorner) | *Corner* |

### startCorner

The start corner point of the edge.

```typescript
startCorner: Corner;
```

### endCorner

The end corner point of the edge.

```typescript
endCorner: Corner;
```
