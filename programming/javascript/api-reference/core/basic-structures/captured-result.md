---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# CapturedResult

The [CapturedResult]({{ site.dcv_js_api }}core/basic-structures/captured-result.html) interface describes the basic structure of a result item returned by Dynamsoft Capture Vision Router.

> NOTE: 
> 
> Depending on the functional module that generated the result item, the interface may vary:
> 
> * dynamsoft-barcode-reader: [DecodedBarcodesResult](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/decoded-barcodes-result.html)
> * dynamsoft-label-recognizer: [RecognizedTextLinesResult](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/recognized-textlines-result.html)
> * dynamsoft-document-normalizer: [DetectedQuadsResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/detected-quads-result.html) or [NormalizedImagesResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/normalized-images-result.html)
> * dynamsoft-code-parser: [ParsedResult](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/interfaces/parsed-result.html)

```typescript
interface CapturedResult {
    readonly originalImageHashId: string;
    readonly originalImageTag: ImageTag;
    readonly items: Array<CapturedResultItem>;
    readonly errorCode: number;
    readonly errorString: string;
}
```

## originalImageHashId

The hash ID of the original image.

## originalImageTag

The tag associated with the original image.

## items

An array of [CapturedResultItem](./captured-result-item.md) objects representing the captured result items.

## errorCode

Error code associated with the capture result.

## errorString

Error string providing details about the error.
