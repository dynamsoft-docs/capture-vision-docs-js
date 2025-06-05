---
layout: default-layout
title: Interface PredetectedRegionElement - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interfaace PredetectedRegionElement in Dynamsoft Core Module.
keywords: line segments, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# PredetectedRegionElement

The `PredetectedRegionElement` interface extends the `RegionObjectElement` interface and represents a pre-detected region element in an image.

```typescript
interface PredetectedRegionElement extends RegionObjectElement {
    modeName: string;
    labelID: number;
    labelName: string;
}
```

## modeName

The name of the detection mode used to detect this region element.

## labelID

The label id of the predetected region element.

## labelName

The label name of the predetected region element.