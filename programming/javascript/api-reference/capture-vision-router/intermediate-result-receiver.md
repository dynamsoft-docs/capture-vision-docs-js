---
layout: default-layout
title: Class IntermediateResultReceiver - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the IntermediateResultReceiver Class in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: intermediate result receiver, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` class is designed as a standardized way for retrieving intermediate results in image processing workflows in the Dynamsoft Capture Vision architecture. It adopts an event-driven approach, with events triggered for specific types of results, such as pre-detected regions, localized barcodes, etc. Each event is optional, allowing flexibility and customization based on the needs of the application.

```typescript
class IntermediateResultReceiver {
    getObservationParameters(): Core.ObservationParameters;
    onTaskResultsReceived?(result: IntermediateResult, info: IntermediateResultExtraInfo): void;
    onPredetectedRegionsReceived?(result: PredetectedRegionsUnit, info: IntermediateResultExtraInfo): void;
    onLocalizedBarcodesReceived?(result: LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
    onDecodedBarcodesReceived?(result: DecodedBarcodesUnit, info: IntermediateResultExtraInfo): void;
    onLocalizedTextLinesReceived?(result: LocalizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
    onRecognizedTextLinesReceived?(result: RecognizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
    onDetectedQuadsReceived?(result: DetectedQuadsUnit, info: IntermediateResultExtraInfo): void;
    onDeskewedImageReceived?(result: DeskewedImageUnit, info: IntermediateResultExtraInfo): void;
    onColourImageUnitReceived?(result: ColourImageUnit, info: IntermediateResultExtraInfo): void;
    onScaledColourImageUnitReceived?(result: ScaledColourImageUnit, info: IntermediateResultExtraInfo): void;
    onGrayscaleImageUnitReceived?(result: GrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
    onTransformedGrayscaleImageUnitReceived?(result: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
    onEnhancedGrayscaleImageUnitReceived?(result: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
    onBinaryImageUnitReceived?(result: BinaryImageUnit, info: IntermediateResultExtraInfo): void;
    onTextureDetectionResultUnitReceived?(result: TextureDetectionResultUnit, info: IntermediateResultExtraInfo): void;
    onTextureRemovedGrayscaleImageUnitReceived?(result: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
    onTextureRemovedBinaryImageUnitReceived?(result: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
    onContoursUnitReceived?(result: ContoursUnit, info: IntermediateResultExtraInfo): void;
    onLineSegmentsUnitReceived?(result: LineSegmentsUnit, info: IntermediateResultExtraInfo): void;
    onTextZonesUnitReceived?(result: TextZonesUnit, info: IntermediateResultExtraInfo): void;
    onTextRemovedBinaryImageUnitReceived?(result: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
    onShortLinesUnitReceived?(result: Core.ShortLinesUnit, info: Core.IntermediateResultExtraInfo): void;
    onLongLinesUnitReceived?(result: LongLinesUnit, info: IntermediateResultExtraInfo): void;
    onCornersUnitReceived?(result: CornersUnit, info: IntermediateResultExtraInfo): void;
    onCandidateQuadEdgesUnitReceived?(result: CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo): void;
    onCandidateBarcodeZonesUnitReceived?(result: LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
    onScaledBarcodeImageUnitReceived?(result: ScaledUpBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
    onDeformationResistedBarcodeImageUnitReceived?(result: DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
    onComplementedBarcodeImageUnitReceived?(result: ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
    OnRawTextLinesUnitReceived?(result: RawTextLinesUnit, info: IntermediateResultExtraInfo): void;
    onLogicLinesUnitReceived?(result: LogicLinesUnit, info: IntermediateResultExtraInfo): void;
    onEnhancedImageReceived?(result: EnhancedImageUnit, info: IntermediateResultExtraInfo): void;
    OnTargetROIResultsReceived?(result: IntermediateResultUnit, info: IntermediateResultExtraInfo): void;
}
```

| Name                                                                                              | Description                                                                 |
| ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [getObservationParameters()](#getobservationparameters)                                           | Gets the observed parameters of the intermediate result receiver.           |
| [onTaskResultsReceived()](#ontaskresultsreceived)                                                 | Event triggered when task results are received.                             |
| [onPredetectedRegionsReceived()](#onpredetectedregionsreceived)                                   | Event triggered when pre-detected regions are received.                     |
| [onLocalizedBarcodesReceived()](#onlocalizedbarcodesreceived)                                     | Event triggered when localized barcodes are received.                       |
| [onDecodedBarcodesReceived()](#ondecodedbarcodesreceived)                                         | Event triggered when decoded barcodes are received.                         |
| [onLocalizedTextLinesReceived()](#onlocalizedtextlinesreceived)                                   | Event triggered when localized text lines are received.                     |
| [onRecognizedTextLinesReceived()](#onrecognizedtextlinesreceived)                                 | Event triggered when recognized text lines are received.                    |
| [onDetectedQuadsReceived()](#ondetectedquadsreceived)                                             | Event triggered when detected quads are received.                           |
| [onDeskewedImageReceived()](#ondeskewedimagereceived)                                             | Event triggered when deskewed image is received.                          |
| [onColourImageUnitReceived()](#oncolourimageunitreceived)                                         | Event triggered when a colour image unit is received.                       |
| [onScaledColourImageUnitReceived()](#onscaledcolourimageunitreceived)                             | Event triggered when a scaled colour image unit is received.           |
| [onGrayscaleImageUnitReceived()](#ongrayscaleimageunitreceived)                                   | Event triggered when a grayscale image unit is received.                    |
| [onTransformedGrayscaleImageUnitReceived()](#ontransformedgrayscaleimageunitreceived)             | Event triggered when a transformed grayscale image unit is received.        |
| [onEnhancedGrayscaleImageUnitReceived()](#onenhancedgrayscaleimageunitreceived)                   | Event triggered when an enhanced grayscale image unit is received.          |
| [onBinaryImageUnitReceived()](#onbinaryimageunitreceived)                                         | Event triggered when a binary image unit is received.                       |
| [onTextureDetectionResultUnitReceived()](#ontexturedetectionresultunitreceived)                   | Event triggered when a texture detection result unit is received.           |
| [onTextureRemovedGrayscaleImageUnitReceived()](#ontextureremovedgrayscaleimageunitreceived)       | Event triggered when a texture-removed grayscale image unit is received.    |
| [onTextureRemovedBinaryImageUnitReceived()](#ontextureremovedbinaryimageunitreceived)             | Event triggered when a texture-removed binary image unit is received.       |
| [onContoursUnitReceived()](#oncontoursunitreceived)                                               | Event triggered when a contours unit is received.                           |
| [onLineSegmentsUnitReceived()](#onlinesegmentsunitreceived)                                       | Event triggered when a line segments unit is received.                      |
| [onTextZonesUnitReceived()](#ontextzonesunitreceived)                                             | Event triggered when a text zones unit is received.                         |
| [onTextRemovedBinaryImageUnitReceived()](#ontextremovedbinaryimageunitreceived)                   | Event triggered when a text-removed binary image unit is received.          |
| [onShortLinesUnitReceived()](#onshortlinesunitreceived)                                           | Event triggered when a short lines unit is received.                        |
| [onLongLinesUnitReceived()](#onlonglinesunitreceived)                                             | Event triggered when a long lines unit is received.                         |
| [onCornersUnitReceived()](#oncornersunitreceived)                                                 | Event triggered when a corners unit is received.                            |
| [onCandidateQuadEdgesUnitReceived()](#oncandidatequadedgesunitreceived)                           | Event triggered when a candidate quad edges unit are detected.              |
| [onCandidateBarcodeZonesUnitReceived()](#oncandidatebarcodezonesunitreceived)                     | Event triggered when a candidate barcode zones unit are detected.           |
| [onScaledBarcodeImageUnitReceived()](#onscaledbarcodeimageunitreceived)                           | Event triggered when a scaled-up barcode image unit is received.            |
| [onDeformationResistedBarcodeImageUnitReceived()](#ondeformationresistedbarcodeimageunitreceived) | Event triggered when a deformation-resisted barcode image unit is received. |
| [onComplementedBarcodeImageUnitReceived()](#oncomplementedbarcodeimageunitreceived)               | Event triggered when a complemented barcode image unit is received.         |
| [OnRawTextLinesUnitReceived()](#onrawtextlinesunitreceived)                                       | Event triggered when a raw text line unit is received.                      |
| [onLogicLinesUnitReceived()](#onlogiclinesunitreceived)                                           | Event triggered when a logic line unit is received.                         |
| [onEnhancedImageReceived()](#onenhancedimagereceived)                                             | Event triggered when enhanced image is received.                          |
| [OnTargetROIResultsReceived()](#ontargetroiresultsreceived)                                       | Event triggered when all tasks for the target ROI are completed and the results are deduplicated.         |

## getObservationParameters

Gets the observed parameters of the intermediate result receiver. Allowing for configuration of intermediate result observation.

```typescript
getObservationParameters(): ObservationParameters;
```

**Return Value**

The observed parameters, of type `ObservationParameters`. The default parameters are to observe all intermediate result unit types and all tasks.

**See Also**

[ObservationParameters](../core/intermediate-results/observation-parameters.md)

## onTaskResultsReceived

Event triggered when task results are received. 

```typescript
onTaskResultsReceived?(result: IntermediateResult, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The intermediate result from the task, of type `IntermediateResult`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[IntermediateResult](../core/intermediate-results/intermediate-result.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

[Image-Processing Tasks](https://www.dynamsoft.com/capture-vision/docs/core/architecture/image-processing/index.html)

## onPredetectedRegionsReceived

Event triggered when pre-detected regions are received.

```typescript
onPredetectedRegionsReceived?(result: PredetectedRegionsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the pre-detected regions, of type `PredetectedRegionsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[PredetectedRegionsUnit](../core/intermediate-results/predetected-regions-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onLocalizedBarcodesReceived

Event triggered when localized barcodes are received.

```typescript
onLocalizedBarcodesReceived?(result: LocalizedBarcodesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the localized barcodes, of type `LocalizedBarcodesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[LocalizedBarcodesUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/localized-barcodes-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onDecodedBarcodesReceived

Event triggered when decoded barcodes are received.

```typescript
onDecodedBarcodesReceived?(result: DecodedBarcodesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the decoded barcodes, of type `DecodedBarcodesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[DecodedBarcodesUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/decoded-barcodes-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onLocalizedTextLinesReceived

Event triggered when localized text lines are received.

```typescript
onLocalizedTextLinesReceived?(result: LocalizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the localized text lines, of type `LocalizedTextLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[LocalizedTextLinesUnit](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/localized-textlines-unit.html?lang=js)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onRecognizedTextLinesReceived

Event triggered when recognized text lines are received.

```typescript
onRecognizedTextLinesReceived?(result: RecognizedTextLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the recognized text lines, of type `RecognizedTextLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[RecognizedTextLinesUnit](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/recognized-textlines-unit.html?lang=js)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onDetectedQuadsReceived

Event triggered when detected quads are received.

```typescript
onDetectedQuadsReceived?(result: DetectedQuadsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the detected quads, of type `DetectedQuadsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[DetectedQuadsUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/detected-quads-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onDeskewedImageReceived

Event triggered when deskewed image is received.

```typescript
onDeskewedImageReceived?(result: DeskewedImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the deskewed image, of type `DeskewedImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[DeskewedImageUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/deskewed-image-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onColourImageUnitReceived

Event triggered when a colour image unit is received.

```typescript
onColourImageUnitReceived?(result: ColourImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the colour image, of type `ColourImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ColourImageUnit](../core/intermediate-results/colour-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onScaledColourImageUnitReceived

Event triggered when a scaled colour image unit is received.

```typescript
onScaledColourImageUnitReceived?(result: ScaledColourImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the scaled colour image, of type `ScaledColourImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ScaledDownColourImageUnit](../core/intermediate-results/scaled-colour-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onGrayscaleImageUnitReceived

Event triggered when a grayscale image unit is received.

```typescript
onGrayscaleImageUnitReceived?(result: GrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the grayscale image, of type `GrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[GrayscaleImageUnit](../core/intermediate-results/grayscale-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTransformedGrayscaleImageUnitReceived

Event triggered when a transformed grayscale image unit is received.

```typescript
onTransformedGrayscaleImageUnitReceived?(result: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the transformed grayscale image, of type `TransformedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TransformedGrayscaleImageUnit](../core/intermediate-results/transformed-grayscale-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onEnhancedGrayscaleImageUnitReceived

Event triggered when an enhanced grayscale image unit is received.

```typescript
onEnhancedGrayscaleImageUnitReceived?(result: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the enhanced grayscale image, of type `EnhancedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[EnhancedGrayscaleImageUnit](../core/intermediate-results/enhanced-grayscale-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onBinaryImageUnitReceived

Event triggered when a binary image unit is received.

```typescript
onBinaryImageUnitReceived?(result: BinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the binary image, of type `BinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[BinaryImageUnit](../core/intermediate-results/binary-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTextureDetectionResultUnitReceived

Event triggered when a texture detection result unit is received.

```typescript
onTextureDetectionResultUnitReceived?(result: TextureDetectionResultUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the texture detection result, of type `TextureDetectionResultUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TextureDetectionResultUnit](../core/intermediate-results/texture-detection-result-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTextureRemovedGrayscaleImageUnitReceived

Event triggered when a texture-removed grayscale image unit is received.

```typescript
onTextureRemovedGrayscaleImageUnitReceived?(result: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the texture-removed grayscale image, of type `TextureRemovedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TextureRemovedGrayscaleImageUnit](../core/intermediate-results/texture-removed-grayscale-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTextureRemovedBinaryImageUnitReceived

Event triggered when a texture-removed binary image unit is received.

```typescript
onTextureRemovedBinaryImageUnitReceived?(result: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the texture-removed binary image, of type `TextureRemovedBinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TextureRemovedBinaryImageUnit](../core/intermediate-results/texture-removed-binary-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onContoursUnitReceived

Event triggered when a contours unit is received.

```typescript
onContoursUnitReceived?(result: ContoursUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the contours, of type `ContoursUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ContoursUnit](../core/intermediate-results/contours-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onLineSegmentsUnitReceived

Event triggered when a line segments unit is received.

```typescript
onLineSegmentsUnitReceived?(result: LineSegmentsUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the line segments, of type `LineSegmentsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[LineSegmentsUnit](../core/intermediate-results/line-segments-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTextZonesUnitReceived

Event triggered when a text zones unit is received.

```typescript
onTextZonesUnitReceived?(result: TextZonesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the text zones, of type `TextZonesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TextZonesUnit](../core/intermediate-results/text-zones-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onTextRemovedBinaryImageUnitReceived

Event triggered when a text-removed binary image unit is received.

```typescript
onTextRemovedBinaryImageUnitReceived?(result: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the text-removed binary image, of type `TextRemovedBinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[TextRemovedBinaryImageUnit](../core/intermediate-results/text-removed-binary-image-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onShortLinesUnitReceived

Event triggered when a short lines unit is received.

```typescript
onShortLinesUnitReceived?(result: ShortLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the short lines, of type `ShortLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ShortLinesUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/short-lines-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onLongLinesUnitReceived

Event triggered when a long lines unit is received.

```typescript
onLongLinesUnitReceived?(result: LongLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the long lines, of type `LongLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[LongLinesUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/long-lines-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onCornersUnitReceived

Event triggered when a corners unit is received.

```typescript
onCornersUnitReceived?(result: CornersUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the corners, of type `CornersUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[CornersUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/corners-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onCandidateQuadEdgesUnitReceived

Event triggered when candidate quad edges are detected.

```typescript
onCandidateQuadEdgesUnitReceived?(result: CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the candidate quad edges, of type `CandidateQuadEdgesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[CandidateQuadEdgesUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/candidate-quad-edges-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onCandidateBarcodeZonesUnitReceived

Event triggered when candidate barcode zones are detected.

```typescript
onCandidateBarcodeZonesUnitReceived?(result: CandidateBarcodeZonesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the candidate barcode zones, of type `CandidateBarcodeZonesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[CandidateBarcodeZonesUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/candidate-barcode-zones-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onScaledBarcodeImageUnitReceived

Called when a scaled barcode image unit is received.

```typescript
onScaledBarcodeImageUnitReceived?(result: ScaledBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the scaled barcode image, of type `ScaledBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ScaledUpBarcodeImageUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/scaled-barcode-image-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onDeformationResistedBarcodeImageUnitReceived

Called when a deformation resisted barcode image unit is received.

```typescript
onDeformationResistedBarcodeImageUnitReceived?(result: DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the deformation resisted barcode image, of type `DeformationResistedBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[DeformationResistedBarcodeImageUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/deformation-resisted-barcode-image-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onComplementedBarcodeImageUnitReceived

Called when a complemented barcode image unit is received.

```typescript
onComplementedBarcodeImageUnitReceived?(result: ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the complemented barcode image, of type `ComplementedBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[ComplementedBarcodeImageUnit](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/api-reference/interfaces/complemented-barcode-image-unit.html)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## OnRawTextLinesUnitReceived

Called when a raw text line unit is received.

```typescript
OnRawTextLinesUnitReceived?(result: RawTextLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the raw text line, of type `RawTextLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[RawTextLinesUnit](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/raw-textlines-unit.html?lang=js)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onLogicLinesUnitReceived

Called when a logic line unit is received.

```typescript
onLogicLinesUnitReceived?(result: LogicLinesUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains the logic line, of type `LogicLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[LogicLinesUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/logic-lines-unit.html?lang=js)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## onEnhancedImageReceived

Called when enhanced image is received.

```typescript
onEnhancedImageReceived?(result: EnhancedImageUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The result unit that contains enhanced image, of type `EnhancedImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[EnhancedImageUnit](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/api-reference/interfaces/enhanced-image-unit.html?lang=js)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)

## OnTargetROIResultsReceived

Called when all tasks for the target ROI are completed and the results are deduplicated.

```typescript
OnTargetROIResultsReceived?(result: IntermediateResultUnit, info: IntermediateResultExtraInfo): void;
```

**Parameters**

`result`: The `IntermediateResult` object that contains the result.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

**See Also**

[IntermediateResultUnit](../core/intermediate-results/intermediate-result-unit.md)

[IntermediateResultExtraInfo](../core/intermediate-results/intermediate-result-extra-info.md)