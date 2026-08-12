---
layout: default-layout
title: LayoutElementSource - Dynamsoft Utility Enumerations
description: The enumeration LayoutElementSource of Dynamsoft Utility describes the origin of an element in a layout analysis.
keywords: layout element source
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LayoutElementSource
codeAutoHeight: true
---

# Enumeration EnumLayoutElementSource

`EnumLayoutElementSource` describes the origin of an element in a layout analysis.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumLayoutElementSource{
   /**No element exists at this logical grid position (used for alignment in non-uniform rows).*/
   LES_NONE = 0,
   /**Element is provided from the original input array.*/
   LES_INPUT = 1,
   /**Element is inferred by the engine.*/
   LES_INFERRED = 2
}
```

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.