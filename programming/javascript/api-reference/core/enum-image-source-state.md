---
layout: default-layout
title: ImageSourceState - Dynamsoft Core Enumerations
description: The enumeration ImageSourceState of Dynamsoft Core describes the state of ImageSourceAdapter.
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
codeAutoHeight: true
ignore: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the state of `ImageSourceAdapter`.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumImageSourceState
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   ISS_BUFFER_EMPTY = 0,
   /** The source of ImageSourceAdapter is empty. */
   ISS_EXHAUSTED = 1
}
```