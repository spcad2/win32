---
Description: INetCfgComponentNotifyGlobal
ms.assetid: 7d948b27-c822-4202-a23d-7915ab79e63a
title: INetCfgComponentNotifyGlobal
ms.date: 05/31/2018
ms.topic: article
ms.author: windowssdkdev
ms.prod: windows
ms.technology: desktop
---

# INetCfgComponentNotifyGlobal

## 

The **INetCfgComponentNotifyGlobal** interface, an optional interface, provides methods that inform a network component's notify object about changes to network configuration that it must accept, reject, or process.

The interface identifier (IID) for this interface is IID\_INetCfgComponentNotifyGlobal.

### When to Implement

Implement the methods of this interface so the network component's notify object will be informed about changes to network configuration that it must accept, reject, or process. This interface is optional.

### When to Use

The network configuration subsystem calls the methods of **INetCfgComponentNotifyGlobal** to inform a network component's notify object about changes to network configuration that might affect the component.

### Methods

The following methods are listed in Vtable order:



| IUnknown method               | Description                                          |
|-------------------------------|------------------------------------------------------|
| **QueryInterface**<br/> | Returns pointers to supported interfaces.<br/> |
| **AddRef**<br/>         | Increments the reference count.<br/>           |
| **Release**<br/>        | Decrements the reference count.<br/>           |



 



| INetCfgComponentNotifyGlobal method                                                                    | Description                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**GetSupportedNotifications**](/windows/win32/netcfgn/nf-netcfgn-inetcfgcomponentnotifyglobal-getsupportednotifications?branch=master)<br/> | Retrieves the types of notifications required by a notify object.<br/> |
| [**SysQueryBindingPath**](/windows/win32/netcfgn/nf-netcfgn-inetcfgcomponentnotifyglobal-sysquerybindingpath?branch=master)<br/>             | Evaluates a pending binding path change.<br/>                          |
| [**SysNotifyBindingPath**](/windows/win32/netcfgn/nf-netcfgn-inetcfgcomponentnotifyglobal-sysnotifybindingpath?branch=master)<br/>           | Performs operations resulting from a binding path change.<br/>         |
| [**SysNotifyComponent**](/windows/win32/netcfgn/nf-netcfgn-inetcfgcomponentnotifyglobal-sysnotifycomponent?branch=master)<br/>               | Performs operations resulting from a component change.<br/>            |



 

### Comments

If a notify object does not need to accept, reject, or process changes to network configuration that might affect its network component, the **INetCfgComponentNotifyGlobal**interface does not need to be implemented for the object. For example, changes to network configuration that might affect a network component include changing how network components (other than the network component that owns the notify object) are bound together.

E\_NOTIMPL is not a valid return type for any of the methods of **INetCfgComponentNotifyGlobal**.

## Requirements



|                   |                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Netcfgn.h (include Netcfgn.h)</dt> </dl> |



 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bnetxp\netxp%5D:%20INetCfgComponentNotifyGlobal%20%20RELEASE:%20%283/30/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")



