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

This class defines common functionality in the Core module.

| API Name                                             | Description                                                                                 |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `static` [getVersion()](#getversion)                 | Returns the version of the Core module.                                                     |
| `static` [detectEnvironment()](#detectenvironment)   | Detects the current environment.                                                            |
| `static` [onWarning](#onwarning)                     | A callback which is triggered when the running environment is not ideal.                    |
| `static` [engineResourcePaths](#engineresourcepaths) | Returns or sets the paths for finding the .wasm files and other resource files for modules. |
| `static` [loadWasm()](#loadwasm)                     | Loads the WebAssembly (.wasm) files for the specified modules.                              |
| `static` [enableLogging()](#enablelogging)           | Enables logging to print internal logs to the browser console for debugging.                |
| `static` [disableLogging()](#disablelogging)         | Disables logging.                                                                           |

## getVersion

Returns the version of the Core module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.Core.CoreModule.getVersion();
console.log(version);
```

## detectEnvironment

Detect the current device environment.

```typescript
detectEnvironment(): Promise<any>
```

**Return Value**

A Promise that resolves to an object containing environment support information.

**Code snippet**

```javascript
await Dynamsoft.Core.CoreModule.detectEnvironment();
// example return value:
// {"wasm":true,"worker":true,"getUserMedia":true,"camera":true,"browser":"Edge","version":119,"OS":"Windows"}
```

## onWarning

A callback which is triggered when the running environment is not ideal.

```typescript
onWarning: (warning:Warning) =>{};
```

**Return Value**

`Promise<any>`

**Code snippet**

```javascript
Dynamsoft.Core.CoreModule.onWarning = warning => console.log(warning.message);
```

**See Also**

* [Warning](./basic-structures/warning.md)

## engineResourcePaths

Returns or sets the paths for finding the .wasm files and other resource files for modules.

When loading the resource files from jsDelivr or UNPKG, the paths are automatically determined based on the referenced JavaScript files for these modules. You only need to specify these paths if

1. You are using the SDK in a web framework like Angular, React or Vue, or
2. You are using a different CDN, or
3. You are hosting the files yourself.

> If you only specify "rootDirectory", the paths will be automatically matched to that directory.
> If you specify both "rootDirectory" and individual paths, the individual paths take precedence.

```typescript
static engineResourcePaths: {
    "rootDirectory"?: string,
    "std"?: string, 
    "dip"?: string,
    "dnn"?: string,
    "core"?: string,
    "license"?: string,
    "cvr"?: string,
    "utility"?: string,
    "dbr"?: string,
    "dlr"?: string,
    "ddn"?: string,
    "dcp"?: string,
    [moduleName: string]: string|undefined
};
```

**Code snippet**

```javascript
// To specify all modules:
Dynamsoft.Core.CoreModule.engineResourcePaths = {
    "std": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-capture-vision-std@1.0.0/dist/",
    "dip": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-image-processing@2.0.20/dist/",
    "dnn": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-capture-vision-dnn@1.0.0/dist/",
    "core": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-core@3.0.20/dist/",
    "license": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-license@3.0.20/dist/",
    "cvr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-capture-vision-router@2.0.20/dist/",
    "utility": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-utility@1.0.20/dist/",
    "dbr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-barcode-reader@10.0.20/dist/"
    "dlr": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-label-recognizer@3.0.20/dist/",
    "ddn": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-document-normalizer@2.0.20/dist/"
    "dcp": "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-code-parser@2.0.20/dist/"
};
// To specify only one module
Dynamsoft.Core.CoreModule.engineResourcePaths.dbr = "https://[SPECIFY-THE-ROOT-DIRECTORY]/dynamsoft-barcode-reader@10.0.20/dist/";
// To specify only the root directory
Dynamsoft.Core.CoreModule.engineResourcePaths.rootDirectory = "https://[SPECIFY-THE-ROOT-DIRECTORY]";
```

## loadWasm

Loads the .wasm files for the specified modules.

```typescript
static loadWasm(moduleNames: Array<string>): Promise<void>;
```

**Parameters**

`moduleNames`: specifies one or multiple modules.

**Code snippet**

```javascript
await Dynamsoft.Core.CoreModule.loadWasm(["cvr", "dbr"]);
```

## enableLogging

Enables logging to print internal logs to the browser console for debugging.

```typescript
static enableLogging(): void;
```

## disableLogging

Disables logging.

```typescript
static disableLogging(): void;
```

