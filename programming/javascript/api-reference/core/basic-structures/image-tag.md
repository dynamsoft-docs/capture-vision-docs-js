---
layout: default-layout
title: Interface ImageTag - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface ImageTag in Dynamsoft Core Module.
keywords: image tag, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# ImageTag

The `ImageTag` interface represents a tag associated with an image, providing metadata such as the image ID and type.

```typescript
interface ImageTag {
    imageId: number;
    type: EnumImageTagType;
}
```

## imageId

The unique identifier of the image.

## type

The type of the image.

[EnumImageTagType]({{ site.dcvb_js_api }}enums-image-tag-type.html?lang=js)
