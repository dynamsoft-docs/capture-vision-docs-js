---
layout: default-layout
title: Interface CapturedResultBase - Dynamsoft Core Module JS Edition API Reference
description: This page shows the JS edition of the interface CapturedResultBase in Dynamsoft Core Module.
keywords: captured result, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
ignore: true
---

# CapturedResultBase

The `CapturedResultBase` interface describes the base structure of all captured result object returned by Dynamsoft Capture Vision Router.

```typescript
interface CapturedResultBase {
    readonly errorCode: number;
    readonly errorString: string;
    readonly originalImageHashId: string;
    readonly originalImageTag: Core.ImageTag;
}
```

## errorCode

Error code associated with the capture result.

## errorString

Error string providing details about the error.

## originalImageHashId

The hash ID of the original image.

## originalImageTag

The tag associated with the original image.