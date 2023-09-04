---
layout: default-layout
title: CaptureVisionRouter Single Process - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to "Single Process" with Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, caputre, image processing, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
permalink: /programming/javascript/api-reference/capture-vision-router/single-file-processing.html
---

# CaptureVisionRouter Single File Processing

| API Name              | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [capture()](#capture) | Process an image or file to derive important information. |

## capture

Process an image or file to derive important information.

**Syntax**

```typescript
capture(imageOrFile: Core.BasicStructures.DSImageData | string | Blob | HTMLImageElement | HTMLCanvasElement, templateName?: string): Promise<Array<Core.BasicStructures.CapturedResult>>;
```

**Parameters**

`imageOrFile`: specifies the image or file to be processed. It can be the image itself in the form of `DSImageData`, the path of the image/file or the file itself in the form of `blob`, `HTMLImageElement` or `HTMLCanvasElement`.

`templateName`: specifies a [CaptureVisionTemplate]({{site.parameterFile}}capture-vision-template.html) to use. If not specified, the default one is used.

**Return value**

A promise that resolves to an array of `CapturedResult` objects which are the derived information from each image processed.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let results = await router.capture("blob:https://demo.dynamsoft.com/afb84bd2-e8cb-4b96-92b6-36dc89783692", "detect-document-boundaries");
let count = results.length;
for(let i = 0; i < count; i++) {
    //...
}
```