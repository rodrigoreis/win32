---
title: BCM\_GETTEXTMARGIN message
description: Gets the margins used to draw text in a button control. You can send this message explicitly or use the Button\_GetTextMargin macro.
ms.assetid: '6c141752-e636-41c4-9d05-df8b320ff59f'
keywords: ["BCM_GETTEXTMARGIN message Windows Controls"]
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
---

# BCM\_GETTEXTMARGIN message

Gets the margins used to draw text in a button control. You can send this message explicitly or use the [**Button\_GetTextMargin**](button-gettextmargin.md) macro.

## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Not used; must be zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**RECT**](https://msdn.microsoft.com/library/windows/desktop/dd162897) structure that contains the margins to use for drawing text.

</dd> </dl>

## Return value

If the message succeeds, it returns **TRUE**. Otherwise it returns **FALSE**.

## Remarks

> [!Note]  
> To use this message, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).

�

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server�2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



�

�




