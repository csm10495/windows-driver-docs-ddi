---
UID: NF:ntifs.CcGetFileObjectFromSectionPtrsRef
title: CcGetFileObjectFromSectionPtrsRef function
author: windows-driver-content
description: When passed a pointer to a SECTION_OBJECT_POINTERS structure for a cached file, the CcGetFileObjectFromSectionPtrsRef routine returns a pointer to the file object that the cache manager is using for the cached file.
old-location: ifsk\ccgetfileobjectfromsectionptrsref.htm
old-project: ifsk
ms.assetid: 8afbd8df-95fc-453f-a1d8-400a993c286a
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CcGetFileObjectFromSectionPtrsRef, CcGetFileObjectFromSectionPtrsRef routine [Installable File System Drivers], ccref_e38ddec7-5501-40b4-a2a3-0a13c1c0fb4d.xml, ifsk.ccgetfileobjectfromsectionptrsref, ntifs/CcGetFileObjectFromSectionPtrsRef
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h, Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating system.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	CcGetFileObjectFromSectionPtrsRef
product:
- Windows
targetos: Windows
req.typenames: 
---

# CcGetFileObjectFromSectionPtrsRef function


## -description


When passed a pointer to a SECTION_OBJECT_POINTERS structure for a cached file, the <b>CcGetFileObjectFromSectionPtrsRef</b> routine returns a pointer to the file object that the cache manager is using for the cached file.


## -parameters




### -param SectionObjectPointer [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563687">SECTION_OBJECT_POINTERS</a> structure that is associated with the cached file.


## -returns



A pointer to the file object for the cached file, or <b>NULL</b> if the file is not cached or is no longer cached.




## -remarks



The file object is returned with a reference.  The caller is responsible for calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff557724">ObDereferenceObject</a> on the file object when it has finished using the file object.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539104">CcGetFileObjectFromSectionPtrs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557724">ObDereferenceObject</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563687">SECTION_OBJECT_POINTERS</a>
 

 

