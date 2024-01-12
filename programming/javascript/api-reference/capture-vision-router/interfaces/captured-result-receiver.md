---
layout: default-layout
title: Interface CapturedResultReceiver - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.30
description: This page introduces the CapturedResultReceiver interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.30.
keywords: captured result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS CapturedResultReceiver Interface
---

# CapturedResultReceiver

The `CapturedResultReceiver` interface defines the standard way to get captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

```typescript
interface CapturedResultReceiver {
    onCapturedResultReceived?(result: Core.CapturedResult): void;
    onOriginalImageResultReceived?(result: OriginalImageResultItem): void;
    onDecodedBarcodesReceived?(result: DBR.DecodedBarcodesResult): void;
    onRecognizedTextLinesReceived?(result: DLR.RecognizedTextLinesResult):void;
    onDetectedQuadsReceived?(result: DDN.DetectedQuadsResult): void;
    onNormalizedImagesReceived?(result: DDN.NormalizedImagesResult): void;
    onParsedResultsReceived?(result: DCP.ParsedResult): void;
} 
```

| API Name                                                          | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [onCapturedResultReceived()](#oncapturedresultreceived)           | Callback function for all captured results.          |
| [onOriginalImageResultReceived()](#onoriginalimageresultreceived) | Callback function for original image results.        |
| [onDecodedBarcodesReceived()](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [onRecognizedTextLinesReceived()](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [onDetectedQuadsReceived()](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [onNormalizedImagesReceived()](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [onParsedResultsReceived()](#onparsedresultsreceived)             | Callback function for parsed results.                |

## onCapturedResultReceived

Callback function for all captured results. It will be called once for each captured result.

```typescript
onCapturedResultReceived(result: Core.CapturedResult): void;
```

**Parameters**

`result`: The captured result.

## onOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```typescript
onOriginalImageResultReceived(result: OriginalImageResultItem): void;
```

**Parameters**

`result`: The original image result.

## onDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```typescript
onDecodedBarcodesReceived(result: DBR.DecodedBarcodesResult): void;
```

**Parameters**

`result`: The decoded barcodes result.

## onRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```typescript
onRecognizedTextLinesReceived(result: DLR.RecognizedTextLinesResult): void;
```

**Parameters**

`result`: The recognized text lines result.

## onDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```typescript
onDetectedQuadsReceived(result: DDN.DetectedQuadsResult): void;
```

**Parameters**

`result`: The detected quads result.

## onNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```typescript
onNormalizedImagesReceived(result: DDN.NormalizedImagesResult): void;
```

**Parameters**

`result`: The normalized images result.

## onParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```typescript
onParsedResultsReceived(result: DCP.ParsedResult): void;
```

**Parameters**

`result`: The parsed result.