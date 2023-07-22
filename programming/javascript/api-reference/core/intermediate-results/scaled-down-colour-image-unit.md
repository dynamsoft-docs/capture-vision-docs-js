---
layout: default-layout
title: interface ScaledDownColourImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ScaledDownColourImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ScaledDownColourImageUnit

The ScaledDownColourImageUnit interface represents a colour image unit after scaling.

## Definition

```typescript
interface ScaledDownColourImageUnit extends IntermediateResultUnit {
                imageData: Core.BasicStructures.DSImageData;
            } 
```

## Attributes Summary

| Attribute               | Type |
|----------------------|-------------|
| [`imageData`](#imageData) | *Core.BasicStructures.DSImageData* |

### imageData

The scaled down colour image data stored in the unit.

```typescript
imageData: Core.BasicStructures.DSImageData;
```