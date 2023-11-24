---
layout: default-layout
title: API Reference Index - CoreModule Class in JavaScript
description: This page introduces the API for the CoreModule Class.
keywords: Core, CoreModule, api reference, javascript, js
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/javascript/api-reference/core/core-module-class.html
---
<!--v3.0.20-->

# CoreModule Class

This class defines common functionality in the `Core` module.

| API Name                                             | Description                                                                                 |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| static [`getVersion()`](#getversion)                 | Returns the version of the `Core` module.                                                   |
| static [`engineResourcePaths`](#engineresourcepaths) | Returns or sets the paths for finding the .wasm files and other resource files for modules. |
| static [`loadWasm()`](#loadwasm)                     | Loads the WebAssembly (.wasm) files for the specified modules.                              |
| static [`loadModel()`](#loadmodel)                   | Loads the model (.data) files for recognizing text.                                         |
| static [`enableLogging()`](#enablelogging)           | Enables logging to print internal logs to the browser console for debugging.                |
| static [`disableLogging()`](#disablelogging)         | Disables logging.                                                                           |

## getVersion

Returns the version of the `Core` module.

```typescript
static getVersion(): string;
```

**Code snippet**

```javascript
const version = Dynamsoft.Core.CoreModule.getVersion();
console.log(version);
```

## engineResourcePaths

Returns or sets the paths for finding the .wasm files and other resource files for modules.

> When loading the resource files from jsDelivr or UNPKG, the paths are automatically deteremined based on the referenced JavaScript files for these modules. You only need to specify these paths if 
> 1. You are using the SDK in a web framework like Angular, React or Vue, or
> 2. You are using a different CDN, or
> 3. You are hosting the files yourself.

```typescript
static engineResourcePaths: any;
```

**Code snippet**

```javascript
Dynamsoft.Core.CoreModule.engineResourcePaths = {
    "core": "https://[SPECIFY-THE-ROOT-PATH]/dynamsoft-core@3.0.20/dist/",
    "license": "https://[SPECIFY-THE-ROOT-PATH]/dynamsoft-license@3.0.20/dist/",
    "cvr": "https://[SPECIFY-THE-ROOT-PATH]/dynamsoft-capture-vision-router@2.0.20/dist/",
    "dbr": "https://[SPECIFY-THE-ROOT-PATH]/dynamsoft-label-recognizer@3.0.20/dist/",
    "dbr": "https://[SPECIFY-THE-ROOT-PATH]/dynamsoft-barcode-reader@10.0.20/dist/"
};
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
await Dynamsoft.Core.CoreModule.loadWasm(["core", "license", "cvr", "dbr"]);
```

## loadModel

Loads the model (.data) files for recognizing text.

```typescript
static loadModel: (modelPath: string | Array<string>) => void;
```

**Parameters**

`modelPath`: specifies the path(s) for one or multiple model files. If specifying only the name of a model, the method will try loading the file from the path specified for the "dlr" module in `Dynamsoft.Core.CoreModule.engineResourcePaths`. For example, if the path for the "dlr" module is "https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer@3.0.20/dist/", then calling `Dynamsoft.Core.CoreModule.loadModel("NumberLetter")` will load the file "NumberLetter.data" from "https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer@3.0.20/dist/NumberLetter/NumberLetter.data".

**Code snippet**

```javascript
await Dynamsoft.Core.CoreModule.loadModel("NumberLetter");
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

