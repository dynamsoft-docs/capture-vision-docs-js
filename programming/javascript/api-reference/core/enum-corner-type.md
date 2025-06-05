---
layout: default-layout
title: CornerType - Dynamsoft Core Enumerations
description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

<div class="sample-code-prefix template2"></div>
   >- JavaScript
   >
>
```javascript
enum EnumCornerType {
    /**
     * Represents a corner formed by the standard intersection of two line segments at a point, creating a typical corner shape.
     * This is the most common corner type, where the angle between the line segments can vary from acute to obtuse.
     */
    CT_NORMAL_INTERSECTED = 0,
    /**
     * Describes a corner where two line segments intersect in a T-shape.
     * This occurs when one line segment terminates at the midpoint of another, creating three distinct angles.
     */
    CT_T_INTERSECTED = 1,
    /**
     * Characterizes a corner formed by two line segments intersecting each other in a cross shape.
     * This configuration results in four angles and is commonly encountered in grid or lattice patterns.
     */
    CT_CROSS_INTERSECTED = 2,
    /**
     * Defines a scenario where two line segments do not physically intersect but conceptually form a corner.
     * This can occur in virtual shapes or when the corner is implied by the continuation of lines beyond their endpoints.
     */
    CT_NOT_INTERSECTED = 3
}
```