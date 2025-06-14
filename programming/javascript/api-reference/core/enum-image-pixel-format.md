---
layout: default-layout
title: ImagePixelFormat - Dynamsoft Core Enumerations
description: The enumeration ImagePixelFormat of Dynamsoft Core describes all supported image pixel formats.
keywords: Image pixel format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImagePixelFormat
codeAutoHeight: true
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` defines the range of pixel formats that an image can have, specifying how color and transparency data are represented in each pixel of the image.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumImagePixelFormat {
   /** 0:Black, 1:White. */
   IPF_BINARY = 0,
   /** 0:White, 1:Black. */
   IPF_BINARYINVERTED = 1,
   /** 8bit gray. */
   IPF_GRAYSCALED = 2,
   /** NV21. */
   IPF_NV21 = 3,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_565 = 4,
   /** 16bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_555 = 5,
   /** 24bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_888 = 6,
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_8888 = 7,
   /** 48bit with RGB channel order stored in memory from high to low address. */
   IPF_RGB_161616 = 8,
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   IPF_ARGB_16161616 = 9,
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_8888 = 10,
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   IPF_ABGR_16161616 = 11,
   /** 24bit with BGR channel order stored in memory from high to low address. */
   IPF_BGR_888 = 12,
   /** 0:Black, 255:White. */
   IPF_BINARY_8 = 13,
   /**NV12 */
   IPF_NV12 = 14
}
```