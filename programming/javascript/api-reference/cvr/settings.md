---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the Settings of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Settings, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
permalink: /programming/javascript/api-reference/cvr/settings.html
---

# Javascript API Reference - `CaptureVisionRouter` Instantiation

| API Name                                          | Description                                                                  |
| ------------------------------------------------- | ---------------------------------------------------------------------------- |
| [initSettings()](#getruntimesettings)             | Returns the current runtime settings.                                        |
| [outputSettings](#initruntimesettingswithstring)  | Initializes the Runtime Settings with the settings in the given JSON string. |
| [getSimplifiedSettings()](#updateruntimesettings) | Updates runtime settings with a given struct or a preset template.           |
| [updateSettings()](#resetruntimesettings)         | Resets all parameters to default values.                                     |
| [resetSettings()](#outputruntimesettingstostring) | Return the current RuntimeSettings in the form of a string.                  |


## createInstance

Initializes a new instance of the `CaptureVisionRouter` class.

```typescript
Dynamsoft.CVR.CaptureVisionRouter.createInstance: () => Promise<CaptureVisionRouter>;
```

### Return value

A promise that resolves to the initalized `CaptureVisionRouter` object.

### Code Snippet

```js
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
```