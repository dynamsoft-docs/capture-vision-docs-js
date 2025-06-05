---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core Enumerations
description: The enumeration PDFReadingMode of Dynamsoft Core describes all available PDF reading modes.
keywords: PDF Reading Mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: PDFReadingMode
codeAutoHeight: true
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumPDFReadingMode
{
   /** Outputs vector data found in the PDFs.*/
   PDFRM_VECTOR = 1,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, 
    * the SDK may rasterize the PDF pages.
    * Check the template for available argument settings.*/
   PDFRM_RASTER = 2,
   /** Reserved setting for PDF reading mode.*/
   PDFRM_REV = -2147483648
}
```