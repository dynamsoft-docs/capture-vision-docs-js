---
layout: default-layout
title: ImageTagType - Dynamsoft Core Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumImageTagType
{
   /**Represents an image that has been sourced from a static file.*/
   ITT_FILE_IMAGE = 0,
   /**Indicates that the image is a frame extracted from a video stream.*/
   ITT_VIDEO_FRAME = 1
}
```