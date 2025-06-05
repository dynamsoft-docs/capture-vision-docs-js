---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumGrayscaleEnhancementMode
{
    /**
     * Disables any grayscale image preprocessing. Selecting this mode skips the preprocessing step,
     * passing the image through to subsequent operations without modification.
     */
    GEM_SKIP = 0,
    /**
     * Automatic selection of grayscale enhancement mode. Currently, not supported.
     * Future implementations may automatically choose the most suitable enhancement based on image analysis.
     */
    GEM_AUTO = 1,
    /**
     * Uses the original, unprocessed image for subsequent operations. This mode is selected when no specific
     * grayscale enhancement is required, maintaining the image in its natural state.
     */
    GEM_GENERAL = 2,
    /**
     * Applies a grayscale equalization algorithm to the image, enhancing contrast and detail in gray level.
     * Suitable for images with poor contrast.
     */
    GEM_GRAY_EQUALIZE = 4,
    /**
     * Implements a grayscale smoothing algorithm to reduce noise and smooth the image.
     * This can be beneficial for images with high levels of grain or noise.
     */
    GEM_GRAY_SMOOTH = 8,
    /**
     * Enhances the image by applying both sharpening and smoothing algorithms. This mode aims to increase
     * clarity and detail while reducing noise, offering a balanced approach to image preprocessing.
     */
    GEM_SHARPEN_SMOOTH = 16,
    /**
     * Placeholder value with no functional meaning.
     */
    GEM_END = 0xFFFFFFFF,
    /**
     * Reserved for future use. This setting is part of the grayscale enhancement mode but is
     * currently not defined for public use. It's reserved for internal development or future enhancements. 
     */
    GEM_REV = -2147483648
}
```