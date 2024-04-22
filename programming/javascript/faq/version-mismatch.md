
---
layout: default-layout
title: Why am I encountering errors like "r.taskSet.intermediateResultUnits is not iterable" when using frameworks like React or Angular with Dynamsoft packages?
keywords: Dynamsoft Capture Vision, FAQ, version, mismatch, taskset
description: Why am I encountering errors like "r.taskSet.intermediateResultUnits is not iterable" when using frameworks like React or Angular with Dynamsoft packages?
needAutoGenerateSidebar: false
---

# Why am I encountering errors like "r.taskSet.intermediateResultUnits is not iterable" when using frameworks like React or Angular with Dynamsoft packages?

[<< Back to FAQ index](index.md)

Topic: Resolving Version Mismatch Issues in Dynamsoft Packages

Resolution:

When using a framework like React or Angular with Dynamsoft packages, it's crucial to ensure that the version number of each Dynamsoft package listed in the `package.json` file matches the version number defined in the `engineResourcePaths` generally found defined in the cvr.ts file if you have followed the samples for developement.

In the `engineResourcePaths` configuration, make sure to include the correct version numbers for each Dynamsoft package mentioned in `package.json`. Here's an example of how to define the engineResourcePaths with the correct version numbers:

```javascript
Dynamsoft.Core.CoreModule.engineResourcePaths = {
  std: "https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-std@<std_version>/dist/",
  dip: "https://cdn.jsdelivr.net/npm/dynamsoft-image-processing@<dip_version>/dist/",
  core: "https://cdn.jsdelivr.net/npm/dynamsoft-core@<core_version>/dist/",
  license: "https://cdn.jsdelivr.net/npm/dynamsoft-license@<license_version>/dist/",
  cvr: "https://cdn.jsdelivr.net/npm/dynamsoft-capture-vision-router@<cvr_version>/dist/",
  dbr: "https://cdn.jsdelivr.net/npm/dynamsoft-barcode-reader@<dbr_version>/dist/",
  dce: "https://cdn.jsdelivr.net/npm/dynamsoft-camera-enhancer@<dce_version>/dist/"
};
```
Replace <std_version>, <dip_version>, <core_version>, <license_version>, <cvr_version>, <dbr_version>, and <dce_version> with the appropriate version numbers corresponding to each Dynamsoft package.

```javascript
//some lines from package.json
"dependencies": {
...
  "dynamsoft-barcode-reader": "<dbr_version>",
  "dynamsoft-camera-enhancer": "<dce_version>",
  "dynamsoft-capture-vision-router": "<cvr_version>",
  "dynamsoft-core": "<core_version>",
  "dynamsoft-license": "<license_version>",
  "dynamsoft-utility": "<utility_version>",
}
```

By following these steps and maintaining consistency in version numbers between `package.json` and `engineResourcePaths`, you can mitigate version mismatch errors and ensure the proper functioning of Dynamsoft packages within your framework-based application.