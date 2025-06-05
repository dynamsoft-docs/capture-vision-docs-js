---
layout: default-layout
title: Interface SimplifiedCaptureVisionSettings - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the SimplifiedCaptureVisionSettings interface in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: capture vision, router, Intermediate-result, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# SimplifiedCaptureVisionSettings

The `SimplifiedCaptureVisionSettings` interface provides a standardized way to adjust a select set of settings for a given `CaptureVisionTemplate`.

```typescript
interface SimplifiedCaptureVisionSettings {
    outputOriginalImage: boolean;
    barcodeSettings: SimplifiedBarcodeReaderSettings;
    documentSettings: SimplifiedDocumentNormalizerSettings;
    labelSettings: SimplifiedLabelRecognizerSettings;
    minImageCaptureInterval: number;
    roi: Quadrilateral;
    roiMeasuredInPercentage: boolean;
}
```

## outputOriginalImage

Specifies whether to output the original image.

```typescript
outputOriginalImage: boolean;
```

## barcodeSettings

Specifies the basic settings for the barcode reader module. It is of type `SimplifiedBarcodeReaderSettings`.

```typescript
barcodeSettings: SimplifiedBarcodeReaderSettings;
```

**See Also**

[SimplifiedBarcodeReaderSettings](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/simplified-barcode-reader-settings.html)

## documentSettings

Specifies the basic settings for the document normalizer module. It is of type `SimplifiedDocumentNormalizerSettings`.

```typescript
documentSettings: SimplifiedDocumentNormalizerSettings;
```

**See Also**

[SimplifiedDocumentNormalizerSettings](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/simplified-document-normalizer-settings.html)

## labelSettings

Specifies the basic settings for the label recognizer module. It is of type `SimplifiedLabelRecognizerSettings`.

```typescript
labelSettings: Dynamsoft.DLR.SimplifiedLabelRecognizerSettings;
```

**See Also**

[SimplifiedLabelRecognizerSettings](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/simplified-label-recognizer-settings.html?lang=js)

## minImageCaptureInterval

Specifies the shortest time span, in milliseconds, that must elapse between two successive image captures. Opting for a higher interval decreases capture frequency, which can lower the system's processing load and conserve energy. On the other hand, a smaller interval value increases the frequency of image captures, enhancing the system's responsiveness.

> Handling of Special Values:
>
> -1: This value ensures the image source waits until processing of the current image is complete before starting to acquire the next one. This approach ensures there is a deliberate pause between processing consecutive images.
>
> 0 (The default setting): Adopting this value means the image source queues up the next image for immediate availability once processing of the current image is finished, facilitating continuous, uninterrupted image processing.

```typescript
minImageCaptureInterval: number;
```

## roi

Designates the region of interest (ROI) within an image, limiting the image processing activities exclusively to this specified area. It is of type `Quadrilateral`.

```typescript
roi: Quadrilateral;
```

**See Also**

[Quadrilateral]({{ site.dcvb_js_api }}core/basic-structures/quadrilateral.html?lang=js)

## roiMeasuredInPercentage

Determines if the coordinates for the region of interest (ROI) are expressed in percentage terms (true) or as exact pixel measurements (false).

```typescript
roiMeasuredInPercentage: boolean;
```
