﻿---
Description: 'Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.'
ms.assetid: 'ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f'
title: D3DXLoadPRTCompBufferFromFile function
---

# D3DXLoadPRTCompBufferFromFile function

Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.

## Syntax


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## Parameters

<dl> <dt>

*pFileName* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](winprog.windows_data_types)**

Name of the file from which to load the compressed buffer data.

</dd> <dt>

*ppBuffer* \[in, out\]
</dt> <dd>

Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.

</dd> </dl>

## Return value

Type: **[**HRESULT**](455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.

## Remarks

The compiler setting also determines the function version. If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW. Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Precomputed Radiance Transfer Functions](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 



