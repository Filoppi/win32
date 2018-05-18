---
Description: 'The Next method retrieves a specified number of media types. This method implements the IEnumMediaTypes::Next method.'
ms.assetid: 'd59dea48-e36c-4ee6-9935-5a47e8a12a9e'
title: 'CEnumMediaTypes.Next method'
---

# CEnumMediaTypes.Next method

The `Next` method retrieves a specified number of media types. This method implements the [**IEnumMediaTypes::Next**](ienummediatypes-next.md) method.

## Syntax


```C++
HRESULT Next(
  �ULONG ��������cMediaTypes,
  �AM_MEDIA_TYPE **ppMediaTypes,
  �ULONG ��������*pcFetched
);
```



## Parameters

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Number of media types to retrieve.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Array of pointers to [**AM\_MEDIA\_TYPE**](am-media-type.md) structures, of size *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Pointer to a variable that receives the number of media types the method returned. Can be **NULL** if *cMediaTypes* is 1.

</dd> </dl>

## Return value

Returns one of the **HRESULT** values shown in the following table.



| Return code                                                                                                | Description                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S\_FALSE**</dt> </dl>                    | Did not retrieve as many media types as requested.<br/>                       |
| <dl> <dt>**S\_OK**</dt> </dl>                       | Success.<br/>                                                                 |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>               | Invalid argument.<br/>                                                        |
| <dl> <dt>**E\_POINTER**</dt> </dl>                  | **NULL** pointer argument.<br/>                                               |
| <dl> <dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt> </dl> | The pin's state has changed and is now inconsistent with the enumerator.<br/> |



�

## Remarks

If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures. The number of structures is equal to *\*pcFetched*. Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.

This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CEnumMediaTypes Class**](cenummediatypes.md)
</dt> </dl>

�

�



