---
layout: default-layout
title: Index - Dynamsoft Capture Vision JavaScript Edition
description: The introduction of Dynamsoft Capture Vision JavaScript edition.
keywords: API reference, guide, JavaScript
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# Dynamsoft Capture Vision JavaScript Edition - Documentation

Dynamsoft Capture Vision (DCV) is an aggregated SDK for a series of specific function products covering image capture, content understanding, result parsing and interactive workflow. In short, it obtains and processes images to derive their specific information that is meaningful in a business context.

The design of DCV empowers developers to effortlessly build conceptual prototypes within hours, while also providing the flexibility for complex customizations to handle more demanding tasks.

> Learn more about [Dynamsoft Capture Vision](https://www.dynamsoft.com/capture-vision/docs/core/introduction/).

These documents discuss the implementation of DCV in JavaScript and are intended to help developers learn and use DCV in web applications that typically run in the browser.

## Implementation Differences

For DCV, no matter which platform or language it is implemented in, a specific task can always be divided into three stages: input, image processing, and output. However, there are often some differences between these implementations due to typical use cases or technical limitations. When implementing DCV in JavaScript, our considerations are as follows:

- `Input`: at this stage, DCV obtains images from an [Image Source Adapter (ISA)](https://www.dynamsoft.com/capture-vision/docs/core/architecture/input.html#image-source-adapter). In web applications, these images are usually captured from live video, and the SDK [Dynamsoft Camera Enhancer](https://www.dynamsoft.com/camera-enhancer/docs/introduction/) is the most commonly used ISA.

- `Image Processing`: at this stage, DCV processes the images and derives information from them. This is the essential part of the task and is powered by the cutting-edge algorithms developed by Dynamsoft. To make these algorithms work as efficiently as possible in a web environment such as a browser, they are compiled into [WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly) modules (files withe the extension `.wasm`). These modules are considered large in size in a web environment, and DCV has the ability to asynchronously preload them into the web page to improve user experience.

- `Output`: this is the last stage of a DCV task, at which the derived information is made available to other business logic. The information comes in the form of various types of results through the [Captured Result Receiver (CRR)](https://www.dynamsoft.com/capture-vision/docs/core/architecture/output.html#captured-result-receiver) interface. In web applications, real-time interaction is important. Therefore, DCV leverages Dynamsoft Camera Enhancer's UI functionality to display results at runtime and in some cases allow user intervention to get better results.

## Using the SDK

### Get started

The best way to get started with Dynamsoft Capture Vision JavaScript Edition is to follow the [User Guide](user-guide/index.md) to build your first barcode reading application.

### Check APIs

While the guide has introduced all the common APIs, you can find more detailed explanation of them and other APIs in the [API Reference](api-reference/index.md).

### Read about CaptureVisionTemplate

As with other implementations of DCV, in JavaScript, all that needs to be done to use DCV are

1. Create a CaptureVisionRouter instance
2. Define and bind to the instance an image source and a result receiver
3. Choose a task to be carried out by specifying a template

Obviously, the difference in the use of DCV in different applications lies in the choice of template. Dynamsoft provides some popular built-in templates and will add more options over time. However, you may want to understand an existing template, try to adjust it or even define your own template. To learn more, you can read about [CaptureVisionTemplate](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html).

## Assumptions

These documents assume you are already familiar with the [Architecture of Dynamsoft Capture Visio](https://www.dynamsoft.com/capture-vision/docs/core/architecture/) and the technologies [HTML](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML), [CSS](https://developer.mozilla.org/docs/Learn/CSS/First_steps), and [JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/A_re-introduction_to_JavaScript).

## Contact Us

Feel free to <a href = "https://www.dynamsoft.com/company/customer-service/#contact" target = "_blank">contact us</a> if you have any questions.