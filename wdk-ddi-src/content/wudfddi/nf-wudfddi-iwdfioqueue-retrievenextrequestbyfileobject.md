---
UID: NF.wudfddi.IWDFIoQueue.RetrieveNextRequestByFileObject
title: IWDFIoQueue::RetrieveNextRequestByFileObject method
author: windows-driver-content
description: The RetrieveNextRequestByFileObject method retrieves from an I/O queue the next I/O request whose file object matches the specified file object.
old-location: wdf\iwdfioqueue_retrievenextrequestbyfileobject.htm
old-project: wdf
ms.assetid: 136b7582-b974-44fb-8026-e9678ae6623c
ms.author: windowsdriverdev
ms.date: 12/15/2017
ms.keywords: IWDFIoQueue, IWDFIoQueue::RetrieveNextRequestByFileObject, RetrieveNextRequestByFileObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.alt-api: IWDFIoQueue.RetrieveNextRequestByFileObject
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

# IWDFIoQueue::RetrieveNextRequestByFileObject method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>RetrieveNextRequestByFileObject</b> method retrieves from an I/O queue the next I/O request whose file object matches the specified file object.



## -syntax

````
HRESULT RetrieveNextRequestByFileObject(
  [in]  IWDFFile      *pFileObject,
  [out] IWDFIoRequest **ppRequest
);
````


## -parameters

### -param pFileObject [in]

A pointer to the <a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a> interface for the file object that is used to retrieve the next I/O request whose file object matches this supplied file object. 


### -param ppRequest [out]

A pointer to a buffer that receives a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfiorequest.md">IWDFIoRequest</a> interface for the next request object whose file object matches the supplied file object, or receives <b>NULL</b> if the queue is empty or if the next request is not found.


## -returns
<b>RetrieveNextRequestByFileObject</b> returns one of the following values:
<dl>
<dt><b>S_OK</b></dt>
</dl>The next I/O request was successfully retrieved from the I/O queue.
<dl>
<dt><b>HRESULT_FROM_NT(STATUS_WDF_PAUSED)</b></dt>
</dl>The queue is not dispatching requests. This situation occurs if the device undergoes a power state transition and all of the queues are stopped from dispatching requests or if the driver explicitly called <a href="wdf.iwdfioqueue_stop">IWDFIoQueue::Stop</a> to stop dispatching requests. This situation can also occur if the driver attempts to remove a request from a manual queue that is power managed and that is powered down or if the queue is paused.
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NO_MORE_ITEMS)</b></dt>
</dl>No requests were in the queue.
<dl>
<dt><b>HRESULT_FROM_NT(STATUS_INVALID_DEVICE_STATE)</b></dt>
</dl>The call was made to retrieve the request from a parallel queue.

 

<b>RetrieveNextRequestByFileObject</b> might also return other HRESULT values.


## -remarks
If a driver configures an I/O queue for manual dispatching of I/O requests, the driver can call the <b>RetrieveNextRequestByFileObject</b> method to obtain the next request whose file object matches the supplied file object from the queue. For more information about manually dispatching I/O requests, see <a href="wdf.configuring_dispatch_mode_for_an_i_o_queue">Configuring Dispatch Mode for an I/O Queue</a>. 

If multiple I/O requests whose file objects match the file object that the <i>pFileObject</i> parameter points to exist in the I/O queue, the first I/O request is returned.

For a code example of how to use the <b>RetrieveNextRequestByFileObject</b> method, see <a href="wdf.iwdfioqueue_retrievenextrequest">IWDFIoQueue::RetrieveNextRequest</a>.


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
1.5

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
<a href="..\wudfddi\nn-wudfddi-iwdfioqueue.md">IWDFIoQueue</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdffile.md">IWDFFile</a>
</dt>
<dt>
<a href="wdf.iwdfioqueue_retrievenextrequest">IWDFIoQueue::RetrieveNextRequest</a>
</dt>
<dt>
<a href="wdf.iwdfioqueue_stop">IWDFIoQueue::Stop</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfiorequest.md">IWDFIoRequest</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFIoQueue::RetrieveNextRequestByFileObject method%20 RELEASE:%20(12/15/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
