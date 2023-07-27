---
layout: default-layout
title: interface CaptureResultFilter - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface CaptureResultFilter in Core Module.
keywords: captured result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS CaptureResultFilter Interface
---

# CaptureResultFilter

The `CaptureResultFilter` interface contains several callback functions for different types of results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

```typescript
interface CapturedResultFilter {
  onRawImageResultReceived: (result: Core.BasicStructures.RawImageResultItem) => void;
  onDecodedBarcodesReceived: (result: DBR.DecodedBarcodesResult) => void;
  onRecognizedTextLinesReceived: (result: DLR.RecognizedTextLinesResult) => void;
  onDetectedQuadsReceived: (result: DDN.DetectedQuadsResult) => void;
  onNormalizedImagesReceived: (result: DDN.NormalizedImagesResult) => void;
  onParsedResultsReceived: (result: DCP.ParsedResult) => void;
} 
```

| API Name                                                            | Description                                          |
| ----------------------------------------------------------------- | ---------------------------------------------------- |
| [`OnRawImageResultReceived`](#onrawimageresultreceived)           | Callback function for raw image results.             |
| [`OnDecodedBarcodesReceived`](#ondecodedbarcodesreceived)         | Callback function for decoded barcodes results.      |
| [`OnRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback function for recognized text lines results. |
| [`OnDetectedQuadsReceived`](#ondetectedquadsreceived)             | Callback function for detected quads results.        |
| [`OnNormalizedImagesReceived`](#onnormalizedimagesreceived)       | Callback function for normalized images results.     |
| [`OnParsedResultsReceived`](#onparsedresultsreceived)             | Callback function for parsed results.                |

### OnRawImageResultReceived

Callback function for raw image results. It will be called once for each raw image result.

```typescript
onRawImageResultReceived: (result: Core.BasicStructures.RawImageResultItem) => void;
```

**Parameters**

`result`: The raw image result.

### OnDecodedBarcodesReceived

Callback function for decoded barcodes results. It will be called once for each decoded barcodes result.

```typescript
onDecodedBarcodesReceived: (result: DBR.DecodedBarcodesResult) => void;
```

**Parameters**

`result`: The decoded barcodes result.

### OnRecognizedTextLinesReceived

Callback function for recognized text lines results. It will be called once for each recognized text lines result.

```typescript
onRecognizedTextLinesReceived: (result: DLR.RecognizedTextLinesResult) => void;
```

**Parameters**

`result`: The recognized text lines result.

### OnDetectedQuadsReceived

Callback function for detected quads results. It will be called once for each detected quads result.

```typescript
onDetectedQuadsReceived: (result: DDN.DetectedQuadsResult) => void;
```

**Parameters**

`result`: The detected quads result.

### OnNormalizedImagesReceived

Callback function for normalized images results. It will be called once for each normalized images result.

```typescript
onNormalizedImagesReceived: (result: DDN.NormalizedImagesResult) => void;
```

**Parameters**

`result`: The normalized images result.

### OnParsedResultsReceived

Callback function for parsed results. It will be called once for each parsed result.

```typescript
onParsedResultsReceived: (result: DCP.ParsedResult) => void;
```

**Parameters**

`result`: The parsed result.