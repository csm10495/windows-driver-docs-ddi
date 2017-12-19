---
UID: NF.printerextension.IPrintSchemaTicket.CommitAsync
title: IPrintSchemaTicket::CommitAsync method
author: windows-driver-content
description: Gets an asynchronous PrintTicket commit operation context.
old-location: print\iprintschematicket_commitasync.htm
old-project: print
ms.assetid: CFEDCABF-A875-4A69-954D-267765350E9D
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: IPrintSchemaTicket, IPrintSchemaTicket::CommitAsync, CommitAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: IPrintSchemaTicket.CommitAsync
req.alt-loc: printerextension.h
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
req.product: Windows 10 or later.
---

# IPrintSchemaTicket::CommitAsync method



## -description
Gets an  asynchronous PrintTicket commit operation context.



## -syntax

````
HRESULT CommitAsync(
  [in]  IPrintSchemaTicket         *pPrintTicketCommit,
  [out] IPrintSchemaAsyncOperation **ppAsyncOperation
);
````


## -parameters

### -param pPrintTicketCommit [in]

The print ticket to commit.


### -param ppAsyncOperation [out]

The asynchronous commit operation context.


## -returns
This method returns an <b>HRESULT</b> value.


## -remarks
To perform the commit operation, call the <a href="print.iprintschemaasyncoperation_start">IPrintSchemaAsyncOperation::Start</a> method to validate the given <i>pPrintTicketCommit</i> and then apply the validated PrintTicket settings to the current PrintTicket object. When the commit operation is completed or if an error occurs during the commit operation, the <a href="print.iprintschemaasyncoperationevent_completed">IPrintSchemaAsyncOperationEvent::Completed</a> event is fired.


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
Header

</th>
<td width="70%">
<dl>
<dt>Printerextension.h</dt>
</dl>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="..\printerextension\nn-printerextension-iprintschematicket.md">IPrintSchemaTicket</a>
</dt>
<dt>
<a href="print.iprintschemaasyncoperation_start">IPrintSchemaAsyncOperation::Start</a>
</dt>
<dt>
<a href="print.iprintschemaasyncoperationevent_completed">IPrintSchemaAsyncOperationEvent::Completed</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [print\print]:%20IPrintSchemaTicket::CommitAsync method%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
