---
UID : NI:pointofservicedriverinterface.IOCTL_POINT_OF_SERVICE_MSR_DEAUTHENTICATE_DEVICE
title : IOCTL_POINT_OF_SERVICE_MSR_DEAUTHENTICATE_DEVICE
author : windows-driver-content
description : This I/O control function deauthenticates the magnetic stripe reader (MSR).
old-location : pos\ioctl_point_of_service_msr_deauthenticate_device.htm
old-project : pos
ms.assetid : 796ee8e7-693f-41dd-ad09-cb3c21779ab9
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _PosPropertyId, PosPropertyId
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : ioctl
req.header : pointofservicedriverinterface.h
req.include-header : Pointofservicedriverinterface.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IOCTL_POINT_OF_SERVICE_MSR_DEAUTHENTICATE_DEVICE
req.alt-loc : pointofservicedriverinterface.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : PosPropertyId
---

# IOCTL_POINT_OF_SERVICE_MSR_DEAUTHENTICATE_DEVICE IOCTL
This I/O control function deauthenticates the magnetic stripe reader (MSR).

### Major Code
[IRP_MJ_DEVICE_CONTROL](xref:"https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/irp-mj-device-control")

### Input Buffer
Pointer to the input buffer, a <a href="..\pointofservicedriverinterface\ns-pointofservicedriverinterface-_msr_deauthenticate_device.md">MSR_DEAUTHENTICATE_DEVICE</a> variable that contains the challenge token.

### Input Buffer Length
Size of the input buffer, in bytes. Set to <b>sizeof(MSR_DEAUTHENTICATE_DEVICE)</b>.

### Output Buffer
Not used with this operation; set to <b>NULL</b>.

### Output Buffer Length
Not used with this operation; set to <b>0</b> (zero).

### Input / Output Buffer
<text></text>

### Input / Output Buffer Length
<text></text>

### Status Block
I/O Status block
Returns TRUE if successful; otherwise, returns FALSE.

To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?LinkId=316871">GetLastError</a>.


## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Header** | pointofservicedriverinterface.h (include Pointofservicedriverinterface.h) |
| **IRQL** |  |