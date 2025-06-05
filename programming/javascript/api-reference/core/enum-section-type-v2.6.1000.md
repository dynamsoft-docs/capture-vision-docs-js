---
layout: default-layout
title: SectionType - Dynamsoft Core Enumerations
description: The enumeration SectionType of Dynamsoft Core describes the section of the algorithm.
keywords: Section type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: SectionType
codeAutoHeight: true
---

# Enumeration SectionType

`SectionType` categorizes the distinct segments within the image processing algorithm, pinpointing the exact phase responsible for generating a specific `IntermediateResult`.


<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumSectionType {
    /** Indicates that no specific section type has been specified. */
    ST_NULL = 0,
    /** Corresponds to results generated in the "region prediction" section. */
    ST_REGION_PREDETECTION = 1,
    /** Corresponds to results generated in the "barcode localization" section. */
    ST_BARCODE_LOCALIZATION = 2,
    /** Corresponds to results generated in the "barcode decoding" section. */
    ST_BARCODE_DECODING = 3,
    /** Corresponds to results generated in the "text line localization" section. */
    ST_TEXT_LINE_LOCALIZATION = 4,
    /** Corresponds to results generated in the "text line recognition" section. */
    ST_TEXT_LINE_RECOGNITION = 5,
    /** Corresponds to results generated in the "document detection" section. */
    ST_DOCUMENT_DETECTION = 6,
    /** Corresponds to results generated in the "document normalization" section. */
    ST_DOCUMENT_NORMALIZATION = 7
}
```