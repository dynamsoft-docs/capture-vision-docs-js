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
   /** Deprecated. Covered by PDFRM_MULTIMODAL.*/
   PDFRM_VECTOR = 1,
   /** Renders the entire page as a bitmap regardless of object type.*/
   PDFRM_RASTER = 2,
   /** Extracts multimodal information from a PDF, including vector graphics,
    * text content, and embedded images, which can be used for subsequent
    * tasks such as barcode reading, text recognition, and document analysis.*/
   PDFRM_MULTIMODAL = 3
}
```