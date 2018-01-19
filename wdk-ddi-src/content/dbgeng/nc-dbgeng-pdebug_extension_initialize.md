---
UID : NC:dbgeng.PDEBUG_EXTENSION_INITIALIZE
title : PDEBUG_EXTENSION_INITIALIZE
author : windows-driver-content
description : The DebugExtensionInitialize callback function is called by the engine after loading a DbgEng extension DLL.C++ CALLBACK* PDEBUG_EXTENSION_INITIALIZE DebugExtensionInitialize;
old-location : debugger\debugextensioninitialize.htm
old-project : debugger
ms.assetid : 2e68fa38-55fc-4538-ae97-ed943d5381be
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : _DOT4_ACTIVITY, *PDOT4_ACTIVITY, DOT4_ACTIVITY
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : callback
req.header : dbgeng.h
req.include-header : 
req.target-type : Universal
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : DebugExtensionInitialize
req.alt-loc : dbgeng.h
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
req.typenames : "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---


# PDEBUG_EXTENSION_INITIALIZE callback function
The <b>DebugExtensionInitialize</b> callback function is called by the engine after loading a DbgEng extension DLL.

## Syntax

```
PDEBUG_EXTENSION_INITIALIZE PdebugExtensionInitialize;

HRESULT PdebugExtensionInitialize(
  PULONG Version,
  PULONG Flags
)
{...}
```

## Parameters

`Version`

Receives the version of the extension.  The high 16 bits contain the major version number, and the low 16 bits contain the minor version number.

`Flags`

Set this to zero. (Reserved for future use.)


## Return Value

<dl>
<dt><b>S_OK</b></dt>
</dl>The extension was successfully initialized.

 

Any other value indicates that the extension DLL was unable to initialize and the engine will unload it.

## Remarks

The engine looks for this function by name in each extension DLL.  This function must be exported by a DbgEng extension DLL.

The version number can be set by using the macro DEBUG_EXTENSION_VERSION found in dbgeng.h, for example:

Implementations of this function should initialize any global variables required by the extension DLL.

There may or may not be a session active when this function is called, so the extension should not assume that it is able to query session information.

 The function type is defined as PDEBUG_EXTENSION_INITIALIZE in dbgeng.h.

## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Universal |
| **Minimum KMDF version** |  |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h |
| **Library** |  |
| **IRQL** |  |
| **DDI compliance rules** |  |

## See Also

<dl>
<dt>
<a href="..\dbgeng\nc-dbgeng-pdebug_extension_uninitialize.md">DebugExtensionUninitialize</a>
</dt>
<dt>
<a href="..\dbgeng\nc-dbgeng-pdebug_extension_notify.md">DebugExtensionNotify</a>
</dt>
<dt>
<a href="..\dbgeng\nc-dbgeng-pdebug_extension_known_struct.md">KnownStructOutput</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20PDEBUG_EXTENSION_INITIALIZE callback function%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>