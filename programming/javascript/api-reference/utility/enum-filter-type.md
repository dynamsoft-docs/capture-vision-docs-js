---
layout: default-layout
title: FilterType - Dynamsoft Utility Enumerations
description: The enumeration FilterType of Dynamsoft Utility describes how to filter images.
keywords: Filter type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: FilterType
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` categorizes the type of pre-build filters to filter images.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumFilterType{
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   FT_HIGH_PASS = 0,
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   FT_SHARPEN = 1,
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   FT_SMOOTH = 2
}
```