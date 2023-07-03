---
layout: default-layout
title: API Reference Index - Dynamsoft Capture Vision JavaScript Edition
description: This is the index page for Dynamsoft Capture Vision API Reference
keywords: CaptureVision, Capture, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: API Reference
permalink: /programming/javascript/api-reference/
---

# JavaScript API Reference

In the Dynamsoft Capture Vision architecture, the following are the basic modules:

* Dynamsoft License
* Capture Vision Router
* Dynamsoft Core

These docs help you learn and use their APIs in your application.

## Dynamsoft License

- [`LicenseManager`]({{ site.js_api }}license/licese-manager.html)
- [`LicenseVerificationListener`]({{ site.js_api }}license/license-verification-listener.html)

## Capture Vision Router

- [`CaptureVisionRouter`]({{ site.js_api }}capture-vision-router/capture-vision-router.html)
- [`CaptureStateListener`]({{ site.js_api }}capture-vision-router/interfaces/capture-state-listener.html)
- [`ImageSourceStateListener`]({{ site.js_api }}capture-vision-router/interfaces/image-source-state-listener.html)
- [`SimplifiedCaptureVisionSettings`]({{ site.js_api }}capture-vision-router/interfaces/simplified-capture-vision-settings.html)

## Dynamsoft Core - Input

- [`ImageSourceAdapter`]({{ site.js_api }}core/basic-structures/image-source-adapter.html)

## Dynamsoft Core - BasicStructures

- [`Arc`]({{ site.js_api }}core/basic-structures/arc.html)
- [`Contour`]({{ site.js_api }}core/basic-structures/contour.html)
- [`Corner`]({{ site.js_api }}core/basic-structures/corner.html)
- [`DSFile`]({{ site.js_api }}core/basic-structures/ds-file.html)
- [`DSImageData`]({{ site.js_api }}core/basic-structures.html)
- [`DSRect`]({{ site.js_api }}core/basic-structures/ds-image-data.html)
- [`Edge`]({{ site.js_api }}core/basic-structures/edge.html)
- [`FileImageTag`]({{ site.js_api }}core/basic-structures/file-image-tag.html)
- [`ImageTag`]({{ site.js_api }}core/basic-structures/image-tag.html)
- [`LineSegment`]({{ site.js_api }}core/basic-structures/line-segment.html)
- [`PDFReadingParameter`]({{ site.js_api }}core/basic-structures/pdf-reading-parameter.html)
- [`Point`]({{ site.js_api }}core/basic-structures/point.html)
- [`Polygon`]({{ site.js_api }}core/basic-structures/polygon.html)
- [`Quadrilateral`]({{ site.js_api }}core/basic-structures/quadrilateral.html)
- [`Rect`]({{ site.js_api }}core/basic-structures/rect.html)
- [`VideoFrameTag`]({{ site.js_api }}core/basic-structures/video-frame-tag.html)


## Dynamsoft Core - IntermediateResults

- [`BinaryImageUnit`]({{ site.js_api }}core/intermediate-results/binary-image-unit.html)
- [`ColourImageUnit`]({{ site.js_api }}core/intermediate-results/colour-image-unit.html)
- [`ContoursUnit`]({{ site.js_api }}core/intermediate-results/contours-unit.html)
- [`EnhancedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`GrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/grayscale-image-unit.html)
- [`IntermediateResultExtraInfo`]({{ site.js_api }}core/intermediate-results/intermediate-result-extra-info.html)
- [`IntermediateResultManager`]({{ site.js_api }}core/intermediate-results/intermediate-result-manager.html)
- [`IntermediateResultReceiver`]({{ site.js_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`IntermediateResultUnit`]({{ site.js_api }}core/intermediate-results/intermediate-result-unit.html)
- [`IntermediateResult`]({{ site.js_api }}core/intermediate-results/intermediate-result.html)
- [`LineSegmentsUnit`]({{ site.js_api }}core/intermediate-results/line-segments-unit.html)
- [`ObservationParameters`]({{ site.js_api }}core/intermediate-results/observation-parameters.html)
- [`PredetectedRegionElement`]({{ site.js_api }}core/intermediate-results/predetected-region-element.html)
- [`PredetectedRegionsUnit`]({{ site.js_api }}core/intermediate-results/predetected-regions-unit.html)
- [`RegionObjectElement`]({{ site.js_api }}core/intermediate-results/region-object-element.html)
- [`ScaledDownColourImageUnit`]({{ site.js_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`TextRemovedBinaryImageUnit`]({{ site.js_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`TextZonesUnit`]({{ site.js_api }}core/intermediate-results/text-zones-unit.html)
- [`TextureDetectionResultUnit`]({{ site.js_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`TextureRemovedBinaryImageUnit`]({{ site.js_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`TextureRemovedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`TransformedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Dynamsoft Core - FinalResult

- [`CapturedResult`]({{ site.js_api }}core/basic-structures/captured-result.html)
- [`CapturedResultFilter`]({{ site.js_api }}core/basic-structures/captured-result-filter.html)
- [`CapturedResultItem`]({{ site.js_api }}core/basic-structures/captured-result-item.html)
- [`CapturedResultReceiver`]({{ site.js_api }}core/basic-structures/captured-result-receiver.html)
- [`RawImageResultItem`]({{ site.js_api }}core/basic-structures/raw-image-result-item.html)

## Enumerations

- [`BarcodeFormat`]({{ site.enums }}barcode-reader/barcode-format.html?lang=js)
- [`BufferOverflowProtectionMode`]({{ site.enums }}core/buffer-overflow-protection-mode.html?lang=js)
- [`CapturedResultItemType`]({{ site.enums }}core/captured-result-item-type.html?lang=js)
- [`CaptureState`]({{ site.enums }}capture-vision-router/capture-state.html?lang=js)
- [`CornerType`]({{ site.enums }}core/corner-type.html?lang=js)  
- [`DeblurMode`]({{ site.enums }}barcode-reader/deblur-mode.html?lang=js)
- [`ErrorCode`]({{ site.enums }}core/error-code.html?lang=js)
- [`ExtendedBarcodeResultType`]({{ site.enums }}barcode-reader/extended-barcode-result-type.html?lang=js)
- [`GrayscaleTransformationMode`]({{ site.enums }}core/grayscale-transformation-mode.html?lang=js)
<!--- [`image-capture-distance-mode`]({{ site.enums }}core/image-capture-distance-mode.html?lang=js)-->
- [`ImagePixelFormat`]({{ site.enums }}core/image-pixel-format.html?lang=js)
- [`ImageSourceState`]({{ site.enums }}core/image-source-state.html?lang=js)
- [`ImageTagType`]({{ site.enums }}core/image-tag-type.html?lang=js)
- [`IntermediateResultUnitType`]({{ site.enums }}core/intermediate-result-unit-type.html?lang=js)
- [`LocalizationMode`]({{ site.enums }}barcode-reader/localization-mode.html?lang=js)
- [`MappingStatus`]({{ site.enums }}code-parser/mapping-status.html?lang=js)
- [`PDFReadingMode`]({{ site.enums }}core/pdf-reading-mode.html?lang=js)
- [`QRCodeErrorCorrectionLevel`]({{ site.enums }}barcode-reader/qr-code-error-correction-level.html?lang=js)
- [`RegionObjectElementType`]({{ site.enums }}core/region-object-element-type.html?lang=js)
- [`SectionType`]({{ site.enums }}core/section-type.html?lang=js)
- [`TargetType`]({{ site.enums }}core/target-type.html?lang=js)
- [`ValidationStatus`]({{ site.enums }}code-parser/validation-status.html?lang=js)
<!--- [`video-frame-quality.html`]({{ site.enums }}core/video-frame-quality.html?lang=js)-->
- [`ColourChannelUsageType`]({{ site.enums }}core/colour-channel-usage-type.html?lang=js)