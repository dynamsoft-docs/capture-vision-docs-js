---
layout: default-layout
title: Interface ImageSourceErrorListener - Dynamsoft Capture Vision JS Edition API Reference
description: This page shows the JS edition of the interface ImageSourceErrorListener in Core Module.
keywords: imagesource, error listener, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: JS ImageSourceErrorListener Interface
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` interface defines the standard way to receive notifications from an image source should errors occur during image acquisition.

```typescript
interface ImageSourceErrorListener {
    onErrorReceived(errorCode: EnumErrorCode, errorMessage:string):void;
} 
```

## onErrorReceived

Event triggered when an error is received from the image source.

```typescript
onErrorReceived(errorCode: EnumErrorCode, errorMessage:string):void;
```

**Parameters**

`errorCode`: An enumeration value of type `EnumErrorCode` indicating the type of error.

`errorMessage`: A string containing the error message providing additional information about the error.

**See Also**

[EnumErrorCode](https://www.dynamsoft.com/capture-vision/docs/core/enums/core/error-code.html?lang=js)