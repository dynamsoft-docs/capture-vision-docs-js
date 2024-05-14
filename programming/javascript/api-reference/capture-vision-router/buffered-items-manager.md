---
layout: default-layout
title: Class BufferedItemsManager - Dynamsoft CaptureVisionRouter Module JS Edition API Reference
description: This page introduces the BufferedItemsManager Class in Dynamsoft CaptureVisionRouter Module JS Edition.
keywords: BufferedItemsManager, JS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# BufferedItemsManager

The `BufferedItemsManager` class is used to manage the buffered items. It provides methods to get and set the maximum number of buffer items and to get buffer items.

| Name                                                           | Description                                                                         |
| -------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [getMaxBufferedItems()](#getmaxbuffereditems)                  | Gets the buffered recognized character items.                                       |
| [setMaxBufferedItems()](#setmaxbuffereditems)                  | Sets the maximum number of buffered items.                                          |
| [getBufferedCharacterItemSet()](#getbufferedcharacteritemset)  | Gets the buffered recognized character items.                                       |

## getMaxBufferedItems

Gets the maximum number of buffered items.

**Syntax**

```typescript
getMaxBufferedItems(): number;
```

**Parameters**

None.

**Return Value**

Returns the max count of buffered items.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const BufferedItemsManager = router.getBufferedItemsManager();
const MaxBufferedItemsCount = BufferedItemsManager.getMaxBufferedItems();
console.log(MaxBufferedItemsCount);
```

## setMaxBufferedItems

Sets the maximum number of buffered items.

**Syntax**

```typescript
setMaxBufferedItems(count: number): void;
```

**Parameters**

`count`: the max number of `BufferedItems`.

**Return Value**

None.

**Code snippet**

```javascript
router = await Dynamsoft.CVR.CaptureVisionRouter.createInstance();
const BufferedItemsManager = router.getBufferedItemsManager();
//set MaxBufferedItems count to 5
BufferedItemsManager.setMaxBufferedItems(5);
```

### getBufferedCharacterItemSet

Gets the buffered character items.

```typescript
getBufferedCharacterItemSet(): DLR.BufferedCharacterItemSet
```

**Parameters**

None.

**Return value**

The `BufferedCharacterItemSet`.

**See Also**

[BufferedCharacterItemSet](https://www.dynamsoft.com/label-recognition/docs/web/programming/javascript/api-reference/interfaces/buffered-character-item-set.html)