---
Description: Constructs an application protocol data unit (APDU) command that conditionally updates security status, verifying the identity of the computer when the smart card does not trust it.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: ISCardISO7816::ExternalAuthenticate method (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- ISCardISO7816.ExternalAuthenticate
api_type: 
- COM
api_location: 
- Scardssp.dll
---

# ISCardISO7816::ExternalAuthenticate method

\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section. It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The [Smart Card Modules](https://msdn.microsoft.com/en-us/library/Dd627652(v=VS.85).aspx) provide similar functionality.\]

The **ExternalAuthenticate** method constructs an [*application protocol data unit*](https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx) does not trust it.

The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.

## Syntax


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## Parameters

<dl> <dt>

*byAlgorithmRef* \[in\]
</dt> <dd>

The reference of the algorithm in the card.

If this value is zero, this indicates that no information is given. The reference of the algorithm is known either before issuing the command or is provided in the data field.

</dd> <dt>

*bySecretRef* \[in\]
</dt> <dd>

The reference of the secret.



| Value                                                                                                                                                                                    | Meaning                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**No Info**</dt> </dl>                     | Bit position: 00000000<br/> No information is given. The reference of the secret is known either before issuing the command or is provided in the data field.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Global ref**</dt> </dl>         | Bit position: 0-------<br/> Global reference data (an MF specific key).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Specific ref**</dt> </dl> | Bit position: 1-------<br/> Specific reference data (a DF specific key).<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Bit position: -xx-----<br/> 00 (other values are RFU).<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Secret**</dt> </dl>                         | Bit position: ---xxxxx<br/> Number of the secret.<br/>                                                                                                             |



 

</dd> <dt>

*pChallenge* \[in\]
</dt> <dd>

A pointer to the authentication-related data. This parameter may be **NULL**.

</dd> <dt>

*ppCmd* \[in, out\]
</dt> <dd>

On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.

On return, it is filled with the APDU command constructed by this operation. If *ppCmd* was set to **NULL**, a [*smart card*](https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.

</dd> </dl>

## Return value

The method returns one of the following possible values.



| Return code                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>          | The operation completed successfully.<br/>     |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>  | A parameter that is not valid was passed.<br/> |
| <dl> <dt>**E\_POINTER**</dt> </dl>     | A bad pointer was passed in.<br/>              |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl> | Out of memory.<br/>                            |



 

## Remarks

For the encapsulated command to be successful, the last challenge obtained from the card must be valid.

Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).

For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).

In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request. For more information, see [Smart Card Return Values](authentication-return-values.md).

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| End of client support<br/>    | Windows XP<br/>                                                                   |
| End of server support<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Type library<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## See also

<dl> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 




