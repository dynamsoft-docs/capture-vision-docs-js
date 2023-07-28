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

The `CaptureResultReceiver` interface is responsible for receiving captured results. It contains several callback functions for different types of results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

```typescript
interface CapturedResultReceiver {
  onCapturedResultReceived?(pResult: Core.BasicStructures.CapturedResult): void;
  onRawImageResultReceived?(pResult: RawImageResultItem): void;
  onDecodedBarcodesReceived?(pResult: DBR.DecodedBarcodesResult): void;
  onRecognizedTextLinesReceived?(pResult: DLR.RecognizedTextLinesResult):void;
  onDetectedQuadsReceived?(pResult: DDN.DetectedQuadsResult): void;
  onNormalizedImagesReceived?(pResult: DDN.NormalizedImagesResult): void;
  onParsedResultsReceived?(pResult: DCP.ParsedResult): void;
} 
```


| API Name                                                            | Description                                          |
| ------------------------------------------------------------------- | ---------------------------------------------------- |
| [`OnCapturedResultReceived()`](#oncapturedresultreceived)           | Callback function for all captured results.          |
| [`OnRawImageResultReceived()`](#onrawimageresultreceived)           | Callback function for raw image results.             |
| [`OnDecodedBarcodesReceived()`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived()`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived()`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived()`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived()`](#onparsedresultsreceived)             | Callback function for parsed results.                |

### OnCapturedResultReceived

Callback function for all captured results. It will be called once for each captured result.

```typescript
onCapturedResultReceived(pResult: Core.BasicStructures.CapturedResult): void;
```

**Parameters**

`pResult`: The captured result.

### OnRawImageResultReceived

Callback function for raw image results. It will be called once for each raw image result.

```typescript
onRawImageResultReceived(pResult: RawImageResultItem): void;
```

**Parameters**

`pResult`: The raw image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```typescript
onDecodedBarcodesReceived(pResult: DBR.DecodedBarcodesResult): void;
```

**Parameters**

`pResult`: The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```typescript
onRecognizedTextLinesReceived(pResult: DLR.RecognizedTextLinesResult): void;
```

**Parameters**

`pResult`: The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```typescript
onDetectedQuadsReceived(pResult: DDN.DetectedQuadsResult): void;
```

**Parameters**

`pResult`: The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```typescript
onNormalizedImagesReceived(pResult: DDN.NormalizedImagesResult): void;
```

**Parameters**

`pResult`: The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```typescript
onParsedResultsReceived(pResult: DCP.ParsedResult): void;
```

**Parameters**

`pResult`: The parsed result.