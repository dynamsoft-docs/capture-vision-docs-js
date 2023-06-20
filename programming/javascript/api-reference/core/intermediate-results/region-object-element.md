---
layout: default-layout
title: class CRegionObjectElement - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CRegionObjectElement in Dynamsoft Core Module.
keywords: region object element, c++
needAutoGenerateSidebar: true
---

# CRegionObjectElement

The CRegionObjectElement class represents an element of a region object in 2D space. It is an abstract class that provides the interface for region object elements.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CRegionObjectElement 
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetLocation`](#getlocation) | Get the location of the region object element. |
| [`GetReferencedElement`](#getreferencedelement) | Get a pointer to a referenced region object element. |
| [`GetElementType`](#getelementtype) | Get the type of the region object element. |

### GetLocation

Get the location of the region object element.

```cpp
CQuadrilateral GetLocation() const
```

**Return value**

Returns a CQuadrilateral object which represents the location of the region object element.

### GetReferencedElement

Get a pointer to a referenced region object element.

```cpp
const CRegionObjectElement* GetReferencedElement() const
```

**Return value**

Returns a const pointer to a referenced CRegionObjectElement object.

### GetElementType

Get the type of the region object element.

```cpp
RegionObjectElementType GetElementType() const
```

**Return value**

Returns a RegionObjectElementType enum value which represents the type of the region object element.


