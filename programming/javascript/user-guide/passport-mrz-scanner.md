---
layout: default-layout
title: Scan & Parse Passport - Dynamsoft Capture Vision JavaScript Edition
description: This page introduce how to scan and parse a passport MRZ with Dynamsoft Capture Vision JavaScript Edition.
keywords: JavaScript, passport
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Passport MRZ Scanner Solution for Your Website - User Guide

![version](https://img.shields.io/npm/v/dynamsoft-label-recognizer.svg)
![downloads](https://img.shields.io/npm/dm/dynamsoft-label-recognizer.svg)
![jsdelivr](https://img.shields.io/jsdelivr/npm/hm/dynamsoft-label-recognizer.svg)

This guide will walk you through the step-by-step process of how to creating a simple passport MRZ scanner solution.

<span style="font-size:20px">Table of Contents</span>

- [Passport MRZ Scanner Solution for Your Website - User Guide](#passport-mrz-scanner-solution-for-your-website---user-guide)
  - [About the solution](#about-the-solution)
    - [Web demo](#web-demo)
    - [Run this Solution](#run-this-solution)
    - [Project structure](#project-structure)
  - [Building your own page](#building-your-own-page)
    - [Add Required Products](#add-required-products)
      - [Use a CDN](#use-a-cdn)
    - [Set Up the Solution](#set-up-the-solution)
      - [Specify the license](#specify-the-license)
      - [Load resources in advance](#load-resources-in-advance)
      - [Create instance and initialize the settings](#create-instance-and-initialize-the-settings)
      - [Use the camera as the image source](#use-the-camera-as-the-image-source)
    - [Complete the Solution](#complete-the-solution)
      - [Start the recognition and coordinate image-processing tasks](#start-the-recognition-and-coordinate-image-processing-tasks)
      - [Handle the captured result](#handle-the-captured-result)
  - [System Requirements](#system-requirements)
  - [Next Steps](#next-steps)

## About the solution

With Passport MRZ Scanner you can use your camera to scan the MRZ code of a passport. It will extract all data like firstname, lastname, passport number, nationality, date of birth, expiration date and personal number from the MRZ string, and converts the encoded string into human-readable fields.

### Web demo

The web demo is available at [https://demo.dynamsoft.com/solutions/passport-scanner/index.html]( https://demo.dynamsoft.com/solutions/passport-scanner/index.html) (nothing will be uploaded).

### Run this Solution

1. Clone the repo to a working directory

```sh
git clone https://github.com/Dynamsoft/passport-MRZ-scanner-javascript
```

2. CD to the folder and run an https server

```sh
cd passport-MRZ-scanner-javascript
```

> Basic Requirements
>
>  * Internet connection  
>  * [A supported browser](#system-requirements)
>  * An accessible Camera

-----

### Project structure

```text
Passport MRZ Scanner
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
│   ├── define.js
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
   * `define.js` : This file contains definitions of certain constants or variables used across the project.
   * `index.js`: This is the main JavaScript file where the core logic of the project is implemented.
   * `init.js` : This file is used for initialization purposes, such as initializing license, load resources, etc.
   * `util.js` : This file contains utility functions that are used across the project.
 * `index.html` : This is the main HTML file that represents the homepage of the project.
 * `template.json` : This file contains predefined templates used in the project.

> Note: A more detailed discussion about these files will be presented in the next section.

## Building your own page

In this section, we'll break down and show some important steps required to build a web page that reads the machine readable zone (MRZ) on a passport.

### Add Required Products

To build the MRZ scanner solution, we use three functional products from Dynamsoft

- [Dynamsoft Camera Enhancer](https://www.dynamsoft.com/camera-enhancer/docs/core/introduction/index.html)(DCE) for fetching video stream as input
- [Dynamsoft Label Recognizer](https://www.dynamsoft.com/label-recognition/overview/?utm_content=nav-products)(DLR) for recognizing text in images
- [Dynamsoft Code Parser](https://www.dynamsoft.com/code-parser/docs/core/introduction/)(DCP) for parsing the recognized text.

Besides the three mentioned above, a few common modules are also necessary. Here are all the resource files needed for this solution:

1. `core.js`: encompasses common classes, interfaces, and enumerations shared across all Dynamsoft SDKs.
2. `license.js`: introduces the LicenseManager class, which manages the licensing for all Dynamsoft SDKs.
3. `utility.js`: encompasses auxiliary classes shared among all Dynamsoft SDKs.
4. `dlr.js`: defines interfaces and enumerations tailored to the label recognizer module.
5. `dcp.js`: provides the ability for converting data strings, typically encrypted in barcodes and machine-readable zones, into human-readable information.
6. `cvr.js`: introduces the CaptureVisionRouter class, which governs the entire image processing workflow.
7. `dce.js`: comprises classes that offer camera support and basic user interface functionalities.

#### Use a CDN

The simplest way to include the SDKs is to use either the [jsDelivr](https://jsdelivr.com/) or [UNPKG](https://unpkg.com/) CDN. This project uses `jsDelivr` in [`index.html`](https://github.com/Dynamsoft/passport-MRZ-scanner-javascript/blob/main/index.html).

* jsDelivr

  ```html
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-core@3.2.30/dist/core.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-license@3.2.21/dist/license.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-utility@1.2.20/dist/utility.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer@3.2.30/dist/dlr.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-code-parser@2.2.10/dist/dcp.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-router@2.2.30/dist/cvr.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/dynamsoft-camera-enhancer@4.0.3/dist/dce.js"></script>
  ```

* UNPKG  

  ```html
  <script src="https://unpkg.com/dynamsoft-core@3.2.30/dist/core.js"></script>
  <script src="https://unpkg.com/dynamsoft-license@3.2.21/dist/license.js"></script>
  <script src="https://unpkg.com/dynamsoft-utility@1.2.20/dist/utility.js"></script>
  <script src="https://unpkg.com/dynamsoft-label-recognizer@3.2.30/dist/dlr.js"></script>
  <script src="https://unpkg.com/dynamsoft-code-parser@2.2.10/dist/dcp.js"></script>
  <script src="https://unpkg.com/dynamsoft-capture-vision-router@2.2.30/dist/cvr.js"></script>
  <script src="https://unpkg.com/dynamsoft-camera-enhancer@4.0.3/dist/dce.js"></script>
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

### Set Up the Solution

Before using the SDK, you need to configure a few things in [`init.js`](https://github.com/Dynamsoft/passport-MRZ-scanner-javascript/blob/main/js/init.js).

#### Specify the license

To enable the SDK's functionality, you must provide a valid license. Use the function `initLicense` to set your license key.

```javascript
Dynamsoft.License.LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9");
```

The key "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" serves as a test license valid for 24 hours, applicable to any newly authorized browser. To test the SDK further, you can request a 30-day free trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=passport&utm_source=docs&package=js" target="_blank">Request a Trial License</a> link.

#### Load resources in advance

To make image processing as efficient as possible in a web environment, the algorithms are compiled into WebAssembly modules (files with the extension .wasm). These modules are considered large in a web environment, and DCV has the ability to asynchronously preload them into the web page to improve user experience. For enhancing speed, we advise utilizing [`loadWasm()`](https://www.dynamsoft.com/capture-vision/docs/web/programming/javascript/api-reference/core/core-module-class.html#loadwasm) to preload the libraries. Because the functional products used in this solution are DCE, DLR, and DCP, we can preload the resources related to them here (no need to load .wasm resources for DCE).

The [`loadSpec()`](https://www.dynamsoft.com/code-parser/docs/web/programming/javascript/api-reference/code-parser-module-class.html#loadspec) method loads the parsing standardization associated with `MRTD_TD3_PASSPORT`. The biggest challenge when dealing with IDs, driver’s licenses, or different types of passports is the standard specifications. In the design of DCP, we have broken down these specifications into smaller units and loaded them in the form of external resources. The advantage of this is that it can be loaded according to actual needs to save resources, and when new standard specifications appear, it can quickly provide support without the need to upgrade the SDK itself. Here you can find [all the code types supported](https://www.dynamsoft.com/code-parser/docs/core/code-types/) by DCP.

The last essential resources are the inference models (referred to as the .data file in the following text). The text recognition function of DLR combines the advantages of CNN (Convolutional Neural Networks) models and traditional image feature extraction, so it relies on the .data file to work. Essentially, text recognition is a classification task. The fewer categories that need to be distinguished, the higher accuracy the model may achieve. Therefore, DLR also provides many models for selection based on actual needs. Additionally, DLR also supports dataset training in order to generate customized recognition models. In this solution we use .date file named `MRZ`.
These .data files are loaded from the server on demand at runtime which could be time-consuming. To make the process user-friendly, it's recommended to load them in advance by calling [`loadRecognitionData()`](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/label-recognizer-module-class.html#loadrecognitiondata).

> These files are cached locally as soon as they are downloaded, so they load very quickly from the second time on.

```javascript
Dynamsoft.Core.CoreModule.loadWasm(["DLR", "DCP"]);
Dynamsoft.DCP.CodeParserModule.loadSpec("MRTD_TD3_PASSPORT");
Dynamsoft.DLR.LabelRecognizerModule.loadRecognitionData("MRZ");
```

#### Create instance and initialize the settings

The method `Dynamsoft.CVR.CaptureVisionRouter.createInstance()` creates a `CaptureVisionRouter` object `cvRouter`, which controls the entire process. First, we load a [template file](https://github.com/Dynamsoft/passport-MRZ-scanner-javascript/blob/main/template.json), in which the specific image processing workflow `ReadPassport` is defined.

> The workflows defined in the template file are customizable, which allows developers to configure multiple tasks and their dependencies based on their specific needs. The individual tasks supported by DCV include barcode recognition, text recognition, document detection and normalization, and result parsing. In addition, developers can accomplish more complex tasks by configuring dependencies and conditions between different tasks.
>
> For more information about the template file, please refer to [Overview of DCV parameters](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html). If you need to customize a special workflow, you can [contact us](https://www.dynamsoft.com/contact/){:target="_blank"}.

```javascript
cvRouter = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await cvRouter.initSettings("./template.json");
```

#### Use the camera as the image source

`cvRouter` connects to the image source through the [ImageSourceAdapter](https://www.dynamsoft.com/capture-vision/docs/core/architecture/input.html#image-source-adapter?lang=js){:target="_blank"} interface with the method `setInput()`.

> The image source in our case is a [CameraEnhancer](https://www.dynamsoft.com/camera-enhancer/docs/web/programming/javascript/user-guide/index.html) object created with `Dynamsoft.DCE.CameraEnhancer.createInstance(cameraView)`.

```javascript
cameraView = await Dynamsoft.DCE.CameraView.createInstance(cameraViewContainer);
cameraEnhancer = await Dynamsoft.DCE.CameraEnhancer.createInstance(cameraView);
cvRouter.setInput(cameraEnhancer);
```

### Complete the Solution

#### Start the recognition and coordinate image-processing tasks

We use `cameraEnhancer.open()` to start the video streaming, and `cvRouter` will start the process by specifying a template name "ReadPassport" in the method `startCapturing()`. Here, "ReadPassport" is a workflow that we have predefined in the [template.json](https://github.com/Dynamsoft/passport-MRZ-scanner-javascript/blob/main/template.json). In this workflow, we specify a recognition region, the specific tasks to be performed in that region, and the details of the image processing operations when performing these tasks. The existence of the template file is a distinctive characteristic of the Dynamsoft Capture Vision architecture, allowing you to encapsulate specific business logic within this template. This eliminates the need for code rewriting when the same business logic is required on other platforms — simply utilizing the same template facilitates seamless porting.

```javascript
await cameraEnhancer.open();
await cvRouter.startCapturing("ReadPassport");
```

#### Handle the captured result

The processing results are returned through the [CapturedResultReceiver](https://www.dynamsoft.com/capture-vision/docs/core/architecture/output.html#captured-result-receiver?lang=js){:target="_blank"} interface. The `CapturedResultReceiver` object is registered to `cvRouter` via the method `addResultReceiver()`.

```javascript
const resultReceiver = new Dynamsoft.CVR.CapturedResultReceiver();
resultReceiver.onCapturedResultReceived = (result) => {
  const recognizedResults = result.textLineResultItems;
  const parsedResults = result.parsedResultItems;
  // Process the results according to your needs.
}
await cvRouter.addResultReceiver(resultReceiver);
```

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

1. Check out the official demo [MRZ Scanner](https://demo.dynamsoft.com/label-recognizer-js/mrz-scanner.html), which can handle more MRZ types than just passports.
2. Check out the [source code for this solution on github](https://github.com/Dynamsoft/passport-MRZ-scanner-javascript).
3. Check out the [Dynamsoft developer blog](https://www.dynamsoft.com/codepool/tag/mrz/).
