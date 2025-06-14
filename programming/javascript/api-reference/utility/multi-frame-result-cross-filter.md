---
layout: default-layout
title: Interface MultiFrameResultCrossFilter - Dynamsoft Utility Module JS Edition API Reference
description: This page shows the JS edition of the class MultiFrameResultCrossFilter in Dynamsoft Utility Module.
keywords: image manager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class offers a set of API functions designed for managing and filtering results from multiple image frames, typically used in consecutive frames of a streaming video.

| Name                                                                    | Description                                                                                  |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [enableLatestOverlapping()](#enablelatestoverlapping)                   | Enables or disables the to-the-latest overlapping feature of one or multiple specific result item types. This feature can increase the read-rate performance when decoding multiple barcodes under the video streaming. |
| [isLatestOverlappingEnabled()](#islatestoverlappingenabled)             | Checks if to-the-latest overlapping is active for a given result item type.                  |
| [enableResultCrossVerification()](#enableresultcrossverification)       | Enables or disables the verification of specific result item types.                          |
| [isResultCrossVerificationEnabled()](#isresultcrossverificationenabled) | Checks if verification is active for a given result item type.                               |
| [enableResultDeduplication()](#enableresultdeduplication)               | Enables or disables the deduplication process for specific result item types.                |
| [isResultDeduplicationEnabled()](#isresultdeduplicationenabled)         | Checks if deduplication is active for a given result item type.                              |
| [setDuplicateForgetTime()](#setduplicateforgettime)                     | Sets the interval during which duplicates are disregarded for specific result item types.    |
| [getDuplicateForgetTime()](#getduplicateforgettime)                     | Retrieves the interval during which duplicates are disregarded for a given result item type. |
| [setMaxOverlappingFrames()](#setmaxoverlappingframes)                   | Set the maximum overlapping frames count for a given result item type.                       |
| [getMaxOverlappingFrames()](#getmaxoverlappingframes)                   | Get the maximum overlapping frames count for a given result item type.                       |
| [onOriginalImageResultReceived()](#onoriginalimageresultreceived)       | Event triggered when the original images are received.                                       |
| [onDecodedBarcodesReceived()](#ondecodedbarcodesreceived)               | Event triggered when the decoded barcodes are received.                                      |
| [onRecognizedTextLinesReceived()](#onrecognizedtextlinesreceived)       | Event triggered when the recognized text lines are received.                                 |
| [onProcessedDocumentResultReceived()](#onprocesseddocumentresultreceived)                   | Event triggered when the processed documents are received.                               |

### enableLatestOverlapping

Enables or disables the latest overlapping of specific result item types.

> Please note that this feature is currently only available for barcodes reading.

```typescript
enableLatestOverlapping(resultItemTypes: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image", enabled: boolean): void;
```

**Parameters**

`resultItemTypes`: Specifies the result item types.

`enabled`: Boolean to toggle the latest overlapping on or off.

**Return Value**

None.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### isLatestOverlappingEnabled

Checks if latest overlapping is active for a given result item type.

```typescript
isLatestOverlappingEnabled(resultItemType: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image"): boolean;
```

**Parameters**

`resultItemType`:  Specifies the result item type in question.

**Return Value**

Boolean indicating the status of the latest overlapping for the specified type.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### enableResultCrossVerification

Enables or disables the verification of specific result item types.

```typescript
enableResultCrossVerification(resultItemTypes: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image", enabled: boolean): void;
```

**Parameters**

`resultItemTypes`: Specifies the result item types.

`enabled`: Boolean to toggle verification on or off.

**Return Value**

None.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### isResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

```typescript
isResultCrossVerificationEnabled(resultItemType: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image"): boolean;
```

**Parameters**

`resultItemType`:  Specifies the result item type in question.

**Return Value**

Boolean indicating the status of verification for the specified type.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### enableResultDeduplication

Enables or disables the deduplication process for specific result item types.

```typescript
enableResultDeduplication(resultItemTypes: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image", enabled: boolean): void;
```

**Parameters**

`resultItemTypes`: Specifies the result item types.

`enabled`: Boolean to toggle deduplication on or off.

**Return Value**

None.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### isResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

```typescript
isResultDeduplicationEnabled(resultItemType: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image"): boolean;
```

**Parameters**

`resultItemType`:  Specifies the result item type in question.

**Return Value**

Boolean indicating the deduplication status for the specified type.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### setDuplicateForgetTime

Sets the interval during which duplicates are disregarded for specific result item types.

```typescript
setDuplicateForgetTime(resultItemTypes: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image", time: number): void;
```

**Parameters**

`resultItemTypes`: Specifies the result item types.

`time`: Time in milliseconds during which duplicates are disregarded. The maximum time allowed is 10,000 milliseconds or 10 seconds.

**Return Value**

None.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### getDuplicateForgetTime

Retrieves the interval during which duplicates are disregarded for a given result item type.

```typescript
getDuplicateForgetTime(resultItemType: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image"): number;
```

**Parameters**

`resultItemType`: Specifies the result item type in question.

**Return Value**

The set interval for the specified item type.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### setMaxOverlappingFrames

Set the maximum overlapping frames count for a given result item type.

```typescript
setMaxOverlappingFrames(resultItemTypes: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image", maxOverlappingFrames: number): void;
```

**Parameters**

`resultItemTypes`: Specifies the result item types.

`maxOverlappingFrames`: The maximum overlapping frame count for the overlapping.

**Return Value**

None.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### getMaxOverlappingFrames

Get the maximum overlapping frames count for a given result item type.

```typescript
getMaxOverlappingFrames(resultItemType: Core.EnumCapturedResultItemType | "barcode" | "text_line" | "detected_quad" | "normalized_image"): number;
```

**Parameters**

`resultItemType`: Specifies the result item type in question.

**Return Value**

The maximum overlapping frame count for the overlapping.

**See Also**

[EnumCapturedResultItemType](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/captured-result-item-type.html?lang=js)

### onOriginalImageResultReceived

Event triggered when the original images are received.

```typescript
onOriginalImageResultReceived?: (result: Core.OriginalImageResultItem) => void;
```

**Parameters**

`result`: The result item that contains the original image, of type `OriginalImageResultItem`.

**Return Value**

None.

### onDecodedBarcodesReceived

Event triggered when the decoded barcodes are received.

```typescript
onDecodedBarcodesReceived?: (result: any) => void;
```

**Parameters**

`result`: The result item that contains the decoded barcodes, of type `any`.

**Return Value**

None.

### onRecognizedTextLinesReceived

Event triggered when the recognized text lines are received.

```typescript
onRecognizedTextLinesReceived?: (result: any) => void;
```

**Parameters**

`result`: The result item that contains the recognized text lines, of type `any`.

**Return Value**

None.

### onProcessedDocumentResultReceived

Event triggered when the processed documents are received.

```typescript
onProcessedDocumentResultReceived?: (result: any) => void;
```

**Parameters**

`result`: The result item that contains the processed documents, of type `any`.

**Return Value**

None.