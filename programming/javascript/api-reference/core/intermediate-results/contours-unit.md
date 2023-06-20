---
layout: default-layout
title: class CContoursUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CContoursUnit in Dynamsoft Core Module.
keywords: contours, c++
needAutoGenerateSidebar: true
---

# CContoursUnit

The CContoursUnit class represents a unit that contains contours as intermediate results. It is derived from the CIntermediateResultUnit class.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CContoursUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method                    | Description |
|---------------------------|---------------------------------------------|
| [`GetCount`](#getcount)   | Gets the number of contours in the unit.    |
| [`GetContour`](#getcontour) | Gets the contour at the specified index.  |

### GetCount

Gets the number of contours in the unit.

```cpp
virtual int GetCount() const;
```

**Return value**

Returns the number of contours in the unit.

### GetContour

Gets the contour at the specified index.

```cpp
virtual int GetContour(int index, CContour* contour) const;
```

**Parameters**

`[in] index` The index of the contour to get.

`[in, out] contour` A pointer to a CContour object that will be filled with the contour data.

**Return value**

Returns 0 if successful, or an error code if the contour could not be retrieved.

Note: The caller of this method is responsible for allocating memory for the `contour` pointer.
