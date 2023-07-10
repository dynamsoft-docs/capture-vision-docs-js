---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces interface related to the SimplifiedCaptureVisionSettings of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
---

# Javascript API Reference - SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` interface represents a simplified configuration for the Capture Vision Router settings.

```ts
export interface SimplifiedCaptureVisionSettings {
            capturedResultItemTypes: Core.BasicStructures.EnumCapturedResultItemType;
            roi: Core.BasicStructures.Quadrilateral;
            roiMeasuredInPercentage: boolean;
            maxParallelTasks: number;
            timeout: number;
            barcodeSettings: DBR.SimplifiedBarcodeReaderSettings;
            labelSettings: DLR.SimplifiedLabelRecognizerSettings;
        }
```

## Attributes Summary

| Attribute                                                     | Type                                                       |
| ------------------------------------------------------------- | ---------------------------------------------------------- |
| [capturedResultItemTypes](#capturedresultitemtypes)           | *Core.BasicStructures.EnumCapturedResultItemType*          |
| [roi](#roi)                                                   | *Core.BasicStructures.Quadrilateral*                       |
| [roiMeasuredInPercentage](#roimeasuredinpercentage)           | *Boolean*                                                  |
| [maxParallelTasks](#maxparalleltasks)                         | *Number*                                                   |
| [timeout](#timeout)                                           | *Number*                                                   |
| [barcodeSettings](#barcodesettings)                           | *DBR.SimplifiedBarcodeReaderSettings*                      |
| [labelSettings](#labelsettings)                               | *DLR.SimplifiedLabelRecognizerSettings*                    |

## capturedResultItemTypes

Specifies the types of captured items to be processed. It uses the EnumCapturedResultItemType enumeration from the Core.BasicStructures namespace.

```ts
capturedResultItemTypes: Core.BasicStructures.EnumCapturedResultItemType;
```

## roi

 Represents the region of interest (ROI) as a quadrilateral. It defines the coordinates of the ROI.

```ts
roi: Core.BasicStructures.Quadrilateral;
```

## roiMeasuredInPercentage

Indicates whether the ROI coordinates are measured in percentage values (true) or absolute pixel values (false).

```ts
roiMeasuredInPercentage: boolean;
```

## maxParallelTasks

Specifies the maximum number of parallel tasks allowed during processing.

```ts
maxParallelTasks: number;
```

## timeout

Specifies the timeout duration for processing tasks.

```ts
timeout: number;
```

## barcodeSettings

Represents the simplified settings for barcode recognition using the SimplifiedBarcodeReaderSettings interface from the DBR namespace.

```ts
barcodeSettings: DBR.SimplifiedBarcodeReaderSettings;
```

## labelSettings

Represents the simplified settings for label recognition using the SimplifiedLabelRecognizerSettings interface from the DLR namespace.

```ts
labelSettings: DLR.SimplifiedLabelRecognizerSettings;
```