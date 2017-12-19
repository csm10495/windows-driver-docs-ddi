---
UID: NS.KSMEDIA.KSEVENT_TUNER_INITIATE_SCAN_S
title: KSEVENT_TUNER_INITIATE_SCAN_S
author: windows-driver-content
description: The KSEVENT_TUNER_INITIATE_SCAN_S structure is used in the KSEVENT_TUNER_INITIATE_SCAN event within the EVENTSETID_TUNER event set.
old-location: stream\ksevent_tuner_initiate_scan_s.htm
old-project: stream
ms.assetid: e690c596-d339-4489-97f3-02cacfdc5b04
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: KSEVENT_TUNER_INITIATE_SCAN_S, *PKSEVENT_TUNER_INITIATE_SCAN_S, KSEVENT_TUNER_INITIATE_SCAN_S, PKSEVENT_TUNER_INITIATE_SCAN_S
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: KSEVENT_TUNER_INITIATE_SCAN_S
req.alt-loc: ksmedia.h
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
---

# KSEVENT_TUNER_INITIATE_SCAN_S structure



## -description
The KSEVENT_TUNER_INITIATE_SCAN_S structure is used in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff561898">KSEVENT_TUNER_INITIATE_SCAN</a> event within the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559566">EVENTSETID_TUNER</a> event set. 



## -syntax

````
typedef struct {
  KSEVENTDATA EventData;
  ULONG       StartFrequency;
  ULONG       EndFrequency;
} KSEVENT_TUNER_INITIATE_SCAN_S, *PKSEVENT_TUNER_INITIATE_SCAN_S;
````


## -struct-fields

### -field EventData

A structure of type <a href="..\ks\ns-ks-kseventdata.md">KSEVENTDATA</a> that specifies the standard event structure, which contains the event handle that the driver notifies about the scan operation. 


### -field StartFrequency

The initial frequency, in Hz, for a scan operation. 


### -field EndFrequency

The final frequency, in Hz, for a scan operation.  


## -remarks


## -requirements
<table>
<tr>
<th width="30%">
Version

</th>
<td width="70%">
Available in Windows Vista and later versions of the operating system.

</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Ksmedia.h (include Ksmedia.h)</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559566">EVENTSETID_TUNER</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff561898">KSEVENT_TUNER_INITIATE_SCAN</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [stream\stream]:%20KSEVENT_TUNER_INITIATE_SCAN_S structure%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
