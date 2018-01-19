---
UID : NC:scsiwmi.PSCSIWMI_SET_DATAITEM
title : PSCSIWMI_SET_DATAITEM
author : windows-driver-content
description : A miniport driver's HwScsiWmiSetDataItem routine is called to change a single data item in an instance of a data block.
old-location : storage\hwscsiwmisetdataitem.htm
old-project : storage
ms.assetid : 24b8415e-4326-4aef-bcbb-fabffa25c7d6
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _SCSISCAN_INFO, *PSCSISCAN_INFO, SCSISCAN_INFO
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : scsiwmi.h
req.include-header : Scsiwmi.h
req.target-type : Desktop
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : HwScsiWmiSetDataItem
req.alt-loc : scsiwmi.h
req.ddi-compliance : 
req.unicode-ansi : 
req.idl : 
req.max-support : 
req.namespace : 
req.assembly : 
req.type-library : 
req.lib : 
req.dll : 
req.irql : 
req.typenames : "*PSCSISCAN_INFO, SCSISCAN_INFO"
req.product : Windows 10 or later.
---


# PSCSIWMI_SET_DATAITEM callback function
A miniport driver's <b>HwScsiWmiSetDataItem</b> routine is called to change a single data item in an instance of a data block. This routine is optional.

## Syntax

```
PSCSIWMI_SET_DATAITEM PscsiwmiSetDataitem;

BOOLEAN PscsiwmiSetDataitem(
  PVOID DeviceContext,
  PSCSIWMI_REQUEST_CONTEXT RequestContext,
  ULONG GuidIndex,
  ULONG InstanceIndex,
  ULONG DataItemId,
  ULONG BufferSize,
  PUCHAR Buffer
)
{...}
```

## Parameters

`DeviceContext`

Points to the miniport driver-defined context value passed to <a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a>.

`RequestContext`

Points to the SCSIWMI_REQUEST_CONTEXT structure that the miniport driver passed to <a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a>.

`GuidIndex`

Specifies the data block by its index into the list of GUIDs in the SCSI_WMILIB_CONTEXT structure that the miniport driver passed to <a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a>.

`InstanceIndex`

If the block specified by <i>GuidIndex</i> has multiple instances, <i>InstanceIndex</i> specifies the instance.

`DataItemId`

Specifies the ID of the data item to set.

`BufferSize`

Specifies the size in bytes of the buffer at <i>Buffer</i>.

`Buffer`

Points to a buffer that contains the new value for the data item.


## Return Value

<b>HwScsiWmiSetDataItem</b> returns SRB_STATUS_PENDING if the request is pending, or a nonzero SRB status value if the request was completed.  The SRB status value returned by this routine is the same as what was passed in to <b>HwScsiWmiSetDataItem</b>.  Although the return value data type is BOOLEAN, the <b>HwScsiWmiSetDataItem</b> routine actually returns an SRB status value.

## Remarks

When a miniport driver receives an SRB in which the <b>Function</b> member is set to SRB_FUNCTION_WMI, it calls <a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a> with a pointer to an initialized SCSI_WMILIB_CONTEXT structure and <i>MinorFunction</i> set to <b>Srb-&gt;WmiSubFunction</b>. The SCSI port driver calls the miniport driver's <b>HwScsiWmiSetDataItem</b> routine if <i>MinorFunction</i> indicates a request to change an item in an instance of a data block.

If a miniport driver does not implement a <b>HwScsiWmiSetDataItem</b> routine, it must set <b>SetWmiDataItem</b> to <b>NULL</b> in the SCSI_WMILIB_CONTEXT the miniport driver passes to <a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a>. In this circumstance, the port driver will return SRB_STATUS_ERROR to the caller.

If the request does not pend, the miniport driver should call <a href="..\scsiwmi\nf-scsiwmi-scsiportwmipostprocess.md">ScsiPortWmiPostProcess</a> in its <b>HwScsiWmiSetDataItem</b> callback. Otherwise, the miniport driver should call <b>ScsiPortWmiPostProcess</b> when the request is actually completed. The miniport driver should call <b>ScsiPortWmiPostProcess</b> with the appropriate <i>SrbStatus</i> value.

If the item is read-only, the miniport driver calls <a href="..\scsiwmi\nf-scsiwmi-scsiportwmipostprocess.md">ScsiPortWmiPostProcess</a> with SRB_STATUS_ERROR. Otherwise, the miniport driver changes the item and calls <b>ScsiPortWmiPostProcess</b> with SRB_STATUS_SUCCESS.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Desktop |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | scsiwmi.h (include Scsiwmi.h) |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\scsiwmi\ns-scsiwmi-_scsiwmilib_context.md">SCSI_WMILIB_CONTEXT</a>
</dt>
<dt>
<a href="..\scsiwmi\nf-scsiwmi-scsiportwmidispatchfunction.md">ScsiPortWmiDispatchFunction</a>
</dt>
<dt>
<a href="..\scsiwmi\nf-scsiwmi-scsiportwmipostprocess.md">ScsiPortWmiPostProcess</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20HwScsiWmiSetDataItem callback function%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>