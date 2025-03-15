---
layout: default-layout
title: Index - Dynamsoft Capture Vision JavaScript Edition
description: The introduction of Dynamsoft Capture Vision JavaScript edition.
keywords: API reference, guide, JavaScript
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# Dynamsoft Capture Vision JavaScript Edition - Documentation

**Dynamsoft Capture Vision (DCV)** is a comprehensive SDK that integrates various functional products. It encompasses image capture, content understanding, result parsing, and interactive workflow. Essentially, DCV processes images to extract specific information that is meaningful within a business context.

DCV is designed to enable developers to quickly create conceptual prototypes within hours. It also offers the flexibility to handle more complex customizations for demanding tasks.

> For more information, visit [Dynamsoft Capture Vision](https://www.dynamsoft.com/capture-vision/docs/core/introduction/).

This documentation provides guidance to assist developers in utilizing DCV for web applications typically run in browsers.

## Implementation Differences

Implementing DCV, regardless of platform or language, involves three stages: input, image processing, and output. However, differences arise due to use cases or technical limitations. When implementing DCV in JavaScript, consider the following:

- `Input`: DCV obtains images from an Image Source based on the [Image Source Adapter (ISA)](https://www.dynamsoft.com/capture-vision/docs/core/architecture/input.html#image-source-adapter) interface. In web applications, these images are usually captured from live video, with the SDK [Dynamsoft Camera Enhancer](https://www.dynamsoft.com/camera-enhancer/docs/introduction/) being the most commonly used Image Source.

- `Image Processing`: DCV processes the images to derive information, powered by Dynamsoft's cutting-edge algorithms. To ensure efficient operation in web environments like browsers, these algorithms are compiled into [WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly) modules (.wasm files). These modules are large in size, and DCV can asynchronously preload them into the web page to enhance user experience.

- `Output`: The derived information is made available to other business logic through the [Captured Result Receiver (CRR)](https://www.dynamsoft.com/capture-vision/docs/core/architecture/output.html#captured-result-receiver) interface. In web applications, real-time interaction is crucial. DCV leverages Dynamsoft Camera Enhancer’s UI functionality to display results at runtime and, in some cases, allows user intervention to improve results.

## Using the SDK

### Get started

The best way to begin with Dynamsoft Capture Vision JavaScript Edition is to follow the User Guide for specific use cases.

- [User Guide for Dynamsoft Barcode Reader](https://www.dynamsoft.com/barcode-reader/docs/web/programming/javascript/user-guide/index.html){:target="_blank"}

- [User Guide for MRZ Scanner](https://www.dynamsoft.com/mrz-scanner/docs/web/guides/mrz-scanner.html){:target="_blank"}

- [User Guide for Document Scanner](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/user-guide/index.html)

### Check APIs

While the guide covers common APIs, more detailed explanations of these and other APIs can be found in the [API Reference](api-reference/index.md).

### Read about CaptureVisionTemplate

Using DCV in JavaScript involves:

1. Creating a `CaptureVisionRouter` instance.
2. Defining and binding an image source and a result receiver to the instance.
3. Specifying a template which defines how to process images.

Apparently, the use of DCV varies with the choice of template. Dynamsoft provides popular preset templates and will add more over time. To understand, adjust, or define your own template, read about [CaptureVisionTemplate](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html).

## Assumptions

This documentation assumes familiarity with the [Architecture of Dynamsoft Capture Vision](https://www.dynamsoft.com/capture-vision/docs/core/architecture/) and the technologies [HTML](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML), [CSS](https://developer.mozilla.org/docs/Learn/CSS/First_steps), and [JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/A_re-introduction_to_JavaScript).

## Contact Us

Feel free to <a href = "https://www.dynamsoft.com/company/customer-service/#contact" target = "_blank">contact us</a> if you have any questions.