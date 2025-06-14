---
layout: default-layout
title: CaptureVisionRouter Settings - Dynamsoft Capture Vision JavaScript Edition API
description: This page introduces APIs related to the Settings of CaptureVisionRouter of Dynamsoft Capture Vision JavaScript Edition.
keywords: capture vision, router, Settings, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: CVR JavaScript CaptureVisionRouter
---

# CaptureVisionRouter Settings

| Name                                              | Description                                                                                                                                                            |
| ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [initSettings()](#initsettings)                   | Configures runtime settings using a provided JSON string, an object, or a URL pointing to an object, which contains settings for one or more `CaptureVisionTemplates`. |
| [outputSettings()](#outputsettings)               | Outputs a `CaptureVisionTemplate` specified by its name.                                                                                                               |
| [outputSettingsToFile](#outputsettingstofile)     | Generates a Blob object or initiates a JSON file download containing the settings for the specified `CaptureVisionTemplate`.                                           |
| [getSimplifiedSettings()](#getsimplifiedsettings) | Retrieves a JSON object that contains simplified settings for the specified `CaptureVisionTemplate`.                                                                   |
| [getTemplateNames()](#gettemplatenames)           | Retrieves the names of all the currently available templates.                         |
| [updateSettings()](#updatesettings)               | Updates the specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object.                                                                |
| [resetSettings()](#resetsettings)                 | Restores all runtime settings to their original default values.                                                                                                        |


## initSettings

Configures runtime settings using a provided JSON string, an object, or a URL pointing to an object, which contains settings for one or more `CaptureVisionTemplates`.

**Syntax**

```typescript
initSettings(settings: string | object): Promise<any>;
```

**Parameters**

`settings`: A JSON string, an object, or a URL pointing to an object that contains settings for one or more `CaptureVisionTemplates`.

**Return value**

A promise that resolves when the operation has completed. It provides an object that describes the result.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const settings = {
  "CaptureVisionTemplates": [
    {
      "Name": "ReadSingleBarcode",
      "ImageROIProcessingNameArray": ["roi-read-single-barcode"]
    }
  ],
  "TargetROIDefOptions": [
    {
      "Name": "roi-read-single-barcode",
      "TaskSettingNameArray": ["task-read-single-barcode"]
    }
  ],
  "BarcodeReaderTaskSettingOptions": [
    {
      "Name": "task-read-single-barcode"
    }
  ]
};
await router.initSettings(settings);

// Later in the code, specify the name of the template to use (e.g., "ReadSingleBarcode" in the sample template). 
router.startCapturing("NAME-OF-TEMPLATE-TO-USE"); 
```

**See Also**

[Structure of a Parameter Template File](https://www.dynamsoft.com/capture-vision/docs/core/parameters/file/index.html#structure-of-a-parameter-template-file)

## outputSettings

Returns an object that contains settings for the specified `CaptureVisionTemplate`.

**Syntax**

```typescript
outputSettings(templateName: string, includeDefaultValues?: boolean): Promise<string>;
```

**Parameters**

`templateName`: specifies a `CaptureVisionTemplate` by its name. If passed "*", the returned object will contain all templates.

`includeDefaultValues` (optional): Boolean that specifies whether to include default values the output. Default to False.

**Return value**

A promise that resolves with the object that contains settings for the specified template or all templates.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const settings = await router.outputSettings("ReadSingleBarcode");
console.log(settings);
```

## outputSettingsToFile

Generates a Blob object or initiates a JSON file download containing the settings for the specified `CaptureVisionTemplate`.

**Syntax**

```typescript
outputSettingsToFile(templateName: string, fileName: string, download?: boolean, includeDefaultValues?: boolean): Promise<Blob>;
```

**Parameters**

`templateName`: specifies a `CaptureVisionTemplate` by its name. If passed "*", the returned object will contain all templates.

`fileName`: specifies the name of the file.

`download` (optional): boolean that specifies whether to initiates a JSON file download.

`includeDefaultValues` (optional): Boolean that specifies whether to include default values the output. Default to False.

**Return value**

A promise that resolves with the Blob object that contains settings for the specified template or all templates.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const settings = await router.outputSettingsToFile("ReadSingleBarcode", "read-single-file", true, true);
console.log(settings);
```

## getSimplifiedSettings

Retrieves a JSON object that contains simplified settings for the specified `CaptureVisionTemplate`.

**Syntax**

```typescript
getSimplifiedSettings(templateName: string): Promise<SimplifiedCaptureVisionSettings>;
```

**Parameters**

`templateName`: specifies a `CaptureVisionTemplate` by its name.

**Return Value**

A promise that resolves with a JSON object, of type `SimplifiedCaptureVisionSettings`, which represents the simplified settings for the specified template.

> Remarks: If the settings of the specified template are too complex, we cannot create a SimplifiedCaptureVisionSettings, and as a result, it will return an error.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
settings = await router.getSimplifiedSettings("ReadSingleBarcode");
```

## getTemplateNames

Retrieves the names of all the currently available templates.

**Syntax**

```typescript
getTemplateNames(): Promise<Array<string>>;;
```

**Return Value**

A promise that resolves with an array of string, which represents the names of currently available templates

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let template_names = await router.getTemplateNames();
```

## updateSettings

Updates the specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object.

**Syntax**

```typescript
updateSettings(templateName: string, settings: SimplifiedCaptureVisionSettings): Promise<any>;
```

**Parameters**

`templateName`: specifies a `CaptureVisionTemplate` by its name.

`settings`: the `SimplifiedCaptureVisionSettings` object that contains updated settings.

**Return value**

A promise that resolves when the operation has completed. It provides an object that describes the result.

**Code snippet**

```javascript
let settings = await router.getSimplifiedSettings("ReadSingleBarcode");
settings.barcodeSettings.barcodeFormatIds =
  Dynamsoft.DBR.EnumBarcodeFormat.BF_QR_CODE;
await router.updateSettings("ReadSingleBarcode", settings);
await router.startCapturing("ReadSingleBarcode");
```

## resetSettings

Restores all runtime settings to their original default values.

**Syntax**

```typescript
resetSettings(): Promise<any>;
```

**Parameters**

None

**Return Value**

A promise that resolves when the operation has completed. It provides an object that describes the result.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await router.resetSettings();
```
