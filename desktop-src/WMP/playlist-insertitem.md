---
title: Playlist.insertItem method
description: The insertItem method inserts a media item into the playlist at the specified location.
ms.assetid: '2db2d28d-4cbf-423c-824f-e1e212c46f7a'
keywords: ["insertItem method Windows Media Player", "insertItem method Windows Media Player , Playlist class", "Playlist class Windows Media Player , insertItem method"]
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
---

# Playlist.insertItem method

The **insertItem** method inserts a media item into the playlist at the specified location.

## Syntax


```JScript
Playlist.insertItem(
  index,
  item
)
```



## Parameters

<dl> <dt>

*index* \[in\]
</dt> <dd>

**Number** (**long**) containing the index at which to add the item.

</dd> <dt>

*item* \[in\]
</dt> <dd>

**Media** object to insert.

</dd> </dl>

## Return value

This method does not return a value.

## Remarks

All items after the inserted item will have their index numbers increased by one.

To use this method, full access to the library is required. For more information, see [Library Access](library-access.md).

## Requirements



|                    |                                                                                    |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player version 7.0 or later.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## See also

<dl> <dt>

[**Playlist Object**](playlist-object.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

�

�




