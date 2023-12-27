---
layout: default-layout
title: Interface BinaryImageUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface BinaryImageUnit in Dynamsoft Core Module.
keywords: binary image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# BinaryImageUnit

The `BinaryImageUnit` interface represents a binary image unit.

```typescript
interface BinaryImageUnit extends IntermediateResultUnit {
    imageData: Core.DSImageData;
} 
```

| Properties               | Type |
|----------------------|-------------|
| [imageData](#imagedata) | *Core.DSImageData* |

## imageData

The binary image data stored in the unit.

```typescript
imageData: Core.DSImageData;
```