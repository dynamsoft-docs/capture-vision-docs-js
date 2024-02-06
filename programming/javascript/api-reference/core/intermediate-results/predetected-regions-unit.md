---
layout: default-layout
title: Interface PredetectedRegionsUnit - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface PredetectedRegionsUnit in Dynamsoft Core Module.
keywords: predetected regions, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# PredetectedRegionsUnit

 The `PredetectedRegionsUnit` interface extends the `IntermediateResultUnit` interface and represents a unit of intermediate result specifically for pre-detected regions.

```typescript
interface PredetectedRegionsUnit extends IntermediateResultUnit {
    predetectedRegions: Array<PredetectedRegionElement>;
}
```

## predetectedRegions

An array of `PredetectedRegionElement` objects, each representing a pre-detected region detected within the image.

**See Also**

[PredetectedRegionElement](./predetected-region-element.md)