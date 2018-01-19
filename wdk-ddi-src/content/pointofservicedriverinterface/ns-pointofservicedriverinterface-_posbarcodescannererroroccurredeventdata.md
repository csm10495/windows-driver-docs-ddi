---
UID : NS:pointofservicedriverinterface._PosBarcodeScannerErrorOccurredEventData
title : _PosBarcodeScannerErrorOccurredEventData
author : windows-driver-content
description : This structure contains the error data that is passed to the BarcodeScannerErrorOccurred event.
old-location : pos\posbarcodescannererroroccurredeventdata.htm
old-project : pos
ms.assetid : c9e18ed0-bc34-49ed-a31e-20c82d43860f
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _PosBarcodeScannerErrorOccurredEventData, PosBarcodeScannerErrorOccurredEventData
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : struct
req.header : pointofservicedriverinterface.h
req.include-header : PointOfServiceDriverInterface.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : PosBarcodeScannerErrorOccurredEventData
req.alt-loc : PointOfServiceDriverInterface.h
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
req.typenames : PosBarcodeScannerErrorOccurredEventData
---

# _PosBarcodeScannerErrorOccurredEventData structure
This structure contains the error data that is passed to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn757464">BarcodeScannerErrorOccurred</a> event.

## Syntax
````
typedef struct _PosBarcodeScannerErrorOccurredEventData {
  PosEventDataHeader                     Header;
  LONG                                   IsRetriable;
  UnifiedPosErrorSeverity                Severity;
  UINT32                                 VendorErrorCode;
  UnifiedPosErrorReason                  Reason;
  UINT32                                 ExtendedReason;
  UINT32                                 MessageLength;
  PosBarcodeScannerDataReceivedEventData PartialData;
} PosBarcodeScannerErrorOccurredEventData;
````

## Members

        
            `ExtendedReason`

            Contains additional data about the reason for the error.
        
            `Header`

            The <a href="..\pointofservicedriverinterface\ns-pointofservicedriverinterface-_poseventdataheader.md">PosEventDataHeader</a> structure that describes the amount of memory, in bytes, of the <b>PosBarcodeScannerErrorOccurredEventData</b> structure and trailing error message and scan data.
        
            `IsRetriable`

            Indicates whether <a href="http://go.microsoft.com/fwlink/p/?LinkId=314125">ReadFile</a> can be called again to read this event
        
            `MessageLength`

            Indicates the length, in bytes, of the error message.
        
            `PartialData`

            If a scanning error occurs, and some scan data was obtained, the partial scan data will be available in this parameter.
        
            `Reason`

            Contains a value in the <a href="..\pointofservicecommontypes\ne-pointofservicecommontypes-driverunifiedposerrorreason.md">UnifiedPosErrorReason</a> enumeration indicating the reason for the error.
        
            `Severity`

            Contains a value in the <a href="..\pointofservicecommontypes\ne-pointofservicecommontypes-driverunifiedposerrorseverity.md">UnifiedPosErrorSeverity</a> enumeration indicating the severity of the error.
        
            `VendorErrorCode`

            Contains a vendor-specific error code.

    ## Remarks
        The error data should fill the buffer as shown in the following table (in order).

<b>PosBarcodeScannerErrorOccurredEventData</b> structure

sizeof(<b>PosBarcodeScannerErrorOccurredEventData</b>)

Error message text

<b>MessageLength</b>

Partial scan data

<b>PartialData.ScanDataLength</b>

Label data

<b>PartialData.ScanDataLabelLength</b></p>

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | pointofservicedriverinterface.h (include PointOfServiceDriverInterface.h) |