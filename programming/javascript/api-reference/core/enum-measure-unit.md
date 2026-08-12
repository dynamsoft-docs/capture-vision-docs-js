---
layout: default-layout
title: MeasureUnit - Dynamsoft Core Enumerations
description: The enumeration MeasureUnit of Dynamsoft Core specifies how a numeric value should be interpreted relative to a reference dimension.
keywords: Measure unit, pixel, percentage
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: MeasureUnit
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension. Used wherever a numeric parameter (e.g. spacing, ROI coordinates) can be expressed either as an absolute pixel count or as a proportion of a reference size.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumMeasureUnit {
   /**The value is an absolute pixel count.*/
   MU_PIXEL = 0,
   /**The value is a percentage of the reference dimension (e.g. 25 = 25%).*/
   MU_PERCENTAGE = 1
}
```

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.
