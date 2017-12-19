---
UID: NF.wdm.NtOpenResourceManager
title: NtOpenResourceManager function
author: windows-driver-content
description: The ZwOpenResourceManager routine returns a handle to an existing resource manager object.
old-location: kernel\zwopenresourcemanager.htm
old-project: kernel
ms.assetid: baa12e3c-dc17-4fef-bce4-29c50328314c
ms.author: windowsdriverdev
ms.date: 12/15/2017
ms.keywords: NtOpenResourceManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later operating system versions.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.alt-api: ZwOpenResourceManager,NtOpenResourceManager
req.alt-loc: NtosKrnl.exe
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
req.product: Windows 10 or later.
---

# NtOpenResourceManager function



## -description
The <b>ZwOpenResourceManager</b> routine returns a handle to an existing <a href="https://msdn.microsoft.com/b44f2035-ee9f-453b-b12d-89ca36a8b280">resource manager object</a>.



## -syntax

````
NTSTATUS ZwOpenResourceManager(
  _Out_    PHANDLE            ResourceManagerHandle,
  _In_     ACCESS_MASK        DesiredAccess,
  _In_     HANDLE             TmHandle,
  _In_     LPGUID             ResourceManagerGuid,
  _In_opt_ POBJECT_ATTRIBUTES ObjectAttributes
);
````


## -parameters

### -param ResourceManagerHandle [out]

A pointer to a caller-allocated variable that receives the resource manager handle if the call to <b>ZwOpenResourceManager</b> succeeds.


### -param DesiredAccess [in]

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> value that specifies the caller's requested access to the resource manager object. For more information about how to specify this parameter, see the <i>DesiredAccess</i> parameter of <a href="kernel.zwcreateresourcemanager">ZwCreateResourceManager</a>. This parameter cannot be zero.


### -param TmHandle [in]

A handle to a transaction manager object that was obtained by a previous call to <a href="kernel.zwcreatetransactionmanager">ZwCreateTransactionManager</a> or <a href="kernel.zwopentransactionmanager">ZwOpenTransactionManager</a>. 


### -param ResourceManagerGuid [in]

A pointer to the GUID that identifies the resource manager to open. 


### -param ObjectAttributes [in, optional]

A pointer to an <a href="kernel.object_attributes">OBJECT_ATTRIBUTES</a> structure that specifies the object's attributes. Use the <a href="kernel.initializeobjectattributes">InitializeObjectAttributes</a> routine to initialize this structure, but specify only that routine's <i>InitializedAttributes</i> and <i>Attributes</i> parameters. If the caller is not running in a system thread context, it must set the OBJ_KERNEL_HANDLE flag in the <i>Attributes</i> parameter. This parameter is optional and can be <b>NULL</b>. 


## -returns
<b>ZwOpenResourceManager</b> returns STATUS_SUCCESS if the operation succeeds. Otherwise, this routine might return one of the following values: 
<dl>
<dt><b>STATUS_OBJECT_TYPE_MISMATCH</b></dt>
</dl>The handle that <i>TmHandle</i> specifies is not a handle to a transaction object.
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>The handle that <i>TmHandle</i> specifies is invalid.
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>The caller does not have appropriate access to the specified transaction manager object.
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>The <i>DesiredAccess</i> parameter is zero or the <i>ResourceManagerGuid</i> parameter is invalid.
<dl>
<dt><b>STATUS_RESOURCEMANAGER_NOT_FOUND</b></dt>
</dl>The specified resource manager could not be found.
<dl>
<dt><b>STATUS_TRANSACTIONMANAGER_NOT_ONLINE</b></dt>
</dl>The specified transaction manager is not online.

 

The routine might return other <a href="https://msdn.microsoft.com/library/windows/hardware/ff557697">NTSTATUS values</a>.


## -remarks
Typically, a TPS component calls <b>ZwOpenResourceManager</b> after it receives an enlistment GUID from another TPS component that had previously called <a href="kernel.zwcreateresourcemanager">ZwCreateResourceManager</a>. Most TPS designs do not require calling <b>ZwOpenResourceManager</b>.

A resource manager that calls <b>ZwOpenResourceManager</b> must eventually call <a href="kernel.zwclose">ZwClose</a> to close the object handle.

For more information about <b>ZwOpenResourceManager</b>, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554272">KTM Objects</a>.

<b>NtOpenResourceManager</b> and <b>ZwOpenResourceManager</b> are two versions of the same Windows Native System Services routine.

For calls from kernel-mode drivers, the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a Windows Native System Services routine can behave differently in the way that they handle and interpret input parameters. For more information about the relationship between the <b>Nt<i>Xxx</i></b> and <b>Zw<i>Xxx</i></b> versions of a routine, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>.


## -requirements
<table>
<tr>
<th width="30%">
Target platform

</th>
<td width="70%">
<dl>
<dt><a href="http://go.microsoft.com/fwlink/p/?linkid=531356" target="_blank">Universal</a></dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
Version

</th>
<td width="70%">
Available in Windows Vista and later operating system versions.

</td>
</tr>
<tr>
<th width="30%">
Header

</th>
<td width="70%">
<dl>
<dt>Wdm.h (include Wdm.h or Ntifs.h)</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
Library

</th>
<td width="70%">
<dl>
<dt>NtosKrnl.lib</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
DLL

</th>
<td width="70%">
<dl>
<dt>NtosKrnl.exe</dt>
</dl>
</td>
</tr>
<tr>
<th width="30%">
IRQL

</th>
<td width="70%">
PASSIVE_LEVEL

</td>
</tr>
<tr>
<th width="30%">
DDI compliance rules

</th>
<td width="70%">
<a href="devtest.wdm_powerirpddis">PowerIrpDDis</a>, <a href="devtest.storport_hwstorportprohibitedddis">HwStorPortProhibitedDDIs</a>
</td>
</tr>
</table>

## -see-also
<dl>
<dt>
<a href="kernel.initializeobjectattributes">InitializeObjectAttributes</a>
</dt>
<dt>
<a href="kernel.object_attributes">OBJECT_ATTRIBUTES</a>
</dt>
<dt>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff565438">Using Nt and Zw Versions of the Native System Services Routines</a>
</dt>
<dt>
<a href="kernel.zwclose">ZwClose</a>
</dt>
<dt>
<a href="kernel.zwcreateresourcemanager">ZwCreateResourceManager</a>
</dt>
<dt>
<a href="kernel.zwcreatetransactionmanager">ZwCreateTransactionManager</a>
</dt>
<dt>
<a href="kernel.zwopentransactionmanager">ZwOpenTransactionManager</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20ZwOpenResourceManager routine%20 RELEASE:%20(12/15/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
