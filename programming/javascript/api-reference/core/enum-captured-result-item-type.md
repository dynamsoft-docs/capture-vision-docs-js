---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Core Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
codeAutoHeight: true
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` defines the various categories of items that can be recognized and captured.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumCapturedResultItemType {
    /**
     * Represents an original image captured by the system.
     * This type is used to identify the raw, unmodified image data directly obtained from the image source.
     */
    CRIT_ORIGINAL_IMAGE = 1,
    /**
     * Identifies a captured item as a barcode within the image.
     * This type signifies that the item has been recognized as a barcode and contains data extracted from the barcode.
     */
    CRIT_BARCODE = 2,
    /**
     * Identifies a captured item as a line of text within the image.
     * This type signifies that the item has been recognized as a line of text and contains the textual content.
     */
    CRIT_TEXT_LINE = 4,
    /**
     * Identifies a captured item as a quadrilateral detected within the image.
     * This type is typically used for geometric shapes or areas of interest that have been identified, often in the context of document scanning.
     */
    CRIT_DETECTED_QUAD = 8,
    /**
     * Represents an image that has been processed and deskewed based on the original image.
     * Deskewing may include adjustments such as perspective correction, etc. to standardize the image presentation.
     */
    CRIT_DESKEWED_IMAGE = 16,
    /**
     * Indicates a parsed result item.
     * This type is used for items that have undergone further interpretation by Dynamsoft Code Parser, transforming raw data into a structured format.
     */
    CRIT_PARSE_RESULT = 32,
    /**
     * Indicates a enhanced image item.
     * This type is used for items that have undergone post-processing, such as adjustments to brightness, contrast, color mode, etc.
     */
    CRIT_ENHANCED_IMAGE = 64
}
```