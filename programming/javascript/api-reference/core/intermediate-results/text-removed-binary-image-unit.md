---
layout: default-layout
title: interface TextRemovedBinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextRemovedBinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextRemovedBinaryImageUnit

The TextRemovedBinaryImageUnit interface represents a binary image unit after removing text.

## Definition

```js
export interface TextRemovedBinaryImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The text-removed binary image data stored in the unit.

```js
imageData: Core.BasicStructures.DSImageData;
```