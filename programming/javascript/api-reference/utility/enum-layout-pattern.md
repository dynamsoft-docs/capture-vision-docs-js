---
layout: default-layout
title: LayoutPattern - Dynamsoft Utility Enumerations
description: The enumeration LayoutPattern of Dynamsoft Utility describes the layout pattern for quadrilateral analysis.
keywords: layout pattern
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LayoutPattern
codeAutoHeight: true
---

# Enumeration EnumLayoutPattern

`EnumLayoutPattern` describes the strategy for the layout engine to organize quadrilaterals.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumLayoutPattern{
   /**Algorithm automatically detects the best layout pattern.*/
   LP_UNKNOWN = 0,
   /**Elements are organized into sequential lines (rows or columns).*/
   LP_LINES = 1,
   /**Elements are organized into a strict grid/matrix structure.*/
   LP_MATRIX = 2
}
```

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.