---
layout: default-layout
title: Interface TextureDetectionResultUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface TextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` interface extends the `IntermediateResultUnit` interface and represents a texture-detection result unit. This interface captures the results of texture analysis, specifically the spacing of texture patterns in both the x and y directions.

```typescript
interface TextureDetectionResultUnit extends IntermediateResultUnit {
    xSpacing: number;
    ySpacing: number;
}
```

## xSpacing

This value represents the detected horizontal distance in pixels between consecutive texture patterns, providing an indication of the texture's density and orientation within the image.

## ySpacing

The spacing between texture stripes in the y-direction. Similar to `xSpacing`, this value measures the vertical distance between texture patterns. It offers insights into the vertical density and alignment of the texture within the image, contributing to the understanding of the texture's characteristics and spatial distribution.
