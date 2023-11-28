---
layout: default-layout
title: Interface ScaledDownColourImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ScaledDownColourImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ScaledDownColourImageUnit

The `ScaledDownColourImageUnit` interface represents a colour image unit after scaling.

## Definition

```typescript
interface ScaledDownColourImageUnit extends IntermediateResultUnit {
    imageData: Core.DSImageData;
} 
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.DSImageData* |

### imageData

The scaled down colour image data stored in the unit.

```typescript
imageData: Core.DSImageData;
```