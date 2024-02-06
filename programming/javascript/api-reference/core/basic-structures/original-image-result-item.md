---
layout: default-layout
title: Interface OriginalImageResultItem - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface OriginalImageResultItem in Dynamsoft Capture Vision Router Module.
keywords: original image, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` interface extends the [CapturedResultItem](./captured-result-item.md) interface and represents an original image result item.

```typescript
interface OriginalImageResultItem extends CapturedResultItem {
    readonly imageData: DSImageData;
}
```

## imageData

The image data associated with this result item.
