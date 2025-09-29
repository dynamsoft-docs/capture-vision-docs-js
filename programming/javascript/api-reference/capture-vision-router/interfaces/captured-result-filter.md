---
layout: default-layout
title: Interface CapturedResultFilter - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.30
description: This page introduces the CapturedResultFilter interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.30.
keywords: captured result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS CapturedResultFilter Interface
---

<!--No need for public access, hidden in doc-->

# CapturedResultFilter

The `CapturedResultReceiver` class is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. It adopts an event-driven approach, with events dedicated to various result types, such as the original image, decoded barcodes, recognized text lines, processed documents, and parsed results, etc.

```typescript
class CapturedResultReceiver {
    onCapturedResultReceived?(result: CapturedResult): void;
    onOriginalImageResultReceived?(result: OriginalImageResultItem): void;
    onDecodedBarcodesReceived?(result: DecodedBarcodesResult): void;
    onRecognizedTextLinesReceived?(result: RecognizedTextLinesResult):void;
    onProcessedDocumentResultReceived?(result: ProcessedDocumentResult): void;
    onParsedResultsReceived?(result: ParsedResult): void;
} 
```

The `CapturedResultFilter` interface defines the standard way to get processing results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, processed documents, and parsed results.


## OnOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```typescript
onOriginalImageResultReceived(result: Core.OriginalImageResultItem): void;
```

**Parameters**

`result`: The original image result.

## OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```typescript
onDecodedBarcodesReceived(result: DBR.DecodedBarcodesResult): void;
```

**Parameters**

`result`: The decoded barcodes result.

## OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```typescript
onRecognizedTextLinesReceived(result: DLR.RecognizedTextLinesResult): void;
```

**Parameters**

`result`: The recognized text lines result.

## onProcessedDocumentResultReceived

Callback function for processed document results. It will be called once for each processed documents result.

```typescript
onProcessedDocumentResultReceived(result: DDN.ProcessedDocumentResult): void;
```

**Parameters**

`result`: The processed documents result.

## OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```typescript
onParsedResultsReceived(result: DCP.ParsedResult): void;
```

**Parameters**

`result`: The parsed result.
