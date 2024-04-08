---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Capture Vision Router Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Capture Vision Router Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` interface describes the basic structure of a result object returned by Dynamsoft Capture Vision Router.

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
    readonly errorCode: number;
    readonly errorString: string;
    readonly originalImageHashId: string;
    readonly originalImageTag: Core.ImageTag;
    readonly items: Array<Core.CapturedResultItem>;
    readonly detectedQuadResultItems: Array<DDN.DetectedQuadResultItem>;
    readonly normalizedImageResultItems: Array<DDN.NormalizedImageResultItem>;
    readonly barcodeResultItems: Array<DBR.BarcodeResultItem>;
    readonly textLineResultItems: Array<DLR.TextLineResultItem>;
    readonly parsedResultItems: Array<DCP.ParsedResultItem>;
}
```

## errorCode

Error code associated with the capture result.

## errorString

Error string providing details about the error.

## originalImageHashId

The hash ID of the original image.

## originalImageTag

The tag associated with the original image.

## items

An array of [CapturedResultItem]({{ site.dcv_js_api }}core/basic-structures/captured-result-item.html) objects representing the captured result items.

## detectedQuadResultItems

An array of [DetectedQuadResultItem]({{ site.ddn_js_api }}interfaces/detected-quad-result-item.html) objects representing the detected quadrilateral result items.

## normalizedImageResultItems

An array of [NormalizedImageResultItem]({{ site.ddn_js_api }}interfaces/normalized-image-result-item.html) objects representing the normalized image result items.

## barcodeResultItems

An array of [BarcodeResultItem]({{ site.dbr_js_api }}interfaces/barcode-result-item.html) objects representing the decoded barcode result items.

## textLineResultItems

An array of [TextLineResultItem]({{ site.dlr_js_api }}interfaces/textline-result-item.html) objects representing the recognized text line result items.

## parsedResultItems

An array of [ParsedResultItem]({{ site.dcp_js_api }}interfaces/parsed-result-item.html) objects representing the parsed result items.