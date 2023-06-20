---
layout: default-layout
title: class CTextZonesUnit - Dynamsoft Core Module C++ Edition API Reference
description: This page shows the C++ edition of the class CTextZonesUnit in Dynamsoft Core Module.
keywords: text zones, c++
needAutoGenerateSidebar: true
---

# CTextZonesUnit

The CTextZonesUnit class represents a unit that contains text zones. It is derived from CIntermediateResultUnit class and provides methods to retrieve the count and details of text zones.

## Definition

*Namespace:* dynamsoft::intermediate_results

*Assembly:* DynamsoftCore.dll

```cpp
class CTextZonesUnit : public CIntermediateResultUnit
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of text zones.|
| [`GetTextZone`](#gettextzone) | Gets the quadrilateral shape of the text zone at the specified index.|

### GetCount

Gets the number of text zones in the unit.

```cpp
virtual int GetCount() const
```

**Return value**

Returns the number of text zones in the unit.

### GetTextZone

Gets the quadrilateral shape of the text zone at the specified index.

```cpp
virtual int GetTextZone(int index, CQuadrilateral* quad) const
```

**Parameters**

`[in] index` The index of the text zone.

`[in, out] quad` A pointer to a CQuadrilateral object to receive the quadrilateral shape of the text zone.

**Return value**

Returns 0 if the operation succeeds, or a nonzero error code if the operation fails.

Note: The caller of this method is responsible for allocating memory for the `quad` pointer.
