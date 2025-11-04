---
layout: default-layout
title: CaptureVisionRouter Auxiliary - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces auxiliary APIs related to the of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, auxiliary, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Auxiliaries

| Name                                         | Description                                                              |
| -------------------------------------------- | ------------------------------------------------------------------------ |
| [maxImageSideLength](#maximagesidelength)                        | Limits the maximum pixel value of the longest side of an image during the processing workflow.       |
| [appendDLModelBuffer()](#appenddlmodelbuffer)                        | Loads a specific data file containing recognition information.       |
| [onDataLoadProgressChanged](#ondataloadprogresschanged)                        | An event that fires during the loading of a recognition data file (.data). |
| [onCaptureError](#oncaptureerror)                        | An event that fires when an error occurs from the start of capturing process. |
| `static`[setGlobalIntraOpNumThreads](#setglobalintraopnumthreads)                        | Sets the global number of threads used internally for model execution. |
| `static`[clearDLModelBuffers](#cleardlmodelbuffers)                        | Clears all deep learning models from buffer to free up memory. |

## maxImageSideLength

The `maxImageSideLength` property limits the maximum pixel value of the longest side of an image during the processing workflow. If this value is exceeded, the image will be automatically downscaled.

**Syntax**

```typescript
maxImageSideLength: number;
```

## appendDLModelBuffer

Loads a specific data file containing recognition information. This file typically comprises a Convolutional Neural Networks (CNN) model.

**Syntax**

```typescript
static appendDLModelBuffer(dataName: string, dataPath?: string) : Promise<void>;
```

**Parameter**

`dataName` : Specifies the name of the data.

`dataPath`(Optional) : Specifies the path to find the data file. If not specified, the default path points to the package "dynamsoft-capture-vision-data" which has the same root path as the packag"dynamsoft-capture-vision-bundle".

**Return value**

None.

**Code snippet**

```javascript
CaptureVisionRouter.appendDLModelBuffer("sample-model.data")
    .then(() => {
        console.log("Model appended successfully.");
    })
    .catch(error => {
        console.error("Error loading model data:", error);
    });
```

**Remarks**

This method was renamed from `appendModelBuffer()` in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.1000.

## onDataLoadProgressChanged

An event that fires during the loading of a recognition data file (.data).

**Syntax**

```typescript
static onDataLoadProgressChanged (filePath: string, tag: "starting"| "in progress" | "completed", progress: { loaded: number, total: number }) : void;
```

**Parameter**

`filePath` : The path of the recognition data file.

`tag`(Optional) : Indicates the ongoing status of the file download ("starting", "in progress", "completed").

`progress` : An object indicating the progress of the download, with `loaded` and `total` bytes.

**Return value**

None.

**Code snippet**

```javascript
CaptureVisionRouter.onDataLoadProgressChanged = function(filePath, tag, progress) {
    console.log(`Status: ${tag} - File: ${filePath}`);
    if (tag === "in progress") {
        let percent = ((progress.loaded / progress.total) * 100).toFixed(1);
        console.log(`Progress: ${percent}%`);
    } else if (tag === "completed") {
        console.log("Model data loading completed!");
    }
};
```

## onCaptureError

An event that fires when an error occurs from the start of capturing process.

**Syntax**

```typescript
onCaptureError(error: Error) : void;
```

**Parameter**

`error` : he error object that contains the error code and error string.

**Return value**

None.

**Code snippet**

```javascript
CaptureVisionRouter.onCaptureError = function(error) {
    console.error("Capture error occurred:", error.message);
    // You can also show an alert or update the UI
    alert("An error occurred during capture: " + error.message);
};
```

## setGlobalIntraOpNumThreads

Sets the global number of threads used internally for model execution.

**Syntax**

```typescript
static setGlobalIntraOpNumThreads(intraOpNumThreads?: number): Promise<void>;
```

**Parameter**

`intraOpNumThreads`(optional) : Number of threads used internally for model execution.

**Code snippet**

```javascript
await CaptureVisionRouter.setGlobalIntraOpNumThreads(4);
```

**Remarks**

Introduced in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.1000.

## clearDLModelBuffers

Clears all deep learning models from buffer to free up memory.

**Syntax**

```typescript
static clearDLModelBuffers(): Promise<void>;
```

**Code snippet**

```javascript
await CaptureVisionRouter.clearDLModelBuffers();
```

**Remarks**

Introduced in Dynamsoft Barcode Reader Bundle version 11.2.2000 and Dynamsoft Capture Vision Bundle version 3.2.1000.