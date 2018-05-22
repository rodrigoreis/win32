---
Description: 'Proxy function for the CreateDecoderFromFilename method.'
ms.assetid: '12c60899-0fe0-47d0-9026-48c74df328ef'
title: 'IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function'
---

# IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function

Proxy function for the [**CreateDecoderFromFilename**](-wic-codec-iwicimagingfactory-createdecoderfromfilename.md) method.

## Syntax


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_��������IWICImagingFactory  *pFactory,
  _In_��������LPCWSTR ������������wzFilename,
  _In_��const GUID ���������������*pguidVendor,
  _In_��������DWORD ��������������dwDesiredAccess,
  _In_��������WICDecodeOptions ���metadataOptions,
  _Out_�������IWICBitmapDecoder ��**ppIDecoder
);
```



## Parameters

<dl> <dt>

*pFactory* \[in\]
</dt> <dd>

Type: **IWICImagingFactory \***

</dd> <dt>

*wzFilename* \[in\]
</dt> <dd>

Type: **LPCWSTR**

A pointer to a null-terminated string that specifies the name of an object to create or open.

</dd> <dt>

*pguidVendor* \[in\]
</dt> <dd>

Type: **const GUID\***

The vendor GUID for the decoder.

</dd> <dt>

*dwDesiredAccess* \[in\]
</dt> <dd>

Type: **DWORD**

The access to the object, which can be read, write, or both.

For more information, see [File Security and Access Rights \[Files\]](http://msdn.microsoft.com/en-us/library/Aa364399(VS.85).aspx).

</dd> <dt>

*metadataOptions* \[in\]
</dt> <dd>

Type: **[**WICDecodeOptions**](-wic-codec-wicdecodeoptions.md)**

The [**WICDecodeOptions**](-wic-codec-wicdecodeoptions.md) to use when creating the decoder.

</dd> <dt>

*ppIDecoder* \[out\]
</dt> <dd>

Type: **[**IWICBitmapDecoder**](-wic-codec-iwicbitmapdecoder.md)\*\***

A pointer that receives a pointer to the new [**IWICBitmapDecoder**](-wic-codec-iwicbitmapdecoder.md).

</dd> </dl>

## Return value

Type: **HRESULT**

If this function succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Remarks

## Requirements



|                                     |                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP with SP2, Windows�Vista \[desktop apps only\]<br/>                                                                                              |
| Minimum supported server<br/> | Windows Server�2008 \[desktop apps only\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



�

�



