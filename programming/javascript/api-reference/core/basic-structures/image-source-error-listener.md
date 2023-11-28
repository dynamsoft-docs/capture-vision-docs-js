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

The `ImageSourceErrorListener` interface defines the standard way to receive notifications should errors occur during image acquisition.

## Definition

```typescript
interface ImageSourceErrorListener {
    onErrorReceived(errorCode: number, errorMessage:string):void;
} 
```

### onErrorReceived

Callback function that is triggered when an error occurs during image acquisition.

```typescript
onErrorReceived(errorCode: number, errorMessage:string):void;
```

**Parameters**

`errorCode`: The error code.

`errorMessage`: The error message.
