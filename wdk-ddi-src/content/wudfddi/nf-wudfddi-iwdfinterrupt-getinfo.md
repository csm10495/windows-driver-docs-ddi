---
UID: NF.wudfddi.IWDFInterrupt.GetInfo
title: IWDFInterrupt::GetInfo method
author: windows-driver-content
description: The GetInfo method retrieves information about a specified interrupt.
old-location: wdf\iwdfinterrupt_getinfo.htm
old-project: wdf
ms.assetid: 744D0FFE-6D3C-4AED-8935-63EE9B0AFA0F
ms.author: windowsdriverdev
ms.date: 12/15/2017
ms.keywords: IWDFInterrupt, IWDFInterrupt::GetInfo, GetInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.alt-api: IWDFInterrupt.GetInfo
req.alt-loc: WUDFx.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
req.product: Windows 10 or later.
---

# IWDFInterrupt::GetInfo method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetInfo</b> method retrieves information about a specified interrupt.



## -syntax

````
void GetInfo(
   WDF_INTERRUPT_INFO *Info
);
````


## -parameters

### -param Info 

A pointer to a caller-allocated <a href="wdf.wdf_interrupt_info">WDF_INTERRUPT_INFO</a> structure that the driver has previously initialized by calling <a href="wdf.wdf_interrupt_info_init">WDF_INTERRUPT_INFO_INIT</a>.


## -returns
This method does not return a value.


## -remarks
The <b>GetInfo</b> method can obtain interrupt information only if your driver calls it after the framework has called the driver's <a href="wdf.ipnpcallbackhardware2_onpreparehardware">OnPrepareHardware</a> callback function and before the framework has called the driver's <a href="wdf.ipnpcallbackhardware2_onreleasehardware">OnReleaseHardware</a> callback function.

For information about the order in which a driver's callback functions are called, see <a href="wdf.pnp_and_power_management_scenarios_in_umdf">PnP and Power Management Scenarios in UMDF</a>.

For more information about handling interrupts in UMDF drivers, see <a href="wdf.accessing_hardware_and_handling_interrupts">Accessing Hardware and Handling Interrupts</a>.


## -requirements
<table>
<tr>
<th width="30%">
Target platform

</th>
<td width="70%">
<dl>
<dt>Desktop</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
End of support

</th>
<td width="70%">
Unavailable in UMDF 2.0 and later.

</td>
</tr>
<tr>
<th width="30%">
Minimum UMDF version

</th>
<td width="70%">
1.11

</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Wudfddi.h</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
DLL

</th>
<td width="70%">
<dl>
<dt>WUDFx.dll</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfinterrupt.md">IWDFInterrupt</a>
</dt>
<dt>
<a href="wdf.ipnpcallbackhardware2_onpreparehardware">OnPrepareHardware</a>
</dt>
<dt>
<a href="wdf.ipnpcallbackhardware2_onreleasehardware">OnReleaseHardware</a>
</dt>
<dt>
<a href="wdf.wdf_interrupt_info">WDF_INTERRUPT_INFO</a>
</dt>
<dt>
<a href="wdf.wdf_interrupt_info_init">WDF_INTERRUPT_INFO_INIT</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFInterrupt::GetInfo method%20 RELEASE:%20(12/15/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
