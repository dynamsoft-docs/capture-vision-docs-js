---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft CaptureVisionRouter Module JS Edition API Reference v2.0.30
description: This page introduces the SimplifiedCaptureVisionSettings interface in Dynamsoft CaptureVisionRouter Module JS Edition v2.0.30.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
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
    minImageCaptureInterval: number;
}
```

| Properties                                          | Type                                              |
| --------------------------------------------------- | ------------------------------------------------- |
| [capturedResultItemTypes](#capturedresultitemtypes) | *Dynamsoft.Core.EnumCapturedResultItemType*       |
| [roi](#roi)                                         | *Dynamsoft.Core.Quadrilateral*                    |
| [roiMeasuredInPercentage](#roimeasuredinpercentage) | *boolean*                                         |
| [timeout](#timeout)                                 | *number*                                          |
| [barcodeSettings](#barcodesettings)                 | *Dynamsoft.DBR.SimplifiedBarcodeReaderSettings*   |
| [labelSettings](#labelsettings)                     | *Dynamsoft.DLR.SimplifiedLabelRecognizerSettings* |
| [minImageCaptureInterval](#minimagecaptureinterval) | *number*                                          |

## capturedResultItemTypes

Defines the types of items that are expected to be obtained through the capture process.

```typescript
capturedResultItemTypes: Dynamsoft.Core.EnumCapturedResultItemType;
```

**See Also**

* [EnumCapturedResultItemType]({{ site.enums }}core/captured-result-item-type.html?lang=js)

## roi

Specifies the specific area (known as region of interest, or roi) within the images that will be targeted by the capture process.

```typescript
roi: Dynamsoft.Core.Quadrilateral;
```

**See Also**

* [Quadrilateral]({{ site.dcv_js_api }}core/basic-structures/quadrilateral.html?lang=js)

## roiMeasuredInPercentage

Specifies if the coordinates of the region of interest (roi) are represented as percentage values (true) or as absolute pixel values (false).

```typescript
roiMeasuredInPercentage: boolean;
```

## timeout

Defines the maximum duration (in milliseconds) permitted for processing each individual image.

```typescript
timeout: number;
```

## barcodeSettings

Specifies the basic configuration for barcode scanning as defined by the `SimplifiedBarcodeReaderSettings` interface.

```typescript
barcodeSettings: Dynamsoft.DBR.SimplifiedBarcodeReaderSettings;
```

**See Also**

* [SimplifiedBarcodeReaderSettings]({{ site.dbr_js_api }}simplified-barcode-reader-settings.html?lang=js)

## labelSettings

Specifies the basic configuration for label recognition as defined by the `SimplifiedLabelRecognizerSettings` interface.

```typescript
labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
```

## minImageCaptureInterval

Defines the minimum time interval in milliseconds that controls the time gap between consecutive image captures. It's a crucial parameter for managing the balance between capture frequency and computational load. Here's how it works:

1. **Adjustable Time Interval**: The value of `minImageCaptureInterval` dictates the minimum duration that should pass before another image capture can occur. A higher value means less frequent captures, leading to reduced computational demands and energy usage. Conversely, a lower value allows for more rapid image capturing.

2. **Special Values and Their Functions**:

    * -1: Setting this value indicates that the image source should wait until the `CaptureVisionRouter` object has completely processed the current image before capturing the next one. This ensures there's a processing break between two successive images.
    * 0 (Default Setting): This value signifies that the image source should prepare the next image for capture immediately. As soon as the `CaptureVisionRouter` finishes processing an image, it can straightaway start with the next, ensuring no delay in processing.

```typescript
minImageCaptureInterval: number;
```
