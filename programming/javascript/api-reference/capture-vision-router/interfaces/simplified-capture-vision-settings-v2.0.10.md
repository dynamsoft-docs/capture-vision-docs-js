---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces interface related to the SimplifiedCaptureVisionSettings of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/javascript/api-reference/capture-vision-router/interface/simplified-capture-vision-settings-v2.0.10.html
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` interface represents a simplified configuration for the Capture Vision Router settings.

## Definition

```typescript
interface SimplifiedCaptureVisionSettings {
    capturedResultItemTypes: Dynamsoft.Core.BasicStructures.EnumCapturedResultItemType;
    roi: Dynamsoft.Core.BasicStructures.Quadrilateral;
    roiMeasuredInPercentage: boolean;
    maxParallelTasks: number;
    timeout: number;
    barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
    labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
}
```

| Properties                                          | Type                                                        |
| --------------------------------------------------- | ----------------------------------------------------------- |
| [capturedResultItemTypes](#capturedresultitemtypes) | *Dynamsoft.Core.BasicStructures.EnumCapturedResultItemType* |
| [roi](#roi)                                         | *Dynamsoft.Core.BasicStructures.Quadrilateral*              |
| [roiMeasuredInPercentage](#roimeasuredinpercentage) | *boolean*                                                   |
| [maxParallelTasks](#maxparalleltasks)               | *number*                                                    |
| [timeout](#timeout)                                 | *number*                                                    |
| [barcodeSettings](#barcodesettings)                 | *Dynamsoft.DBR.SimplifiedBarcodeReaderSettings*             |
| [labelSettings](#labelsettings)                     | *Dynamsoft.DLR.SimplifiedLabelRecognizerSettings*           |

### capturedResultItemTypes

Specifies the types of captured items to be processed. It uses the EnumCapturedResultItemType enumeration from the Core.BasicStructures namespace.

```typescript
capturedResultItemTypes: Dynamsoft.Core.BasicStructures.EnumCapturedResultItemType;
```

**See Also**

* [EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)

## roi

 Represents the region of interest (ROI) as a quadrilateral. It defines the coordinates of the ROI.

```typescript
roi: Dynamsoft.Core.BasicStructures.Quadrilateral;
```

### roiMeasuredInPercentage

Indicates whether the ROI coordinates are measured in percentage values (true) or absolute pixel values (false).

```typescript
roiMeasuredInPercentage: boolean;
```

### maxParallelTasks

Specifies the maximum number of parallel tasks allowed during processing.

```typescript
maxParallelTasks: number;
```

### timeout

Specifies the timeout duration for processing tasks.

```typescript
timeout: number;
```

### barcodeSettings

Represents the simplified settings for barcode recognition using the SimplifiedBarcodeReaderSettings interface from the DBR namespace.

```typescript
barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
```

### labelSettings

Represents the simplified settings for label recognition using the SimplifiedLabelRecognizerSettings interface from the DLR namespace.

```typescript
labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
```