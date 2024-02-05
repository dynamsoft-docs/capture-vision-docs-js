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

| Name                                         | Description                                                                                              |
| ------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| [initSettings()](#initsettings)                   | Configures runtime settings using a provided JSON string, an object, or a URL pointing to an object, which contains settings for one or more `CaptureVisionTemplates`.           |
| [outputSettings()](#outputsettings)               | Outputs a `CaptureVisionTemplate` specified by its name.                                                 |
| [getSimplifiedSettings()](#getsimplifiedsettings) | Returns a `SimplifiedCaptureVisionSettings` object for manipulating a specified `CaptureVisionTemplate`. |
| [updateSettings()](#updatesettings)               | Updates the specified `CaptureVisionTemplate` with an updated `SimplifiedCaptureVisionSettings` object.    |
| [resetSettings()](#resetsettings)                 | Restores all runtime settings to their original default values.                                                                      |


## initSettings

Initializes the Runtime Settings with the settings in the given JSON string.

**Syntax**

```typescript
initSettings(settings: string): Promise<void>;
```

**Parameters**


`settings`: A JSON string containing the configuration settings for the CaptureVisionRouter.

**Return value**

Returns a promise that resolves when the settings have been successfully initialized.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const settings = {
  "CaptureVisionTemplates": [
    {
      "Name": "ReadBarcodes_my_setting",
    }
  ],
};
await router.initSettings(settings);
```

## outputSettings

Returns the settings of the CaptureVisionRouter as a JSON string.

**Syntax**

```typescript
outputSettings(templateName?: string): Promise<string>;
```

**Parameters**

`templateName`(optional): The name of the template for which to output the settings. If not specified, the settings currently in effect will be returned.

**Return value**

Returns a promise that resolves with the JSON string representing the settings.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const settings = await router.outputSettings();
console.log(settings);
```

## getSimplifiedSettings

Retrieves the simplified settings for a specific template from the CaptureVisionRouter.

**Syntax**

```typescript
getSimplifiedSettings(templateName: string): Promise<SimplifiedCaptureVisionSettings | null>;
```

**Parameters**

`templateName`: The name of the template for which to retrieve the simplified settings.

**Return Value**

Returns a promise that resolves with a SimplifiedCaptureVisionSettings object representing the simplified settings for the specified template.

> Remarks: If the underlying CaptureSettings is too complicated, we cannot construct a Simplified CaptureSettings in which case it returns null.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
settings = await router.getSimplifiedSettings();
```

## updateSettings

Updates a few key settings of a template with new values.

**Syntax**

```typescript
updateSettings(templateName: string, settings: SimplifiedCaptureVisionSettings): Promise<void>;
```

**Parameters**

`templateName`: The name of the template to be updated with the provided settings.

`settings`: The SimplifiedCaptureVisionSettings object containing the new values for the template.

**Return Value**

Returns a promise that resolves when the template settings have been successfully updated.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
let newSettings = await router.getSimplifiedSettings("normalize-document");
await router.updateSettings("normalize-document", newSettings);
```

> Note: The updateSettings method allows you to update a template's settings with new values. It is specifically designed for fast configuration of the image processing process, with certain limitations:

> 1. There can only be one target region of interest (ROI), typically the input image itself.
> 2. For the ROI, the SDK processes it only once.
> 3. The processes within the template are independent and do not rely on each other.

## resetSettings

Resets all settings of the CaptureVisionRouter to their default values.

**Syntax**

```typescript
resetSettings(): Promise<void>;
```

**Parameters**

None

**Return Value**

Returns a promise that resolves when the settings have been successfully reset to their default values.

**Code snippet**

```javascript
let router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
await router.resetSettings();
```

> Note: The resetSettings method allows you to reset all settings of the CaptureVisionRouter instance to their default values. This can be useful when you want to start with a clean slate and remove any custom configurations. It is important to note that the default values may vary depending on the specific edition, such as the JavaScript edition, which may have slightly different defaults compared to other editions like C++.