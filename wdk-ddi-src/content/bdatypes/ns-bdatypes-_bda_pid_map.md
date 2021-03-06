---
UID: NS:bdatypes._BDA_PID_MAP
title: "_BDA_PID_MAP"
author: windows-driver-content
description: The BDA_PID_MAP structure describes a type of data to filter out of the input stream of a packet identifier (PID) filter and then pass to a downstream filter.
old-location: stream\bda_pid_map.htm
old-project: stream
ms.assetid: a5ad0f35-8413-4828-92f8-47544a6e802e
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PBDA_PID_MAP, BDA_PID_MAP, BDA_PID_MAP structure [Streaming Media Devices], PBDA_PID_MAP, PBDA_PID_MAP structure pointer [Streaming Media Devices], _BDA_PID_MAP, bdaref_a0793356-2192-4a72-9605-3d0d6d981ad2.xml, bdatypes/BDA_PID_MAP, bdatypes/PBDA_PID_MAP, stream.bda_pid_map"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: Bdatypes.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdatypes.h
api_name:
-	BDA_PID_MAP
product:
- Windows
targetos: Windows
req.typenames: BDA_PID_MAP, *PBDA_PID_MAP
---

# _BDA_PID_MAP structure


## -description


The BDA_PID_MAP structure describes a type of data to filter out of the input stream of a packet identifier (PID) filter and then pass to a downstream filter. This output consists of packets that are identified with PIDs and contain particular media content. 


## -struct-fields




### -field MediaSampleContent

MEDIA_SAMPLE_CONTENT enumerated type value that specifies the type of media content that packets contain. 


### -field ulcPIDs

Number of PIDs in the <b>aulPIDs</b> array. 


### -field aulPIDs

Array of PIDs that identify packets to map to the output of a PID filter. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556540">BDA_PID_UNMAP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566551">KSPROPSETID_BdaPIDFilter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567719">MEDIA_SAMPLE_CONTENT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567763">PID_MAP</a>
 

 

