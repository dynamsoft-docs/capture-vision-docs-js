---
layout: default-layout
title: Scan & Parse MRZ  - Dynamsoft Capture Vision JavaScript Edition
description: This page introduce how to use Dynamsoft Capture Vision JS edition to recognize the Machine-Readable Zone (MRZ) on a passport or ID card and converts the encoded strings into human-readable fields.
keywords: JavaScript, scan mrz, read mrz, scan passport, read passport, scan id mrz, read id mrz
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# MRZ Scanner Solution for Your Website - User Guide

This guide walks you through the process of creating a simple MRZ scanner solution.

<span style="font-size:20px">Table of Contents</span>

- [MRZ Scanner Solution for Your Website - User Guide](#mrz-scanner-solution-for-your-website---user-guide)
  - [About the solution](#about-the-solution)
    - [Web demo](#web-demo)
    - [Run this Solution](#run-this-solution)
    - [Project structure](#project-structure)
  - [Building your own page](#building-your-own-page)
    - [Include the SDK](#include-the-sdk)
    - [Set up the solution](#set-up-the-solution)
      - [Specify the license](#specify-the-license)
      - [Load resources in advance](#load-resources-in-advance)
      - [Create an CaptureVisionRouter instance and initialize the settings](#create-an-capturevisionrouter-instance-and-initialize-the-settings)
      - [Use the camera as the image source](#use-the-camera-as-the-image-source)
    - [Complete the Solution](#complete-the-solution)
      - [Start recognition and coordinate image-processing tasks](#start-recognition-and-coordinate-image-processing-tasks)
      - [Handle the captured result](#handle-the-captured-result)
  - [Host the SDK yourself](#host-the-sdk-yourself)
  - [System Requirements](#system-requirements)
  - [Next Steps](#next-steps)

## About the solution

With the MRZ Scanner, you can use your camera to scan the MRZ code from a passport or ID. The scanner extracts data such as first name, last name, document number, nationality, date of birth, expiration date, and personal number from the MRZ string, converting it into human-readable fields.

### Web demo

The web demo is available at [https://demo.dynamsoft.com/solutions/mrz-scanner/index.html]( https://demo.dynamsoft.com/solutions/mrz-scanner/index.html). Rest assured, no personal data will be uploaded.

### Run this Solution

**1. Clone the repository to a working directory or download the code as a ZIP file**

```sh
git clone https://github.com/Dynamsoft/mrz-scanner-javascript
```

**2. Deploy the files to a directory hosted on an HTTPS server**

**3. Open the "index.html" file in your browser**

> Basic Requirements
>
>  * Internet connection  
>  * [A supported browser](#system-requirements)
>  * An accessible Camera

-----

### Project structure

```text
MRZ Scanner
├── assets
│   ├── ...
│   ├── ...
│   └── ...
├── css
│   └── index.css
├── font
│   ├── ...
│   ├── ...
│   └── ...
├── js
│   ├── const.js
│   ├── index.js
│   ├── init.js
│   └── util.js
├── index.html
└── template.json
```

 * `/assets` : This directory contains all the static files such as images, icons, etc. that are used in the project.
 * `/css` : This directory contains the CSS file(s) used for styling the project.
 * `/font` : This directory contains the font files used in the project.
 * `/js` : This directory contains all the JavaScript files used in the project.
   * `const.js` : This file contains definitions of certain constants or variables used across the project.
   * `index.js`: This is the main JavaScript file where the core logic of the project is implemented.
   * `init.js` : This file is used for initialization purposes, such as initializing license, load resources, etc.
   * `util.js` : This file contains utility functions that are used across the project.
 * `index.html` : This is the main HTML file that represents the homepage of the project.
 * `template.json` : This file contains predefined templates used in the project.

> Note: A more detailed discussion about these files will be presented in the next section.

## Building your own page

In this section, we’ll walk through the key steps needed to build a web page that reads the machine-readable zone (MRZ) on a passport or ID.

### Include the SDK

The simplest way to include the SDK is to use either the [jsDelivr](https://jsdelivr.com/) or [UNPKG](https://unpkg.com/) CDN. This project uses `jsDelivr` in [`index.html`](https://github.com/Dynamsoft/mrz-scanner-javascript/blob/main/index.html).

* jsDelivr

  ```html
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-bundle@2.2.3000/dist/dcv.bundle.js"></script>
  ```

* UNPKG  

  ```html
  <script src="https://unpkg.com/dynamsoft-capture-vision-bundle@2.2.3000/dist/dcv.bundle.js"></script>
  ```

> Besides using the public CDN, you can also download the SDK from the npm and host its files on your own server or a commercial CDN before including it in your application. Please see [Host the SDK yourself](#host-the-sdk-yourself)

### Set up the solution

Before using the SDK, you need to configure a few things in [`init.js`](https://github.com/Dynamsoft/mrz-scanner-javascript/blob/main/js/init.js).

#### Specify the license

To enable the SDK's functionality, you must provide a valid license. Use the function `initLicense` to set your license key.

```javascript
Dynamsoft.License.LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9");
```

The key "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" used in this solution (found in the js/init.js file) is a test license valid for 24 hours for any newly authorized browser. If you wish to test the SDK further, you can request a 30-day free trial license through the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=mrz&utm_source=docs&package=js" target="_blank">Request a Trial License</a> link.

#### Load resources in advance

To optimize image processing in a web environment, the algorithms are compiled into WebAssembly modules (files with a .wasm extension). These modules can be quite large, but the SDK can preload them asynchronously to enhance the user experience. For better performance, we recommend using [`loadWasm()`](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/core/core-module-class.html#loadwasm) to preload the necessary libraries. Since this solution uses DCE, DLR, and DCP, only the relevant resources need to be preloaded (no need to preload .wasm resources for DCE).


```javascript
Dynamsoft.Core.CoreModule.loadWasm(["DLR", "DCP"]);
```

In addition to the .wasm files, performance can be further enhanced by preloading the parsing standards and inference models (referred to as .data files) using the methods [`loadSpec()`](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/code-parser-module-class.html#loadspec) and [`loadRecognitionData()`](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/label-recognizer-module-class.html#loadrecognitiondata), respectively.

In our solution, we preload the parsing standards for `MRTD_TD3_PASSPORT`, `MRTD_TD1_ID`, and `MRTD_TD2_ID`, along with the .data file for `MRZ` recognition.

```javascript
Dynamsoft.DCP.CodeParserModule.loadSpec("MRTD_TD3_PASSPORT");
Dynamsoft.DCP.CodeParserModule.loadSpec("MRTD_TD1_ID");
Dynamsoft.DCP.CodeParserModule.loadSpec("MRTD_TD2_ID");
Dynamsoft.DLR.LabelRecognizerModule.loadRecognitionData("MRZ");
```

> All these files are cached locally after being downloaded, so they load much faster on subsequent uses.

#### Create an CaptureVisionRouter instance and initialize the settings

The `Dynamsoft.CVR.CaptureVisionRouter.createInstance()` method creates a `CaptureVisionRouter` object, `cvRouter`, which controls the entire process. First, a [template file](https://github.com/Dynamsoft/mrz-scanner-javascript/blob/main/template.json) is loaded, where specific image processing workflows, such as "ReadPassport", "ReadId", and "ReadPassportAndId", are defined.

> If you'd like to understand the template file, refer to the [Overview of DCV parameters](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html).

```javascript
cvRouter = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await cvRouter.initSettings("./template.json");
```

#### Use the camera as the image source

`cvRouter` connects to the image source using the [ImageSourceAdapter](https://www.dynamsoft.com/capture-vision/docs/core/architecture/input.html#image-source-adapter?lang=js){:target="_blank"} interface via the `setInput()` method.

> In our case, the image source is a [CameraEnhancer](https://www.dynamsoft.com/camera-enhancer/docs/web/programming/javascript/user-guide/index.html) object, created using `Dynamsoft.DCE.CameraEnhancer.createInstance(cameraView)`.

```javascript
cameraView = await Dynamsoft.DCE.CameraView.createInstance(cameraViewContainer);
cameraEnhancer = await Dynamsoft.DCE.CameraEnhancer.createInstance(cameraView);
cvRouter.setInput(cameraEnhancer);
```

### Complete the Solution

#### Start recognition and coordinate image-processing tasks

We use `cameraEnhancer.open()` to start video streaming, and `cvRouter` begins the process by specifying a template name ("ReadPassport", "ReadId", or "ReadPassportAndId") in the `startCapturing()` method.

```javascript
await cameraEnhancer.open();
await cvRouter.startCapturing("ReadPassport");
```

#### Handle the captured result

The processing results are returned through the [CapturedResultReceiver](https://www.dynamsoft.com/capture-vision/docs/core/architecture/output.html#captured-result-receiver?lang=js){:target="_blank"} interface. The `CapturedResultReceiver` object is registered to `cvRouter` using the `addResultReceiver()` method.

```javascript
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onCapturedResultReceived = (result) => {
  const recognizedResults = result.textLineResultItems;
  const parsedResults = result.parsedResultItems;
  // Process the results according to your needs.
}
await cvRouter.addResultReceiver(resultReceiver);
```

## Host the SDK yourself

You can download the SDK from npm and host it yourself.

> Note that you need to get two other assisting packages.

```cmd
npm i dynamsoft-capture-vision-bundle@2.2.3000 -E
npm i dynamsoft-capture-vision-std@1.2.10 -E
npm i dynamsoft-image-processing@2.2.30 -E
```

The resources are located at the path node_modules/<pkg>, without @<version>, so the script in your page would be like:

<script src="node_modules/dynamsoft-capture-vision-bundle/dist/dcv.bundle.js"></script>

Since @<version> is missing, you need to specify the location of the "engine" files:

```javascript
//The following code uses the jsDelivr CDN, feel free to change it to your own location of these files
Object.assign(Dynamsoft.Core.CoreModule.engineResourcePaths, {
  "std":"https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-std@1.2.10/dist/",
  "core":"https://cdn.jsdelivr.net/npm/dynamsoft-core@3.2.30/dist/",
  "dip":"https://cdn.jsdelivr.net/npm/dynamsoft-image-processing@2.2.30/dist/",
  "license":"https://cdn.jsdelivr.net/npm/dynamsoft-license@3.2.21/dist/",
  "cvr":"https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-router@2.2.30/dist/",
  "dce":"https://cdn.jsdelivr.net/npm/dynamsoft-camera-enhancer@4.0.3/dist/",
  "dbr":"https://cdn.jsdelivr.net/npm/dynamsoft-barcode-reader@10.2.10/dist/",
  "dlr":"https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer@3.2.30/dist/",
  "dcp":"https://cdn.jsdelivr.net/npm/dynamsoft-code-parser@2.2.10/dist/",
  "ddn":"https://cdn.jsdelivr.net/npm/dynamsoft-document-normalizer@2.2.10/dist/",
  "dlrData":"https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer-data@1.0.11/dist/",
  "dnn":"https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-dnn@1.0.20/dist/",
  "utility":"https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-bundle@2.2.3000/dist/"
});
```

*Note*:

* Certain legacy web application servers may lack support for the `application/wasm` mimetype for .wasm files. To address this, you have two options:
  1. Upgrade your web application server to one that supports the `application/wasm` mimetype.
  2. Manually define the mimetype on your server. You can refer to the following resources for guidance:
     1. [Apache](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Apache_Configuration_htaccess#media_types_and_character_encodings){:target="_blank"}
     2. [IIS](https://docs.microsoft.com/en-us/iis/configuration/system.webserver/staticcontent/mimemap){:target="_blank"}
     3. [Nginx](https://www.nginx.com/resources/wiki/start/topics/examples/full/#mime-types){:target="_blank"}

* To work properly, the SDK requires a few engine files, which are relatively large and may take quite a few seconds to download. We recommend that you set a longer cache time for these engine files, to maximize the performance of your web application.

  ```cmd
  Cache-Control: max-age=31536000
  ```

  Reference: [Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control){:target="_blank"}.

## System Requirements

This project requires the following features to work:

- Secure context (HTTPS deployment)

  When deploying your application / website for production, make sure to serve it via a secure HTTPS connection. This is required for two reasons
  
  - Access to the camera video stream is only granted in a security context. Most browsers impose this restriction.
  > Some browsers like Chrome may grant the access for `http://127.0.0.1` and `http://localhost` or even for pages opened directly from the local disk (`file:///...`). This can be helpful for temporary development and test.
  
  - Dynamsoft License requires a secure context to work.

- `WebAssembly`, `Blob`, `URL`/`createObjectURL`, `Web Workers`

  The above four features are required for the SDK to work.

- `MediaDevices`/`getUserMedia`

  This API is required for in-browser video streaming.

- `getSettings`

  This API inspects the video input which is a `MediaStreamTrack` object about its constrainable properties.

The following table is a list of supported browsers based on the above requirements:

  | Browser Name |     Version      |
  | :----------: | :--------------: |
  |    Chrome    | v78+<sup>1</sup> |
  |   Firefox    | v63+<sup>1</sup> |
  |     Edge     |       v79+       |
  |    Safari    |       v14+       |

  <sup>1</sup> devices running iOS needs to be on iOS 14.3+ for camera video streaming to work in Chrome, Firefox or other Apps using webviews.

Apart from the browsers, the operating systems may impose some limitations of their own that could restrict the use of the SDK. Browser compatibility ultimately depends on whether the browser on that particular operating system supports the features listed above.

## Next Steps

Now that you have got the SDK integrated, you can choose to move forward in the following directions

1. Check out the [source code for this solution on github](https://github.com/Dynamsoft/mrz-scanner-javascript).
2. Check out the [Dynamsoft developer blog](https://www.dynamsoft.com/codepool/tag/mrz/).