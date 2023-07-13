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

In Dynamsoft Capture Vision architecture, the following are the basic modules:

* **License**: handles the licensing of the software.
* **Capture Vision Router**: manages the capturing process.
* **Core**: provides basic interfaces that facilitate the capturing process.

These docs help you learn and use their APIs in your application.

## License Module

- [`LicenseManager`]({{ site.js_api }}license/licese-manager.html) Class
- [`LicenseVerificationListener`]({{ site.js_api }}license/license-verification-listener.html) Interface

## Capture Vision Router Module

- [`CaptureVisionRouter`]({{ site.js_api }}capture-vision-router/capture-vision-router.html) Class
- [`CaptureStateListener`]({{ site.js_api }}capture-vision-router/interfaces/capture-state-listener.html) Interface
- [`ImageSourceStateListener`]({{ site.js_api }}capture-vision-router/interfaces/image-source-state-listener.html) Interface
- [`SimplifiedCaptureVisionSettings`]({{ site.js_api }}capture-vision-router/interfaces/simplified-capture-vision-settings.html) Interface

## Core Module

### Input

- [`ImageSourceAdapter`]({{ site.js_api }}core/basic-structures/image-source-adapter.html) Class

### Output

- [`CapturedResultReceiver`]({{ site.js_api }}core/basic-structures/captured-result-receiver.html) Interface
- [`CapturedResultFilter`]({{ site.js_api }}core/basic-structures/captured-result-filter.html) Interface
- [`CapturedResult`]({{ site.js_api }}core/basic-structures/captured-result.html) Interface
- [`CapturedResultItem`]({{ site.js_api }}core/basic-structures/captured-result-item.html) Interface
- [`RawImageResultItem`]({{ site.js_api }}core/basic-structures/raw-image-result-item.html) Interface

### BasicStructures

- [`Arc`]({{ site.js_api }}core/basic-structures/arc.html) Interface
- [`Contour`]({{ site.js_api }}core/basic-structures/contour.html) Interface
- [`Corner`]({{ site.js_api }}core/basic-structures/corner.html) Interface
- [`DSFile`]({{ site.js_api }}core/basic-structures/ds-file.html) Interface
- [`DSImageData`]({{ site.js_api }}core/basic-structures.html) Interface
- [`DSRect`]({{ site.js_api }}core/basic-structures/ds-image-data.html) Interface
- [`Edge`]({{ site.js_api }}core/basic-structures/edge.html) Interface
- [`FileImageTag`]({{ site.js_api }}core/basic-structures/file-image-tag.html) Interface
- [`ImageTag`]({{ site.js_api }}core/basic-structures/image-tag.html) Interface
- [`LineSegment`]({{ site.js_api }}core/basic-structures/line-segment.html) Interface
- [`PDFReadingParameter`]({{ site.js_api }}core/basic-structures/pdf-reading-parameter.html) Interface
- [`Point`]({{ site.js_api }}core/basic-structures/point.html) Interface
- [`Polygon`]({{ site.js_api }}core/basic-structures/polygon.html) Interface
- [`Quadrilateral`]({{ site.js_api }}core/basic-structures/quadrilateral.html) Interface
- [`Rect`]({{ site.js_api }}core/basic-structures/rect.html) Interface
- [`VideoFrameTag`]({{ site.js_api }}core/basic-structures/video-frame-tag.html) Interface

### IntermediateResults

- [`IntermediateResultManager`]({{ site.js_api }}core/intermediate-results/intermediate-result-manager.html) Class
- [`BinaryImageUnit`]({{ site.js_api }}core/intermediate-results/binary-image-unit.html) Interface
- [`ColourImageUnit`]({{ site.js_api }}core/intermediate-results/colour-image-unit.html) Interface
- [`ContoursUnit`]({{ site.js_api }}core/intermediate-results/contours-unit.html) Interface
- [`EnhancedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/enhanced-grayscale-image-unit.html) Interface
- [`GrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/grayscale-image-unit.html) Interface
- [`IntermediateResultExtraInfo`]({{ site.js_api }}core/intermediate-results/intermediate-result-extra-info.html) Interface
- [`IntermediateResultReceiver`]({{ site.js_api }}core/intermediate-results/intermediate-result-receiver.html) Interface
- [`IntermediateResultUnit`]({{ site.js_api }}core/intermediate-results/intermediate-result-unit.html) Interface
- [`IntermediateResult`]({{ site.js_api }}core/intermediate-results/intermediate-result.html) Interface
- [`LineSegmentsUnit`]({{ site.js_api }}core/intermediate-results/line-segments-unit.html) Interface
- [`ObservationParameters`]({{ site.js_api }}core/intermediate-results/observation-parameters.html) Interface
- [`PredetectedRegionElement`]({{ site.js_api }}core/intermediate-results/predetected-region-element.html) Interface
- [`PredetectedRegionsUnit`]({{ site.js_api }}core/intermediate-results/predetected-regions-unit.html) Interface
- [`RegionObjectElement`]({{ site.js_api }}core/intermediate-results/region-object-element.html) Interface
- [`ScaledDownColourImageUnit`]({{ site.js_api }}core/intermediate-results/scaled-down-colour-image-unit.html) Interface
- [`TextRemovedBinaryImageUnit`]({{ site.js_api }}core/intermediate-results/text-removed-binary-image-unit.html) Interface
- [`TextZonesUnit`]({{ site.js_api }}core/intermediate-results/text-zones-unit.html) Interface
- [`TextureDetectionResultUnit`]({{ site.js_api }}core/intermediate-results/texture-detection-result-unit.html) Interface
- [`TextureRemovedBinaryImageUnit`]({{ site.js_api }}core/intermediate-results/texture-removed-binary-image-unit.html) Interface
- [`TextureRemovedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html) Interface
- [`TransformedGrayscaleImageUnit`]({{ site.js_api }}core/intermediate-results/transformed-grayscale-image-unit.html) Interface


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