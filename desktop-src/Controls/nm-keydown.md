---
title: NM\_KEYDOWN notification code
description: Sent by a control when the control has the keyboard focus and the user presses a key. This notification code is sent in the form of a WM\_NOTIFY message.
ms.assetid: 'e3b38096-797d-4948-9595-a252cf33dcdd'
keywords: ["NM_KEYDOWN notification code Windows Controls"]
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
---

# NM\_KEYDOWN notification code

Sent by a control when the control has the keyboard focus and the user presses a key. This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## Parameters

<dl> <dt>

*lParam* 
</dt> <dd>

A pointer to an [**NMKEY**](nmkey.md) structure that contains additional information about the key that caused the notification code.

</dd> </dl>

## Return value

Return nonzero to prevent the control from processing the key, or zero otherwise.

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�Vista \[desktop apps only\]<br/>                                        |
| Minimum supported server<br/> | Windows Server�2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



�

�




