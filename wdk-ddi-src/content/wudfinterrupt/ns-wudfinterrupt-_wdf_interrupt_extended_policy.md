---
UID: NS:wudfinterrupt._WDF_INTERRUPT_EXTENDED_POLICY
title: "_WDF_INTERRUPT_EXTENDED_POLICY"
author: windows-driver-content
description: The WDF_INTERRUPT_EXTENDED_POLICY structure contains information about an interrupt's policy, priority, affinity, and group.
old-location: wdf\wdf_interrupt_extended_policy_umdf.htm
old-project: wdf
ms.assetid: CD11AD87-D3F1-41E5-AE86-DC289504EF6D
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PWDF_INTERRUPT_EXTENDED_POLICY, PWDF_INTERRUPT_EXTENDED_POLICY, PWDF_INTERRUPT_EXTENDED_POLICY structure pointer, WDF_INTERRUPT_EXTENDED_POLICY, WDF_INTERRUPT_EXTENDED_POLICY structure, _WDF_INTERRUPT_EXTENDED_POLICY, umdf.wdf_interrupt_extended_policy, wdf.wdf_interrupt_extended_policy_umdf, wudfinterrupt/PWDF_INTERRUPT_EXTENDED_POLICY, wudfinterrupt/WDF_INTERRUPT_EXTENDED_POLICY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wudfinterrupt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
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
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wudfinterrupt.h
api_name:
-	WDF_INTERRUPT_EXTENDED_POLICY
product:
- Windows
targetos: Windows
req.typenames: WDF_INTERRUPT_EXTENDED_POLICY, *PWDF_INTERRUPT_EXTENDED_POLICY
---

# _WDF_INTERRUPT_EXTENDED_POLICY structure


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552349">WDF_INTERRUPT_EXTENDED_POLICY</a> structure contains information about an interrupt's policy, priority, affinity, and group.


## -struct-fields




### -field Size

The size, in bytes, of this structure.


### -field Policy

A <a href="https://msdn.microsoft.com/library/windows/hardware/hh464032">WDF_INTERRUPT_POLICY</a>-typed enumerator that specifies a processor affinity policy for the interrupt.


### -field Priority

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552355">WDF_INTERRUPT_PRIORITY</a>-typed enumerator that specifies a priority for the interrupt.


### -field TargetProcessorSetAndGroup

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff546539">GROUP_AFFINITY</a> structure that specifies a processor group and a processor affinity mask within the group, if the <i>Policy</i> parameter is set to <b>WdfIrqPolicySpecifiedProcessors</b>. The GROUP_AFFINITY structure is defined in <i>Winnt.h</i>. 


## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552349">WDF_INTERRUPT_EXTENDED_POLICY</a> structure is used as input for the <a href="https://msdn.microsoft.com/6637E939-010E-4462-92CE-50C4DB867694">IWDFInterrupt::SetExtendedPolicy</a> method. 

To initialize a <a href="https://msdn.microsoft.com/library/windows/hardware/ff552349">WDF_INTERRUPT_EXTENDED_POLICY</a> structure, your driver must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552350">WDF_INTERRUPT_EXTENDED_POLICY_INIT</a>.




## -see-also




<a href="https://msdn.microsoft.com/6637E939-010E-4462-92CE-50C4DB867694">IWDFInterrupt::SetExtendedPolicy</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552350">WDF_INTERRUPT_EXTENDED_POLICY_INIT</a>
 

 

