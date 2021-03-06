---
UID: NF:iddcx.IddCxSwapChainReportFrameStatistics
title: IddCxSwapChainReportFrameStatistics function
author: windows-driver-content
description: An OS callback function the driver calls to report the frame statistics after it has processed a frame completely.
old-location: display\iddcxswapchainreportframestatistics.htm
old-project: display
ms.assetid: 0dd32160-93d4-4fb8-aed1-9267f38e9909
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IddCxSwapChainReportFrameStatistics, IddCxSwapChainReportFrameStatistics method [Display Devices], display.iddcxswapchainreportframestatistics, iddcx/IddCxSwapChainReportFrameStatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iddcx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
req.irql: "_Must_inspect_result_"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	iddcx.h
api_name:
-	IddCxSwapChainReportFrameStatistics
product:
- Windows
targetos: Windows
req.typenames: 
---

# IddCxSwapChainReportFrameStatistics function


## -description




                An OS callback function the driver calls to report the frame statistics after it has processed a frame completely


## -parameters




### -param SwapChainObject [in]

The swap-chain object whose current frame is being queried.


### -param pInArgs [in]

Input arguments to the function


## -returns




(NTSTATUS) The method returns STATUS_SUCCESS if the operation succeeds. Otherwise, this method may return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.
                    



