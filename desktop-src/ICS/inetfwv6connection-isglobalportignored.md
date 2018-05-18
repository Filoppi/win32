---
title: INetFwV6Connection IsGlobalPortIgnored method
description: The IsGlobalPortIgnored method returns VARIANT\_TRUE if the global setting to permit inbound connection attempts is ignored for the specified port and protocol pair.
ms.assetid: '826edcbb-6b02-4945-bcf3-aeb8f33de04d'
keywords: ["IsGlobalPortIgnored method ICS/ICF", "IsGlobalPortIgnored method ICS/ICF , INetFwV6Connection interface", "INetFwV6Connection interface ICS/ICF , IsGlobalPortIgnored method"]
topic_type:
- apiref
api_name:
- INetFwV6Connection.IsGlobalPortIgnored
api_location:
- Netfwv6.dll
api_type:
- COM
---

# INetFwV6Connection::IsGlobalPortIgnored method

\[The IPv6 Internet Connection Firewall is available for use in the operating systems specified in the Requirements section. Instead, use the [Windows Firewall API](windows-firewall-start-page.md).\]

The **IsGlobalPortIgnored** method returns VARIANT\_TRUE if the global setting to permit inbound connection attempts is ignored for the specified port and protocol pair.

## Syntax


```C++
HRESULT IsGlobalPortIgnored(
  [in]��USHORT �������usPort,
  [in]��PORT_PROTOCOL Protocol,
  [out]�VARIANT_BOOL �*pvbGlobalPortIsIgnored
);
```



## Parameters

<dl> <dt>

*usPort* \[in\]
</dt> <dd>

Specifies the port ID in host byte order. Must be in the range 1 � 65535.

</dd> <dt>

*Protocol* \[in\]
</dt> <dd>

Specifies the port protocol type as defined in the [**PORT\_PROTOCOL**](port-protocol.md) enumeration.

</dd> <dt>

*pvbGlobalPortIsIgnored* \[out\]
</dt> <dd>

Specifies the port name for information only. See the Remarks section for further explanation.

</dd> </dl>

## Return value

If the method succeeds the return value is S\_OK.

If the method fails, the return value is one of the following error codes.



| Return code                                                                                   | Description                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**E\_ABORT**</dt> </dl>       | The operation was aborted.<br/>                        |
| <dl> <dt>**E\_FAIL**</dt> </dl>        | An unspecified error occurred.<br/>                    |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>  | One of the parameters is invalid.<br/>                 |
| <dl> <dt>**E\_NOINTERFACE**</dt> </dl> | A specified interface is not supported.<br/>           |
| <dl> <dt>**E\_NOTIMPL**</dt> </dl>     | A specified method is not implemented.<br/>            |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl> | The method is unable to allocate required memory.<br/> |
| <dl> <dt>**E\_POINTER**</dt> </dl>     | A pointer passed as a parameter is not valid.<br/>     |
| <dl> <dt>**E\_UNEXPECTED**</dt> </dl>  | The method failed for unknown reasons.<br/>            |



�

## Requirements



|                                     |                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP with SP1 \[desktop apps only\]<br/>                                   |
| Minimum supported server<br/> | None supported<br/>                                                              |
| End of client support<br/>    | Windows�XP with SP1<br/>                                                         |
| Redistributable<br/>          | Advanced Networking Pack for Windows�XP<br/>                                     |
| Header<br/>                   | <dl> <dt>Netfwv6.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Netfwv6.dll</dt> </dl> |



## See also

<dl> <dt>

[**INetFwV6Connection**](inetfwv6connection.md)
</dt> </dl>

�

�




