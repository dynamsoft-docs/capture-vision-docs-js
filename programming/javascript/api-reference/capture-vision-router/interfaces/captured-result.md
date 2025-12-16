---
layout: default-layout
title: Interface CapturedResult - Dynamsoft Capture Vision Router Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResult in Dynamsoft Capture Vision Router Module.
keywords: captured result, JS, capture vision
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
> * dynamsoft-document-normalizer: [ProcessedDocumentResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/processed-document-result.html)
> * dynamsoft-code-parser: [ParsedResult](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/interfaces/parsed-result.html)

```typescript
interface CapturedResult extends CapturedResultBase{
    items: Array<CapturedResultItem>;
    decodedBarcodesResult?: DecodedBarcodesResult;
    recognizedTextLinesResult?: RecognizedTextLinesResult;
    processedDocumentResult?: ProcessedDocumentResult;
    parsedResult?: ParsedResult;
}
```

## items

An array of [CapturedResultItem]({{ site.dcvb_js_api }}core/basic-structures/captured-result-item.html) objects representing the captured result items.

## barcodeResultItems

An array of [BarcodeResultItem]({{ site.dbr_js_api }}interfaces/barcode-result-item.html) objects representing the decoded barcode result items.

## textLineResultItems

An array of [TextLineResultItem]({{ site.dlr_js_api }}interfaces/textline-result-item.html) objects representing the recognized text line result items.

## processedDocumentResult

An array of [ProcessedDocumentResultItem]({{ site.ddn_js_api }}interfaces/processed-document-result-item.html) objects representing the processed document result related items.

## parsedResultItems

An array of [ParsedResultItem]({{ site.dcp_js_api }}interfaces/parsed-result-item.html) objects representing the parsed result items.
