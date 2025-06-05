---
layout: default-layout
title: RegionObjectElementType - Dynamsoft Core Enumerations
description: The enumeration RegionObjectElementType of Dynamsoft Core describes the types of RegionObjectElement.
keywords: Region object element type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RegionObjectElementType
codeAutoHeight: true
---

# Enumeration RegionObjectElementType

`RegionObjectElementType` specifies the exact subclass type within the `RegionObjectElement` hierarchy. This enumeration facilitates the identification and differentiation of various processed elements in an image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumRegionObjectElementType {
    /** 
     * Corresponds to the `PredetectedRegionElement` subclass, representing areas within the image identified as potentially significant
     * for further analysis before detailed processing.
     */
    ROET_PREDETECTED_REGION = 0,
    /** Corresponds to the `LocalizedBarcodeElement` subclass, indicating areas where barcodes have been localized within the image.*/
    ROET_LOCALIZED_BARCODE = 1,
    /** Corresponds to the `DecodedBarcodeElement` subclass, signifying barcodes that have not only been localized but also successfully decoded. */
    ROET_DECODED_BARCODE = 2,
    /** Corresponds to the `LocalizedTextLineElement` subclass, indicating lines of text that have been localized within the image. */
    ROET_LOCALIZED_TEXT_LINE = 3,
    /** Corresponds to the `RecognizedTextLineElement` subclass, referring to text lines that have been recognized. */
    ROET_RECOGNIZED_TEXT_LINE = 4,
    /** Corresponds to the `DetectedQuadElement` subclass, representing quadrilateral shapes detected within the image. */
    ROET_DETECTED_QUAD = 5,
    /** Corresponds to the `DeskewedImageElement` subclass, referring to images that have been deskewed. */
    ROET_DESKEWED_IMAGE = 6,
    /** Corresponds to the `EnhancedImageElement` subclass, referring to images that have been enhanced. */
    ROET_ENHANCED_IMAGE = 7
}
```