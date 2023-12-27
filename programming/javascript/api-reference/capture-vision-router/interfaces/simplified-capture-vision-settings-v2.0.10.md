---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.10
description: This page introduces the SimplifiedCaptureVisionSettings interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.10.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/javascript/api-reference/capture-vision-router/interface/simplified-capture-vision-settings-v2.0.10.html
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` interface represents a simplified configuration for the Capture Vision Router settings.

```typescript
interface SimplifiedCaptureVisionSettings {
    capturedResultItemTypes: Dynamsoft.Core.EnumCapturedResultItemType;
    roi: Dynamsoft.Core.Quadrilateral;
    roiMeasuredInPercentage: boolean;
    timeout: number;
    barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
    labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
}
```

| Properties                                          | Type                                                        |
| --------------------------------------------------- | ----------------------------------------------------------- |
| [capturedResultItemTypes](#capturedresultitemtypes) | *Dynamsoft.Core.EnumCapturedResultItemType* |
| [roi](#roi)                                         | *Dynamsoft.Core.Quadrilateral*              |
| [roiMeasuredInPercentage](#roimeasuredinpercentage) | *boolean*                                                   |
| [timeout](#timeout)                                 | *number*                                                    |
| [barcodeSettings](#barcodesettings)                 | *Dynamsoft.DBR.SimplifiedBarcodeReaderSettings*             |
| [labelSettings](#labelsettings)                     | *Dynamsoft.DLR.SimplifiedLabelRecognizerSettings*           |

<!-- | [maxParallelTasks](#maxparalleltasks)               | *number*                                                    | -->

## capturedResultItemTypes

Specifies the types of captured items to be processed. It uses the EnumCapturedResultItemType enumeration from the Core.BasicStructures namespace.

```typescript
capturedResultItemTypes: Dynamsoft.Core.EnumCapturedResultItemType;
```

**See Also**

* [EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)

## roi

 Represents the region of interest (ROI) as a quadrilateral. It defines the coordinates of the ROI.

```typescript
roi: Dynamsoft.Core.Quadrilateral;
```

## roiMeasuredInPercentage

Indicates whether the ROI coordinates are measured in percentage values (true) or absolute pixel values (false).

```typescript
roiMeasuredInPercentage: boolean;
```

<!-- ## maxParallelTasks

Specifies the maximum number of parallel tasks allowed during processing.

```typescript
maxParallelTasks: number;
``` -->

## timeout

Specifies the timeout duration for processing tasks.

```typescript
timeout: number;
```

## barcodeSettings

Represents the simplified settings for barcode recognition using the SimplifiedBarcodeReaderSettings interface from the DBR namespace.

```typescript
barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
```

## labelSettings

Represents the simplified settings for label recognition using the SimplifiedLabelRecognizerSettings interface from the DLR namespace.

```typescript
labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
```