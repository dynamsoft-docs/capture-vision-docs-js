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
    toCanvas: () => HTMLCanvasElement;
    toImage: (MIMEType: "image/png" | "image/jpeg") => HTMLImageElement;
    toBlob: (MIMEType: "image/png" | "image/jpeg") => Promise<Blob>;
}
```

## imageData

The image data associated with this result item.

## toCanvas

Converts the image data into an HTMLCanvasElement for display or further manipulation in web applications.

**See Also**

[HTMLCanvasElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement)

**Remarks**

Introduced in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.2000.

## toImage

Converts the image data into an HTMLImageElement of a specified MIME type ('image/png' or 'image/jpeg').

**See Also**

[HTMLImageElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement)

**Remarks**

Introduced in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.2000.

## toBlob

Converts the image data into a Blob object of a specified MIME type ('image/png' or 'image/jpeg').

**See Also**

[Blob](https://developer.mozilla.org/en-US/docs/Web/API/Blob)

**Remarks**

Introduced in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.2000.