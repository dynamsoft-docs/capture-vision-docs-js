---
layout: default-layout
title: IntermediateResultUnitType - Dynamsoft Core Enumerations
description: The enumeration IntermediateResultUnitType of Dynamsoft Core describes the type of the intermediate result unit.
keywords: Intermediate result unit type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: IntermediateResultUnitType
codeAutoHeight: true
---

# Enumeration IntermediateResultUnitType

`IntermediateResultUnitType` defines different types of intermediate results generated or expected to be generated during image processing.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumIntermediateResultUnitType {
    /** No intermediate result. */
    IRUT_NULL = 0,
    /** A full-color image. */
    IRUT_COLOUR_IMAGE = 1,
    /** A color image that has been scaled down for efficiency. */
    IRUT_SCALED_DOWN_COLOUR_IMAGE = 1 << 1,
    /** A grayscale image derived from the original input. */
    IRUT_GRAYSCALE_IMAGE = 1 << 2,
    /** A grayscale image that has undergone transformation. */
    IRUT_TRANSOFORMED_GRAYSCALE_IMAGE = 1 << 3,
    /** A grayscale image enhanced for further processing. */
    IRUT_ENHANCED_GRAYSCALE_IMAGE = 1 << 4,
    /** Regions pre-detected as potentially relevant for further analysis. */
    IRUT_PREDETECTED_REGIONS = 1 << 5,
    /** A binary (black and white) image. */
    IRUT_BINARY_IMAGE = 1 << 6,
    /** Results from detecting textures within the image. */
    IRUT_TEXTURE_DETECTION_RESULT = 1 << 7,
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1 << 8,
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1 << 9,
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    IRUT_CONTOURS = 1 << 10,
    /** Detected line segments, useful in structural analysis of the image content. */
    IRUT_LINE_SEGMENTS = 1 << 11,
    /** Identified text zones, indicating areas with potential textual content. */
    IRUT_TEXT_ZONES = 1 << 12,
    /** A binary image with text regions removed. */
    IRUT_TEXT_REMOVED_BINARY_IMAGE = 1 << 13,
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    IRUT_CANDIDATE_BARCODE_ZONES = 1 << 14,
    /** Barcodes that have been localized but not yet decoded. */
    IRUT_LOCALIZED_BARCODES = 1 << 15,
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    IRUT_SCALED_UP_BARCODE_IMAGE = 1 << 16,
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1 << 17,
    /** Barcode images that have been complemented. */
    IRUT_COMPLEMENTED_BARCODE_IMAGE = 1 << 18,
    /** Successfully decoded barcodes. */
    IRUT_DECODED_BARCODES = 1 << 19,
    /** Detected long lines. */
    IRUT_LONG_LINES = 1 << 20,
    /** Detected corners within the image. */
    IRUT_CORNERS = 1 << 21,
    /** Candidate edges identified as potential components of quadrilaterals. */
    IRUT_CANDIDATE_QUAD_EDGES = 1 << 22,
    /** Successfully detected quadrilaterals. */
    IRUT_DETECTED_QUADS = 1 << 23,
    /** Text lines that have been localized in preparation for recognition. */
    IRUT_LOCALIZED_TEXT_LINES = 1 << 24,
    /** Successfully recognized text lines. */
    IRUT_RECOGNIZED_TEXT_LINES = 1 << 25,
    /** Successfully normalized images. */
    IRUT_NORMALIZED_IMAGES = 1 << 26,
    /**Detected short lines.*/
    IRUT_SHORT_LINES = 1 << 27,
    /**grouped lines of text.*/
    IRUT_TEXT_LINE_GROUPS = 1 << 28,
    /** Detected logic lines. */
    IRUT_LOGIC_LINES = 1 << 29,
    /** A mask to select all types of intermediate results. */
    IRUT_ALL = 0xFFFFFFFFFFFFFFFF
}
```