---
layout: default-layout
title: Index - Dynamsoft Capture Vision JavaScript Edition
description: The introduction of Dynamsoft Capture Vision JavaScript edition.
keywords: API reference, guide, JavaScript
needAutoGenerateSidebar: true
---

# Dynamsoft Capture Vision Documentation for JavaScript Edition

For both video and static image processing with Dynamsoft Capture Vision(DCV), a specific task can be broken down into three stages: Input, Image Processing, and Output.

- `Input`: DCV retrieves images from the Image Source Adapter (ISA). In the JavaScript edition, DCE is the most commonly used ISA.

- `Image Processing`: This part is compiled into WASM format, which has a small size. Asynchronously preloading it when known modules might be used also enhances efficiency. Image processing is a computationally intensive task, and delegating it to WASM significantly boosts product performance.

- `Output`: As images are processed, various types of results can be produced. Capture Vision Router(CVR) collects the desired results through the Captured Result Receiver (CRR). In the JavaScript edition, DCE can also be utilized to achieve UI effects and visualize these collected results.

The design of DCV empowers developers to effortlessly build conceptual prototypes within hours, while also providing the flexibility for complex customizations to handle more demanding tasks. In the code, all that needs to be done is to create the required instances and define the input and output contents. The specific tasks, task dependencies, and image processing details are defined by the parameter template. Consequently, even if the business needs change or more image processing functionality, such as barcode reading, text recognition, edge detection, etc., needs to be added, minimal code modifications are necessary. Achieving these goals can be accomplished by adjusting the parameter template.

## Get Started with DCV JavaScript Edition

The best way to get started with Dynamsoft Capture Vision JavaScript Edition is to follow the [User Guide](user-guide/index.md) to build your first barcode reading application.

## Check APIs

For a complete list of available APIs, read [API Reference](api-reference/index.md).

## Read about CaptureVisionTemplate

[CaptureVisionTemplate](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html) represents the flow of image processing. In addition to rewriting CaptureVisionTemplate, it is also possible to modify the preset templates to achieve a similar purpose, but it should be noted that not all parameters are currently open in the setup, and only a few parameters that have a significant impact on the image processing task are reserved for quick adjustment.

## Contact Us

<a href = "https://www.dynamsoft.com/company/customer-service/#contact" target = "_blank">Feel free to contact us if you have any questions.</a>