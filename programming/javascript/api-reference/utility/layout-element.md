---
layout: default-layout
title: Interface LayoutElement - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the interface LayoutElement in Dynamsoft Utility Module.
keywords: layout element, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# LayoutElement

The `LayoutElement` interface represents an element in a layout analysis.

```typescript
interface LayoutElement {
    quad: Quadrilateral;
    source: EnumLayoutElementSource;
}
```

## quad

The geometric coordinates of the element.

## source

The origin of this element, of type `EnumLayoutElementSource`.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.