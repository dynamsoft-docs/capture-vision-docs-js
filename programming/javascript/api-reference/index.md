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

- [`image-source-adapter`]({{ site.js_api }}core/basic-structures/image-source-adapter.html)

## Dynamsoft Core - BasicStructures

- [`arc`]({{ site.js_api }}core/basic-structures/arc.html)
- [`contour`]({{ site.js_api }}core/basic-structures/contour.html)
- [`corner`]({{ site.js_api }}core/basic-structures/corner.html)
- [`ds-file`]({{ site.js_api }}core/basic-structures/ds-file.html)
- [`ds-image-data`]({{ site.js_api }}core/basic-structures.html)
- [`ds-rect`]({{ site.js_api }}core/basic-structures/ds-image-data.html)
- [`edge`]({{ site.js_api }}core/basic-structures/edge.html)
- [`file-image-tag`]({{ site.js_api }}core/basic-structures/file-image-tag.html)
- [`image-tag`]({{ site.js_api }}core/basic-structures/image-tag.html)
- [`line-segment`]({{ site.js_api }}core/basic-structures/line-segment.html)
- [`pdf-reading-parameter`]({{ site.js_api }}core/basic-structures/pdf-reading-parameter.html)
- [`point`]({{ site.js_api }}core/basic-structures/point.html)
- [`polygon`]({{ site.js_api }}core/basic-structures/polygon.html)
- [`quadrilateral`]({{ site.js_api }}core/basic-structures/quadrilateral.html)
- [`rect`]({{ site.js_api }}core/basic-structures/rect.html)
- [`video-frame-tag`]({{ site.js_api }}core/basic-structures/video-frame-tag.html)


## Dynamsoft Core - IntermediateResults

- [`binary-image-unit`]({{ site.js_api }}core/intermediate-results/binary-image-unit.html)
- [`colour-image-unit`]({{ site.js_api }}core/intermediate-results/colour-image-unit.html)
- [`contours-unit`]({{ site.js_api }}core/intermediate-results/contours-unit.html)
- [`enhanced-grayscale-image-unit`]({{ site.js_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`grayscale-image-unit`]({{ site.js_api }}core/intermediate-results/grayscale-image-unit.html)
- [`intermediate-result-extra-info`]({{ site.js_api }}core/intermediate-results/intermediate-result-extra-info.html)
- [`intermediate-result-manager`]({{ site.js_api }}core/intermediate-results/intermediate-result-manager.html)
- [`intermediate-result-receiver`]({{ site.js_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`intermediate-result-unit`]({{ site.js_api }}core/intermediate-results/intermediate-result-unit.html)
- [`intermediate-result`]({{ site.js_api }}core/intermediate-results/intermediate-result.html)
- [`line-segments-unit`]({{ site.js_api }}core/intermediate-results/line-segments-unit.html)
- [`observation-parameters`]({{ site.js_api }}core/intermediate-results/observation-parameters.html)
- [`predetected-region-element`]({{ site.js_api }}core/intermediate-results/predetected-region-element.html)
- [`predetected-regions-unit`]({{ site.js_api }}core/intermediate-results/predetected-regions-unit.html)
- [`region-object-element`]({{ site.js_api }}core/intermediate-results/region-object-element.html)
- [`scaled-down-colour-image-unit`]({{ site.js_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`text-removed-binary-image-unit`]({{ site.js_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- [`text-zones-unit`]({{ site.js_api }}core/intermediate-results/text-zones-unit.html)
- [`texture-detection-result-unit`]({{ site.js_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`texture-removed-binary-image-unit`]({{ site.js_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`texture-removed-grayscale-image-unit`]({{ site.js_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`transformed-grayscale-image-unit`]({{ site.js_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Dynamsoft Core - FinalResult

- [`captured-result`]({{ site.js_api }}core/basic-structures/captured-result.html)
- [`captured-result-filter`]({{ site.js_api }}core/basic-structures/captured-result-filter.html)
- [`captured-result-item`]({{ site.js_api }}core/basic-structures/captured-result-item.html)
- [`captured-result-receiver`]({{ site.js_api }}core/basic-structures/captured-result-receiver.html)
- [`raw-image-result-item`]({{ site.js_api }}core/basic-structures/raw-image-result-item.html)

## Enumerations

- [`barcode-format`]({{ site.enums }}barcode-reader/barcode-format.html?lang=js)
- [`buffer-overflow-protection-mode`]({{ site.enums }}core/buffer-overflow-protection-mode.html?lang=js)
- [`captured-result-item-type`]({{ site.enums }}core/captured-result-item-type.html?lang=js)
- [`capture-state`]({{ site.enums }}capture-vision-router/capture-state.html?lang=js)
- [`corner-type`]({{ site.enums }}core/corner-type.html?lang=js)  
- [`deblur-mode`]({{ site.enums }}barcode-reader/deblur-mode.html?lang=js)
- [`error-code`]({{ site.enums }}core/error-code.html?lang=js)
- [`extended-barcode-result-type`]({{ site.enums }}barcode-reader/extended-barcode-result-type.html?lang=js)
- [`grayscale-transformation-mode`]({{ site.enums }}core/grayscale-transformation-mode.html?lang=js)
<!--- [`image-capture-distance-mode`]({{ site.enums }}core/image-capture-distance-mode.html?lang=js)-->
- [`image-pixel-format`]({{ site.enums }}core/image-pixel-format.html?lang=js)
- [`image-source-state`]({{ site.enums }}core/image-source-state.html?lang=js)
- [`image-tag-type`]({{ site.enums }}core/image-tag-type.html?lang=js)
- [`intermediate-result-unit-type`]({{ site.enums }}core/intermediate-result-unit-type.html?lang=js)
- [`localization-mode`]({{ site.enums }}barcode-reader/localization-mode.html?lang=js)
- [`mapping-status`]({{ site.enums }}code-parser/mapping-status.html?lang=js)
- [`pdf-reading-mode`]({{ site.enums }}core/pdf-reading-mode.html?lang=js)
- [`qr-code-error-correction-level`]({{ site.enums }}barcode-reader/qr-code-error-correction-level.html?lang=js)
- [`region-object-element-type`]({{ site.enums }}core/region-object-element-type.html?lang=js)
- [`section-type`]({{ site.enums }}core/section-type.html?lang=js)
- [`target-type`]({{ site.enums }}core/target-type.html?lang=js)
- [`validation-status`]({{ site.enums }}code-parser/validation-status.html?lang=js)
<!--- [`video-frame-quality.html`]({{ site.enums }}core/video-frame-quality.html?lang=js)-->
- [`colour-channel-usage-type`]({{ site.enums }}core/colour-channel-usage-type.html?lang=js)