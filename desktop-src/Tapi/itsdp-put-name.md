---
Description: The put\_Name method sets the session name.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: ITSdp::put_Name method (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
---

# ITSdp::put\_Name method

\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API provides similar functionality.\]

The **put\_Name** method sets the session name.

## Syntax


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## Parameters

<dl> <dt>

*pName* \[in\]
</dt> <dd>

Pointer to a **BSTR** containing the session name.

</dd> </dl>

## Return value

This method can return one of these values.



| Return code                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>          | Method succeeded.<br/>                                    |
| <dl> <dt>**E\_POINTER**</dt> </dl>     | The *pName* parameter is not a valid pointer.<br/>        |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl> | Insufficient memory exists to perform the operation.<br/> |
| <dl> <dt>**E\_FAIL**</dt> </dl>        | Unspecified error.<br/>                                   |
| <dl> <dt>**E\_NOTIMPL**</dt> </dl>     | This method is not yet implemented.<br/>                  |



 

## Remarks

The application must use [**SysAllocString**](https://msdn.microsoft.com/en-us/library/ms221458(v=VS.71).aspx) to allocate memory for the *pName* parameter and use [**SysFreeString**](https://msdn.microsoft.com/en-us/library/ms221481(v=VS.71).aspx) to free the memory when the variable is no longer needed.

## Requirements



|                         |                                                                                       |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI version<br/> | Requires TAPI 3.0 or later<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Library<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## See also

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get\_Name**](itsdp-get-name.md)
</dt> </dl>

 

 




