---
layout: default-layout
title: class CTextureDetectionResultUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextureDetectionResultUnit in Dynamsoft Core Module.
keywords: texture detection result, c++
needAutoGenerateSidebar: true
---

# CTextureDetectionResultUnit

The CTextureDetectionResultUnit class represents an intermediate result unit for texture detection. It is derived from the CIntermediateResultUnit class and contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CTextureDetectionResultUnit : public CIntermediateResultUnit 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetXSpacing`](#getxspacing) | Gets x-direction spacing of the texture stripes. |
| [`GetYSpacing`](#getyspacing) | Gets y-direction spacing of the texture stripes. |

### GetXSpacing

Gets x-direction spacing of the texture stripes.

```cpp
virtual int GetXSpacing() 
```

**Return value**

Returns the x-direction spacing of the texture stripes.

### GetYSpacing

Gets y-direction spacing of the texture stripes.

```cpp
virtual int GetYSpacing() 
```

**Return value**

Returns the y-direction spacing of the texture stripes.
