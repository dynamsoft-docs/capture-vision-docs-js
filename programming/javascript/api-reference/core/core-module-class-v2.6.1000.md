---
layout: default-layout
title: API Reference Index - CoreModule Class in JavaScript
description: This page introduces the API for the CoreModule Class.
keywords: Core, CoreModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---
<!--v3.0.20--Updated on 11/23/2023-->

# CoreModule Class

The CoreModule class defines common functionality in the Core module.

| Name                                                 | Description                                                                                       |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `static` [detectEnvironment()](#detectenvironment)   | Detects and returns information about the current runtime environment.                            |
| `static` [engineResourcePaths](#engineresourcepaths) | Configures the paths where the .wasm files and other necessary resources for modules are located. |
| `static` [getVersion()](#getversion)                 | Returns the version of the Core module.                                                           |
| `static` [isModuleLoaded()](#ismoduleloaded)         | Returns whether the WebAssembly (.wasm) file for the specified module is successfully loaded.     |
| `static` [loadWasm()](#loadwasm)                     | Initiates the loading process for the .wasm file(s) corresponding to the specified module(s).     |

<!-- 
| `static` [onLog](#onlog)                             | Event triggered whenever a log message is ready to be dispatched.                           |
| `static` [disableLogging()](#disablelogging)         | Disables logging.                                                                           |
| `static` [enableLogging()](#enablelogging)           | Enables logging to print internal logs to the browser console for debugging.                | -->

## detectEnvironment

Detects and returns information about the current runtime environment.

```typescript
detectEnvironment(): Promise<any>
```

**Return Value**

A promise that resolves with the detected environment information (e.g., browser type and version, operating system, camera support, etc.).

**Code snippet**

```javascript
await Dynamsoft.Core.CoreModule.detectEnvironment();
// Example return value:
// {"wasm":true,"worker":true,"getUserMedia":true,"camera":true,"browser":"Edge","version":119,"OS":"Windows"}
```

## engineResourcePaths

Configures the paths where the .wasm files and other necessary resources for modules are located. It allows you to either return or set the paths that the system uses to find these resources.

For resources loaded from popular CDNs like jsDelivr or UNPKG, the paths are automatically identified based on the JavaScript files referenced for these modules. Manual specification of these paths is necessary only in the following scenarios:

1. When integrating the SDK within web frameworks such as Angular, React, or Vue.
2. If you opt for a CDN different from the default choices.
3. When you are serving the files on your own.

<!-- 
> Specifying only the "rootDirectory" configures all paths to align with this directory automatically. However, if you provide both "rootDirectory" and specific paths for individual modules, the specific module paths will override the root directory setting.
    /** NOT WORKING AS EXPECTED YET
     * Specifies the root directory in which all the modules are located
     */ 
    "rootDirectory"?: string;
    /** WILL BE RENAMED TO dlrData LATER
     * Specifies the resource path for the dynamsoft-capture-vision-dnn module.
     */ 
    "dcm"?: string;
    /** NOT AVAILABLE NOW
     * Specifies the resource path for the dynamsoft-capture-vision-dnn module.
     */ 
    "dnn"?: string;
-->
```typescript
static engineResourcePaths: {
    /**
     * Specifies the root directory in which all the modules are located
     */ 
    "rootDirectory"?: string;
    /**
     * Specifies the resource path for the dynamsoft-capture-vision-std module.
     */
    "std"?: string;
    /**
     * Specifies the resource path for the dynamsoft-image-processing module.
     */
    "dip"?: string;
    /**
     * Specifies the resource path for the dynamsoft-core module.
     */
    "core"?: string;
    /**
     * Specifies the resource path for the dynamsoft-license module.
     */
    "license"?: string;
    /**
     * Specifies the resource path for the dynamsoft-capture-vision-router module.
     */
    "cvr"?: string;
    /**
     * Specifies the resource path for the dynamsoft-utility module.
     */
    "utility"?: string;
    /**
     * Specifies the resource path for the dynamsoft-barcode-reader module.
     */
    "dbr"?: string;
    /**
     * Specifies the resource path for the dynamsoft-label-recognizer module.
     */
    "dlr"?: string;
    /**
     * Specifies the resource path for the dynamsoft-document-normalizer module.
     */
    "ddn"?: string;
    /**
     * Specifies the resource path for the dynamsoft-code-parser module.
     */
    "dcp"?: string;
    /**
     * Specifies the resource path for the dynamsoft-camera-enhancer module.
     */
    "dce"?: string;
};
```

**Code snippet**

```javascript
// To specify the path for rootDirectory
Dynamsoft.Core.CoreModule.engineResourcePaths.rootDirectory = "https://cdn.jsdelivr.net/npm/";
// To specify the paths for multiple modules:
Dynamsoft.Core.CoreModule.engineResourcePaths = {
    "std": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-capture-vision-std@1.0.0/dist/",
    "dip": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-image-processing@2.0.20/dist/",
    "core": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-core@3.0.20/dist/",
    "license": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-license@3.0.20/dist/",
    "cvr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-capture-vision-router@2.0.20/dist/",
    "utility": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-utility@1.0.20/dist/",
    "dbr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-barcode-reader@10.0.20/dist/"
    "dlr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-label-recognizer@3.0.20/dist/",
    "ddn": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-document-normalizer@2.0.20/dist/"
    "dcp": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-code-parser@2.0.20/dist/"
};
// To specify the path for only one module:
Dynamsoft.Core.CoreModule.engineResourcePaths.dbr = "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-barcode-reader@10.0.20/dist/";
```

## getVersion

Returns the version of the Core module.

```typescript
static getVersion(): string;
```

**Return Value**

A string type representing the version.

**Code snippet**

```javascript
const version = Dynamsoft.Core.CoreModule.getVersion();
console.log(version);
```

## isModuleLoaded

Returns whether the WebAssembly (.wasm) file for the specified module is successfully loaded.

```typescript
static isModuleLoaded(moduleName: string): boolean;
```

**Parameters**

`moduleName`: specifies a module.

**Return Value**

Boolean indicating whether the .wasm file for the specified module is loaded.

**Code snippet**

```javascript
if(Dynamsoft.Core.CoreModule.isModuleLoaded("cvr")){
    console.log("cvr module is loaded!").
}
```

## loadWasm

Initiates the loading process for the .wasm file(s) corresponding to the specified module(s). If a module relies on other modules, the other modules will be loaded as well.

```typescript
static loadWasm(moduleNames: Array<string> | string): Promise<void>;
```

**Parameters**

`moduleNames`: specifies one or multiple modules. Supported module names are "cvr", "core", "license", "std", "dip", "dbr", "dlr", "ddn".

**Return Value**

A promise that resolves when the resources have been successfully released. It does not provide any value upon resolution.

**Code snippet**

```javascript
await Dynamsoft.Core.CoreModule.loadWasm("cvr");
```

<!-- 
## onLog

Event triggered whenever a log message is ready to be dispatched.

```typescript
static onLog: (message:string) =>void;
```

**Parameters**

`message`: the log message ready to be dispatched.

**Code snippet**

```javascript
Dynamsoft.Core.CoreModule.onLog = console.log;
```

## disableLogging

Disables logging.

```typescript
static disableLogging(): void;
```

## enableLogging

Enables logging to print internal logs to the browser console for debugging.

```typescript
static enableLogging(): void;
``` -->
