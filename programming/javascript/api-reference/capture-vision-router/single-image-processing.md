---
layout: default-layout
title: CaptureVisionRouter Single File Processing - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to processing single files, including images and multi-page PDF documents.
keywords: capture vision, file processing, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Single File Processing

| Name                  | Description                                                                                   |
| --------------------- | --------------------------------------------------------------------------------------------- |
| [capture()](#capture) | Processes a single image or file to derive important information. |
| [captureMultiPages()](#capturemultipages) | Processes a multi-page PDF file and returns the extracted content for each page. |

## capture

Processes a single image or file to derive important information.

**Syntax**

```typescript
capture(imageOrFile: Blob | HTMLImageElement | HTMLCanvasElement | HTMLVideoElement | DSImageData | string, templateName?: string): Promise<CapturedResult>;
```

**Parameters**

`imageOrFile`: specifies the image or file to be processed.

  >The following data types are accepted: `Blob`, `HTMLImageElement`, `HTMLCanvasElement`, `HTMLVideoElement`, `DSImageData`, `string`.
  >
  >The supported image formats include: `.jpg`, `.jpeg`, `.icon`, `.gif`, `.svg`, `.webp`, `.png`, `.bmp`.

`templateName`: specifies a "CaptureVisionTemplate" to use. If not specified, the preset template named 'Default' will be used.

There are two types of CaptureVisionTemplates: the [preset ones](./preset-templates.md) which come with the SDK and the custom ones that get initialized when the user calls [initSettings](./settings.md#initsettings). 

Please be aware that the [preset CaptureVisionTemplates](./preset-templates.md)  will be overwritten if the user calls [initSettings](./settings.md#initsettings) and passes customized settings.

**Return value**

A promise that resolves with a [CapturedResult]({{ site.dcv_js_api }}interfaces/captured-result.html) object which contains the derived information from the file processed.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let results = await router.capture("blob:https://demo.dynamsoft.com/afb84bd2-e8cb-4b96-92b6-36dc89783692", "ReadSingleBarcode");
let count = results.items.length;
for(let i = 0; i < count; i++) {
    //...
}
```

## captureMultiPages

Captures multiple pages from a PDF file and returns the extracted content for each specified page.

**Syntax**

```typescript
captureMultiPages(file: Blob | string, templateName?: string, options?: PDFOptions): Promise<CapturedResult[]>;
```

**Parameters**

`file`: the PDF file to process. Can be provided as a `Blob` object or a file path string.

`templateName`: specifies a "CaptureVisionTemplate" to use. If not specified, the preset template named 'Default' will be used.

`options`: optional configuration parameters for the capture operation.

- `pages`: an array of page numbers (0-indexed) to extract. If empty or omitted, all pages in the document will be processed.
- `dpi`: the DPI (dots per inch) resolution for rendering. Defaults to 300.

**Return value**

A promise that resolves to an array of [CapturedResult]({{ site.dcv_js_api }}interfaces/captured-result.html) objects, where each object corresponds to the extracted data from a single page in the order specified.

**Remarks**

New added in CaptureVisionBundle version 3.6.2000 & BarcodeReaderBundle version 11.6.2000.