---
title: ID3DX11DataLoader Destroy method (D3DX11core.h)
description: Note The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps. Destroys the loader after a work item completes.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Destroy method Direct3D 11
- Destroy method Direct3D 11 , ID3DX11DataLoader interface
- ID3DX11DataLoader interface Direct3D 11 , Destroy method
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
---

# ID3DX11DataLoader::Destroy method

> [!Note]  
> The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.

 

Destroys the loader after a work item completes.

## Syntax


```C++
HRESULT Destroy();
```



## Parameters

This method has no parameters.

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/en-us/library/Bb401631(v=MSDN.10).aspx)**

The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).

## Remarks

This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).

## Requirements



|                    |                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





