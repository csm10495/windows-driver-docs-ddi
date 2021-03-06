---
UID: NF:wiautil.CWiauPropertyList.SetCurrentValue(INT,FLOAT)
title: CWiauPropertyList::SetCurrentValue(INT,FLOAT)
author: windows-driver-content
description: The CWiauPropertyList::SetCurrentValue(FLOAT) method sets the current value of a property of type FLOAT, and sets its type to VT_R4.
old-location: image\cwiaupropertylist_setcurrentvalue_float_.htm
old-project: image
ms.assetid: dfcbe65b-7da1-4427-a58f-cbec4ce355bf
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: CWiauPropertyList interface [Imaging Devices],SetCurrentValue method, CWiauPropertyList.SetCurrentValue, CWiauPropertyList.SetCurrentValue(INT,FLOAT), CWiauPropertyList::SetCurrentValue, CWiauPropertyList::SetCurrentValue(INT,FLOAT), SetCurrentValue, SetCurrentValue method [Imaging Devices], SetCurrentValue method [Imaging Devices],CWiauPropertyList interface, SetCurrentValue(FLOAT)(CWiauPropertyList), image.cwiaupropertylist_setcurrentvalue_float_, wiauFncs_871f53bf-7ad7-459e-9760-04c67a55f800.xml, wiautil/CWiauPropertyList::SetCurrentValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiautil.h
req.include-header: Wiautil.h, Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
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
-	COM
api_location:
-	Wiautil.h
api_name:
-	CWiauPropertyList.SetCurrentValue
product: Windows
targetos: Windows
req.typenames: 
---

# CWiauPropertyList::SetCurrentValue(INT,FLOAT)


## -description


The <b>CWiauPropertyList::SetCurrentValue(FLOAT)</b> method sets the current value of a property of type <b>FLOAT</b>, and sets its type to VT_R4.


## -parameters




### -param index

Specifies the property index. Set this parameter to the value in *<i>pIdx</i> when the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a> method returns.


### -param value

Specifies the value that is written to the device property in the property list.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4f11bec0-8ff4-4fa0-824c-71ce9774d5d1">CWiauPropertyList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540391">CWiauPropertyList::DefineProperty</a>
 

 

