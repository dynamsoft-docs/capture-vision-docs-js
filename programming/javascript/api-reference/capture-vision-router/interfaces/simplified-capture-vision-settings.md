---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.20
description: This page introduces the SimplifiedCaptureVisionSettings interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.20.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` interface represents a simplified configuration for the Capture Vision Router settings.

## Definition

```typescript
interface SimplifiedCaptureVisionSettings {
    capturedResultItemTypes: Dynamsoft.Core.EnumCapturedResultItemType;
    roi: Dynamsoft.Core.Quadrilateral;
    roiMeasuredInPercentage: boolean;
    timeout: number;
    barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
    labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
    minImageCaptureInterval: number;
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
| [minImageCaptureInterval](#minimagecaptureinterval) | *number*                                                    |

### capturedResultItemTypes

Specifies the types of captured items to be processed. It uses the EnumCapturedResultItemType enumeration from the Core.BasicStructures namespace.

```typescript
capturedResultItemTypes: Dynamsoft.Core.EnumCapturedResultItemType;
```

**See Also**

* [EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)

### roi

 Represents the region of interest (ROI) as a quadrilateral. It defines the coordinates of the ROI.

```typescript
roi: Dynamsoft.Core.Quadrilateral;
```

**See Also**

* [Quadrilateral]({{ site.dcv_js_api }}core/basic-structures/quadrilateral.html?lang=js)

### roiMeasuredInPercentage

Indicates whether the ROI coordinates are measured in percentage values (true) or absolute pixel values (false).

```typescript
roiMeasuredInPercentage: boolean;
```

### timeout

Specifies the timeout duration (in milliseconds) for processing tasks.

```typescript
timeout: number;
```

### barcodeSettings

Represents the simplified settings for barcode recognition using the SimplifiedBarcodeReaderSettings interface from the DBR namespace.

```typescript
barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
```

**See Also**

* [SimplifiedBarcodeReaderSettings]({{ site.dbr_js_api }}simplified-barcode-reader-settings.html?lang=js)

### labelSettings

Represents the simplified settings for label recognition using the SimplifiedLabelRecognizerSettings interface from the DLR namespace.

```typescript
labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
```

### minImageCaptureInterval

Represents the minimum time interval (in milliseconds) that must elapse before the next image capture operation can be initiated. Setting a larger value for this property will introduce a delay between image captures, while setting a smaller value allows for more frequent captures. It can be used to reduce the computational frequency, which can effectively lower energy consumption.

```typescript
minImageCaptureInterval: number;
```
