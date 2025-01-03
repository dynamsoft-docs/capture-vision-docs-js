---
layout: default-layout
title: Interface CapturedResultItem - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResultItem in Dynamsoft Core Module.
keywords: captured result item, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` interface provides a common structure for representing different types of captured results. Each specific captured result item type will have its own implementation and additional properties specific to that type.

> NOTE: 
> 
> Depending on the functional module that generated the result item, the interface may vary:
> 
> * dynamsoft-barcode-reader: [BarcodeResultItem](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/barcode-result-item.html)
> * dynamsoft-label-recognizer: [TextLineResultItem](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/textline-result-item.html)
> * dynamsoft-document-normalizer: [DetectedQuadResultItem](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/detected-quad-result-item.html) or [NormalizedImageResultItem](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/normalized-image-result-item.html)
> * dynamsoft-code-parser: [ParsedResultItem](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/interfaces/parsed-result-item.html)

```typescript
interface CapturedResultItem {
    readonly type: EnumCapturedResultItemType;
    readonly referencedItem: CapturedResultItem;
}
```

## type

The type of the captured result item, indicating what kind of data it represents.

**See Also**

[EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)

## referencedItem

A property of type `CapturedResultItem` that represents a reference to another captured result item.
