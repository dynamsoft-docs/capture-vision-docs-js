---
layout: default-layout
title: interface BinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface BinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BinaryImageUnit

The BinaryImageUnit interface represents a binary image unit.

## Definition

```typescript
interface BinaryImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The binary image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```