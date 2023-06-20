---
layout: default-layout
title: class CPredetectedRegionElement - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CPredetectedRegionElement in Dynamsoft Core Module.
keywords: predetected region element, c++
needAutoGenerateSidebar: true
---

# CPredetectedRegionElement

The CPredetectedRegionElement class represents a region element that has been pre-detected in an image. It is a subclass of the CRegionObjectElement.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CPredetectedRegionElement : public CRegionObjectElement
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetModeName`](#getmodename) | Gets the name of the detection mode used to detect this region element. |

### GetModeName

Gets the name of the detection mode used to detect this region element.

```cpp
virtual const char* GetModeName() const;
```

**Return value**

Returns the name of the detection mode used to detect this region element.
