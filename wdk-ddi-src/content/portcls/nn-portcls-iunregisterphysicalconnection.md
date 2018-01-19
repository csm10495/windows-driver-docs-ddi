---
UID : NN:portcls.IUnregisterPhysicalConnection
title : IUnregisterPhysicalConnection
author : windows-driver-content
description : The IUnregisterPhysicalConnection interface implements three methods to remove a registered physical connection.
old-location : audio\iunregisterphysicalconnection.htm
old-project : audio
ms.assetid : 876a457e-8774-4c51-bd23-6451b3e3a7b7
ms.author : windowsdriverdev
ms.date : 12/14/2017
ms.keywords : PcUnregisterIoTimeout
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : portcls.h
req.include-header : 
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IUnregisterPhysicalConnection
req.alt-loc : portcls.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : Portcls.lib
req.dll : 
req.irql : PASSIVE_LEVEL
req.typenames : PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IUnregisterPhysicalConnection interface

The <code>IUnregisterPhysicalConnection</code> interface implements three methods to remove a registered physical connection. The port driver implements this interface. To determine whether a port driver supports the <code>IUnregisterPhysicalConnection</code> interface, a miniport driver calls the port driver object's <b>QueryInterface</b> method with REFIID <b>IID_IUnregisterPhysicalConnection</b>. The miniport driver is responsible for releasing the <code>IUnregisterPhysicalConnection</code> object after it is no longer needed. The <code>IUnregisterPhysicalConnection</code> interface inherits from <b>IUnknown</b>.

The following port drivers support the <code>IUnregisterSubdevice</code> interface:

WaveCyclic

WavePci

Topology

DMus

MIDI

The three methods in this interface "unregister" physical connections that were registered previously by calls to the <a href="..\portcls\nf-portcls-pcregisterphysicalconnection.md">PcRegisterPhysicalConnection</a>, <a href="..\portcls\nf-portcls-pcregisterphysicalconnectionfromexternal.md">PcRegisterPhysicalConnectionFromExternal</a>, or <a href="..\portcls\nf-portcls-pcregisterphysicalconnectiontoexternal.md">PcRegisterPhysicalConnectionToExternal</a> routines. PortCls supports the three PcRegisterPhysicalConnection<i>Xxx</i> routines.

The port driver uses the information that it obtains from PcRegisterPhysicalConnection<i>Xxx</i> calls to respond to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565205">KSPROPERTY_PIN_PHYSICALCONNECTION</a> property requests.

When deleting a subdevice from an adapter's topology, the driver must unregister the subdevice's physical connections to that portion of the topology. Failure to unregister the subdevice's physical connections can cause memory leaks.

## Methods

<p>The <b>IUnregisterPhysicalConnection</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [portcls.IUnregisterPhysicalConnection.UnregisterPhysicalConnection](nf-portcls-iunregisterphysicalconnection-unregisterphysicalconnection.md) | The UnregisterPhysicalConnection method deletes the registration of a physical connection that was registered by a previous call to PcRegisterPhysicalConnection. |
| [portcls.IUnregisterPhysicalConnection.UnregisterPhysicalConnectionFromExternal](nf-portcls-iunregisterphysicalconnection-unregisterphysicalconnectionfromexternal.md) | The UnregisterPhysicalConnectionFromExternal method deletes the registration of a physical connection that was registered by a previous call to PcRegisterPhysicalConnectionFromExternal. |
| [portcls.IUnregisterPhysicalConnection.UnregisterPhysicalConnectionToExternal](nf-portcls-iunregisterphysicalconnection-unregisterphysicalconnectiontoexternal.md) | The UnregisterPhysicalConnectionToExternal method deletes the registration of a physical connection that was registered by a previous call to PcRegisterPhysicalConnectionToExternal. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | portcls.h |
| **DLL** |  |