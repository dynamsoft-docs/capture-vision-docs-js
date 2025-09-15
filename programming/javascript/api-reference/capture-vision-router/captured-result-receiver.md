---
layout: default-layout
title: Class CapturedResultReceiver - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.30
description: This page introduces the CapturedResultReceiver class in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.30.
keywords: captured result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS CapturedResultReceiver Class
---

# CapturedResultReceiver

The `CapturedResultReceiver` class is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. It adopts an event-driven approach, with events dedicated to various result types, such as the original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results, etc.

```typescript
class CapturedResultReceiver {
    onCapturedResultReceived?(result: CapturedResult): void;
    onOriginalImageResultReceived?(result: OriginalImageResultItem): void;
    onDecodedBarcodesReceived?(result: DecodedBarcodesResult): void;
    onRecognizedTextLinesReceived?(result: RecognizedTextLinesResult):void;
    onDetectedQuadsReceived?(result: DetectedQuadsResult): void;
    onNormalizedImagesReceived?(result: NormalizedImagesResult): void;
    onParsedResultsReceived?(result: ParsedResult): void;
} 
```

| Name                                                              | Description                                                  |
| ----------------------------------------------------------------- | ------------------------------------------------------------ |
| [onCapturedResultReceived()](#oncapturedresultreceived)           | Event triggered when a generic captured result is available. |
| [onOriginalImageResultReceived()](#onoriginalimageresultreceived) | Event triggered when the original image result is available. |
| [onDecodedBarcodesReceived()](#ondecodedbarcodesreceived)         | Event triggered when decoded barcodes are available.         |
| [onRecognizedTextLinesReceived()](#onrecognizedtextlinesreceived) | Event triggered when recognized text lines are available.    |
| [onDetectedQuadsReceived()](#ondetectedquadsreceived)             | Event triggered when detected quads are available.           |
| [onNormalizedImagesReceived()](#onnormalizedimagesreceived)       | Event triggered when normalized images are available.        |
| [onParsedResultsReceived()](#onparsedresultsreceived)             | Event triggered when parsed results are available.           |

## onCapturedResultReceived

Event triggered when a generic captured result is available, occurring each time an image finishes its processing. This event can be used for any result that does not fit into the specific categories of the other callback events.

```typescript
onCapturedResultReceived(result: CapturedResult): void;
```

**Parameters**

The captured result, an instance of `CapturedResult`.

**See Also**

[CapturedResult](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/capture-vision-router/interfaces/captured-result.html?product=dbr&lang=javascript)

## onOriginalImageResultReceived

Event triggered when the original image result is available. This event is used to handle the original image captured by an image source such as Dynamsoft Camera Enhancer.

```typescript
onOriginalImageResultReceived(result: OriginalImageResultItem): void;
```

**Parameters**

`result`: The original image result, an instance of `OriginalImageResultItem`.

**See Also**

[OriginalImageResultItem](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/core/basic-structures/original-image-result-item.html?product=dbr&lang=javascript)

## onDecodedBarcodesReceived

Event triggered when decoded barcodes are available. This event is used to handle barcodes that have been successfully decoded by Dynamsoft Barcode Reader

```typescript
onDecodedBarcodesReceived(result: DecodedBarcodesResult): void;
```

**Parameters**

`result`: The decoded barcode result, an instance of `DecodedBarcodesResult`.

**See Also**

[DecodedBarcodesResult](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/decoded-barcodes-result.html)

## onRecognizedTextLinesReceived

Event triggered when recognized text lines are available. This event is used to handle the result of text recognition by Dynamsoft Label Recognizer.

```typescript
onRecognizedTextLinesReceived(result: RecognizedTextLinesResult): void;
```

**Parameters**

`result`: The recognized text lines result, an instance of `RecognizedTextLinesResult`.

[RecognizedTextLinesResult](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/recognized-textlines-result.html)

## onDetectedQuadsReceived

Event triggered when detected quads are available. This event is used to handle the detection of quadrilateral shapes, typically used as document boundaries, by Dynamsoft Document Normalizer.

```typescript
onDetectedQuadsReceived(result: DetectedQuadsResult): void;
```

**Parameters**

`result`: The detected quads result, an instance of `DetectedQuadsResult`.

**See Also**

[DetectedQuadsResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/detected-quads-result.html)

## onNormalizedImagesReceived

Event triggered when normalized images are available. This event is used for handling images that have been processed or normalized (e.g., corrected for skew or perspective), by Dynamsoft Document Normalizer.

```typescript
onNormalizedImagesReceived(result: NormalizedImagesResult): void;
```

**Parameters**

`result`: The normalized images result, an instance of `NormalizedImagesResult`.

**See Also**

[NormalizedImagesResult](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/normalized-images-result.html)

## onParsedResultsReceived

Event triggered when parsed results are available. This event is used for handling results that have been parsed into a structured format by Dynamsoft Code Parser.

```typescript
onParsedResultsReceived(result: ParsedResult): void;
```

**Parameters**

`result`: The parsed result, an instance of `ParsedResult`.

**See Also**

[ParsedResult](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/interfaces/parsed-result.html)