---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumGrayscaleTransformationMode
{
    /**
     * Bypasses grayscale transformation, leaving the image in its current state without any modification to its grayscale values.
     * This mode is selected when no alteration of the grayscale data is desired, passing the image through to subsequent operations without modification.
     */
    GTM_SKIP = 0,
    /**
     * Applies an inversion to the grayscale values of the image, effectively transforming light elements to dark and vice versa.
     * This mode is particularly useful for images with light text on dark backgrounds, enhancing visibility for further processing.
     */
    GTM_INVERTED = 1,
    /**
     * Maintains the original grayscale values of the image without any transformation. This mode is suited for images with
     * dark elements on light backgrounds, ensuring the natural contrast and detail are preserved for subsequent analysis.
     */
    GTM_ORIGINAL = 2,
    /**
     * Delegates the choice of grayscale transformation to the library's algorithm, which automatically determines the most
     * suitable transformation based on the image's characteristics. This mode is beneficial when the optimal transformation
     * is not known in advance or varies across different images.
     */
    GTM_AUTO = 4,
    /**
     * Placeholder value with no functional meaning.
     */
    GEM_END = 0xFFFFFFFF,
    /**
     * Reserved for future expansion or internal use. This placeholder indicates a grayscale transformation mode that is
     * not currently defined for public use but may be utilized for upcoming features or reserved for specific, undocumented adjustments.
     */
    GTM_REV = -2147483648
}
```