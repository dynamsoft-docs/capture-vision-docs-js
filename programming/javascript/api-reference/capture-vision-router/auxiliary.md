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
| [appendModelBuffer()](#appendmodelbuffer)                        | Loads a specific data file containing recognition information.       |
| [onDataLoadProgressChanged](#ondataloadprogresschanged)                        | An event that fires during the loading of a recognition data file (.data). |
| [onCaptureError](#oncaptureerror)                        | An event that fires when an error occurs from the start of capturing process. |

## maxImageSideLength

The `maxImageSideLength` property limits the maximum pixel value of the longest side of an image during the processing workflow. If this value is exceeded, the image will be automatically downscaled.

**Syntax**

```typescript
maxImageSideLength: number;
```

## appendModelBuffer

Loads a specific data file containing recognition information. This file typically comprises a Convolutional Neural Networks (CNN) model.

**Syntax**

```typescript
static appendModelBuffer(dataName: string, dataPath?: string) : Promise<void>;
```

**Parameter**

`dataName` : Specifies the name of the data.

`dataPath`(Optional) : Specifies the path to find the data file. If not specified, the default path points to the package "dynamsoft-capture-vision-data" which has the same root path as the packag"dynamsoft-capture-vision-bundle".

**Return value**

None.

**Code snippet**

```javascript
CaptureVisionRouter.appendModelBuffer("sample-model.data")
    .then(() => {
        console.log("Model appended successfully.");
    })
    .catch(error => {
        console.error("Error loading model data:", error);
    });
```

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