---
layout: default-layout
title: interface CaptureResultReceiver - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface CaptureResultReceiver in Core Module.
keywords: captured result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS CaptureResultReceiver Interface
---

# CaptureResultReceiver

The `CaptureResultReceiver` interface is responsible for receiving captured results. It contains several callback functions for different types of results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

```typescript
interface CapturedResultReceiver {
  onCapturedResultReceived?(result: Core.BasicStructures.CapturedResult): void;
  onOriginalImageResultReceived?(result: OriginalImageResultItem): void;
  onDecodedBarcodesReceived?(result: DBR.DecodedBarcodesResult): void;
  onRecognizedTextLinesReceived?(result: DLR.RecognizedTextLinesResult):void;
  onDetectedQuadsReceived?(result: DDN.DetectedQuadsResult): void;
  onNormalizedImagesReceived?(result: DDN.NormalizedImagesResult): void;
  onParsedResultsReceived?(result: DCP.ParsedResult): void;
} 
```


| API Name                                                            | Description                                          |
| ------------------------------------------------------------------- | ---------------------------------------------------- |
| [`OnCapturedResultReceived()`](#oncapturedresultreceived)           | Callback function for all captured results.          |
| [`OnOriginalImageResultReceived()`](#onoriginalimageresultreceived) | Callback function for original image results.             |
| [`OnDecodedBarcodesReceived()`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived()`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived()`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived()`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived()`](#onparsedresultsreceived)             | Callback function for parsed results.                |

### OnCapturedResultReceived

Callback function for all captured results. It will be called once for each captured result.

```typescript
onCapturedResultReceived(result: Core.BasicStructures.CapturedResult): void;
```

**Parameters**

`result`: The captured result.

### OnOriginalImageResultReceived

Callback function for original image results. It will be called once for each original image result.

```typescript
onOriginalImageResultReceived(result: OriginalImageResultItem): void;
```

**Parameters**

`result`: The original image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```typescript
onDecodedBarcodesReceived(result: DBR.DecodedBarcodesResult): void;
```

**Parameters**

`result`: The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```typescript
onRecognizedTextLinesReceived(result: DLR.RecognizedTextLinesResult): void;
```

**Parameters**

`result`: The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```typescript
onDetectedQuadsReceived(result: DDN.DetectedQuadsResult): void;
```

**Parameters**

`result`: The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```typescript
onNormalizedImagesReceived(result: DDN.NormalizedImagesResult): void;
```

**Parameters**

`result`: The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```typescript
onParsedResultsReceived(result: DCP.ParsedResult): void;
```

**Parameters**

`result`: The parsed result.