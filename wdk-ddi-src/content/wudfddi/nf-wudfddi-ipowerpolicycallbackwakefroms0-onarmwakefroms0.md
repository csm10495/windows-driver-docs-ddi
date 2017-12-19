---
UID: NF.wudfddi.IPowerPolicyCallbackWakeFromS0.OnArmWakeFromS0
title: IPowerPolicyCallbackWakeFromS0::OnArmWakeFromS0 method
author: windows-driver-content
description: A driver's OnArmWakeFromS0 callback function arms (that is, enables) a device so that it can trigger a wake signal while in a low-power device state, if the system remains in the system working state (S0).
old-location: wdf\ipowerpolicycallbackwakefroms0_onarmwakefroms0.htm
old-project: wdf
ms.assetid: 4801a7c4-8bd4-4372-bcdd-49e5570d833e
ms.author: windowsdriverdev
ms.date: 12/15/2017
ms.keywords: IPowerPolicyCallbackWakeFromS0, IPowerPolicyCallbackWakeFromS0::OnArmWakeFromS0, OnArmWakeFromS0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
req.alt-api: IPowerPolicyCallbackWakeFromS0.OnArmWakeFromS0
req.alt-loc: Wudfddi.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
req.product: Windows 10 or later.
---

# IPowerPolicyCallbackWakeFromS0::OnArmWakeFromS0 method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

A driver's <b>OnArmWakeFromS0</b> callback function arms (that is, enables) a device so that it can trigger a wake signal while in a low-power device state, if the system remains in the <a href="https://msdn.microsoft.com/93ab0943-a4cc-4ef0-a250-1c63b2c915d5">system working state</a> (S0). 



## -syntax

````
HRESULT OnArmWakeFromS0(
  [in] IWDFDevice *pWdfDevice
);
````


## -parameters

### -param pWdfDevice [in]

A pointer to the <b>IWDFDevice</b> interface of the device object that represents one of the driver's devices.


## -returns
If the operation is successful, the <b>OnArmWakeFromS0</b> callback function must return S_OK or another status value for which SUCCEEDED(<i>status</i>) equals <b>TRUE</b>. Otherwise it must return a status value for which SUCCEEDED(<i>status</i>) equals <b>FALSE</b>.

If SUCCEEDED(status) equals <b>FALSE</b>, the framework calls the driver's <a href="wdf.ipowerpolicycallbackwakefroms0_ondisarmwakefroms0">IPowerPolicyCallbackWakeFromS0::OnDisarmWakeFromS0</a> callback function. (The framework does not report a device failure to the PnP manager.) 




## -remarks
Your driver must provide an <b>OnArmWakeFromS0</b> callback function if the driver supports the <a href="..\wudfddi\nn-wudfddi-ipowerpolicycallbackwakefroms0.md">IPowerPolicyCallbackWakeFromS0</a> interface. 

The <b>OnArmWakeFromS0</b> callback function handles device-specific operations that are needed to enable the device to detect an external event that triggers a wake signal on the bus. The kernel-mode bus driver handles bus-specific operations, such as enabling the PCI bus's Power Management Event (PME) signal.

If the driver has registered an <b>OnArmWakeFromS0</b> callback function, the framework calls it while the device is still in the D0 device power state, before the bus driver lowers the device's power state but after the framework has sent a <a href="https://msdn.microsoft.com/ed582644-af51-4841-be59-6a3deb6d9de5">wait/wake IRP</a> on behalf of the driver. 

The process occurs in the following sequence:

The framework determines that the device has been idle for a preset amount of time.

The framework calls the driver's <b>OnArmWakeFromS0</b> callback function.

The framework requests the driver for the device's bus to lower the device's power.

Immediately before your device enters a low power state, the framework will call your driver's <a href="wdf.ipnpcallback_ond0exit">IPnpCallback::OnD0Exit</a> callback function.

For more information about when the framework calls this callback function, see <a href="wdf.pnp_and_power_management_scenarios_in_umdf">PnP and Power Management Scenarios in UMDF</a>.

You do not need to provide an <b>OnArmWakeFromS0</b> callback function if your device:

Is a USB device that supports "selective suspend."

Cannot be powered down while the system remains fully powered.

Does not require special hardware operations that enable the device to trigger a wake signal.

If your device supports USB "selective suspend" and if your driver specifies <b>IdleUsbSelectiveSuspend</b> when it calls <a href="wdf.iwdfdevice2_assigns0idlesettings">IWDFDevice2::AssignS0IdleSettings</a>, the framework sends a "selective suspend" request to the USB bus driver when the device has been idle for a preset amount of time.

For more information about this callback function, see <a href="wdf.supporting_idle_power_down_in_umdf_drivers">Supporting Idle Power-Down in UMDF-based Drivers</a>.


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
1.9

</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Wudfddi.h (include Wudfddi.h)</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\wudfddi\nn-wudfddi-ipowerpolicycallbackwakefroms0.md">IPowerPolicyCallbackWakeFromS0</a>
</dt>
<dt>
<a href="wdf.ipowerpolicycallbackwakefroms0_ondisarmwakefroms0">IPowerPolicyCallbackWakeFromS0::OnDisarmWakeFromS0</a>
</dt>
<dt>
<a href="wdf.ipowerpolicycallbackwakefroms0_onwakefroms0triggered">IPowerPolicyCallbackWakeFromS0::OnWakeFromS0Triggered</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IPowerPolicyCallbackWakeFromS0::OnArmWakeFromS0 method%20 RELEASE:%20(12/15/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
