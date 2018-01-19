---
UID : NN:dbgeng.IDebugSymbols3
title : IDebugSymbols3
author : windows-driver-content
description : IDebugSymbols3 interface
old-location : debugger\idebugsymbols3.htm
old-project : debugger
ms.assetid : 3fce9384-93f3-4d81-b6ae-bda7a94da24a
ms.author : windowsdriverdev
ms.date : 1/10/2018
ms.keywords : IDebugSystemObjects4, IDebugSystemObjects4::SetImplicitThreadDataOffset, SetImplicitThreadDataOffset
ms.prod : windows-hardware
ms.technology : windows-devices
ms.topic : interface
req.header : dbgeng.h
req.include-header : Dbgeng.h
req.target-type : Windows
req.target-min-winverclnt : 
req.target-min-winversvr : 
req.kmdf-ver : 
req.umdf-ver : 
req.alt-api : IDebugSymbols3,IDebugSymbols3.IsManagedModule,IDebugSymbols3.SetScopeFromJitDebugInfo,IDebugSymbols3.GetSymbolEntryByToken,IDebugSymbols3.GetSymbolEntryOffsetRegions,IDebugSymbols3.GetSymbolEntryBySymbolEntry,IDebugSymbols3.GetSourceEntriesByOffset,IDebugSymbols3.GetSourceEntryString,IDebugSymbols3.GetSourceEntryStringWide,IDebugSymbols3.GetSourceEntryOffsetRegions,IDebugSymbols3.GetSourceEntryBySourceEntry
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

# IDebugSymbols3 interface



## Methods

<p>The <b>IDebugSymbols3</b> interface has these methods.</p>

| Method | Description |
| ---- |:---- |
| [dbgeng.IDebugSymbols3.AddSymbolOptions](nf-dbgeng-idebugsymbols3-addsymboloptions.md) | The AddSymbolOptions method turns on some of the engine's global symbol options. |
| [dbgeng.IDebugSymbols3.AddSyntheticModule](nf-dbgeng-idebugsymbols3-addsyntheticmodule.md) | The AddSyntheticModule method adds a synthetic module to the module list the debugger maintains for the current process. |
| [dbgeng.IDebugSymbols3.AddSyntheticModuleWide](nf-dbgeng-idebugsymbols3-addsyntheticmodulewide.md) | The AddSyntheticModuleWide method adds a synthetic module to the module list the debugger maintains for the current process. |
| [dbgeng.IDebugSymbols3.AddSyntheticSymbol](nf-dbgeng-idebugsymbols3-addsyntheticsymbol.md) | The AddSyntheticSymbol method adds a synthetic symbol to a module in the current process. |
| [dbgeng.IDebugSymbols3.AddSyntheticSymbolWide](nf-dbgeng-idebugsymbols3-addsyntheticsymbolwide.md) | The AddSyntheticSymbolWide method adds a synthetic symbol to a module in the current process. |
| [dbgeng.IDebugSymbols3.AddTypeOptions](nf-dbgeng-idebugsymbols3-addtypeoptions.md) | The AddTypeOptions method turns on some type formatting options for output generated by the engine. |
| [dbgeng.IDebugSymbols3.AppendImagePath](nf-dbgeng-idebugsymbols3-appendimagepath.md) | The AppendImagePath method appends directories to the executable image path. |
| [dbgeng.IDebugSymbols3.AppendImagePathWide](nf-dbgeng-idebugsymbols3-appendimagepathwide.md) | The AppendImagePathWide method appends directories to the executable image path. |
| [dbgeng.IDebugSymbols3.AppendSourcePath](nf-dbgeng-idebugsymbols3-appendsourcepath.md) | The AppendSourcePath method appends directories to the source path. |
| [dbgeng.IDebugSymbols3.AppendSourcePathWide](nf-dbgeng-idebugsymbols3-appendsourcepathwide.md) | The AppendSourcePathWide method appends directories to the source path. |
| [dbgeng.IDebugSymbols3.AppendSymbolPath](nf-dbgeng-idebugsymbols3-appendsymbolpath.md) | The AppendSymbolPath method appends directories to the symbol path. |
| [dbgeng.IDebugSymbols3.AppendSymbolPathWide](nf-dbgeng-idebugsymbols3-appendsymbolpathwide.md) | The AppendSymbolPathWide method appends directories to the symbol path. |
| [dbgeng.IDebugSymbols3.CreateSymbolGroup](nf-dbgeng-idebugsymbols3-createsymbolgroup.md) | The CreateSymbolGroup method creates a new symbol group. |
| [dbgeng.IDebugSymbols3.CreateSymbolGroup2](nf-dbgeng-idebugsymbols3-createsymbolgroup2.md) | The CreateSymbolGroup2 method creates a new symbol group. |
| [dbgeng.IDebugSymbols3.EndSymbolMatch](nf-dbgeng-idebugsymbols3-endsymbolmatch.md) | The EndSymbolMatch method releases the resources used by a symbol search. |
| [dbgeng.IDebugSymbols3.FindSourceFile](nf-dbgeng-idebugsymbols3-findsourcefile.md) | The FindSourceFile method searches the source path for a specified source file. |
| [dbgeng.IDebugSymbols3.FindSourceFileWide](nf-dbgeng-idebugsymbols3-findsourcefilewide.md) | The FindSourceFileWide method searches the source path for a specified source file. |
| [dbgeng.IDebugSymbols3.GetConstantName](nf-dbgeng-idebugsymbols3-getconstantname.md) | The GetConstantName method returns the name of the specified constant. |
| [dbgeng.IDebugSymbols3.GetConstantNameWide](nf-dbgeng-idebugsymbols3-getconstantnamewide.md) | The GetConstantNameWide method returns the name of the specified constant. |
| [dbgeng.IDebugSymbols3.GetCurrentScopeFrameIndex](nf-dbgeng-idebugsymbols3-getcurrentscopeframeindex.md) | The GetCurrentScopeFrameIndex method returns the index of the current stack frame in the call stack. |
| [dbgeng.IDebugSymbols3.GetFieldName](nf-dbgeng-idebugsymbols3-getfieldname.md) | The GetFieldName method returns the name of a field within a structure. |
| [dbgeng.IDebugSymbols3.GetFieldNameWide](nf-dbgeng-idebugsymbols3-getfieldnamewide.md) | The GetFieldNameWide method returns the name of a field within a structure. |
| [dbgeng.IDebugSymbols3.GetFieldOffset](nf-dbgeng-idebugsymbols3-getfieldoffset.md) | The GetFieldOffset method returns the offset of a field from the base address of an instance of a type. |
| [dbgeng.IDebugSymbols3.GetFieldOffsetWide](nf-dbgeng-idebugsymbols3-getfieldoffsetwide.md) | The GetFieldOffsetWide method returns the offset of a field from the base address of an instance of a type. |
| [dbgeng.IDebugSymbols3.GetFieldTypeAndOffset](nf-dbgeng-idebugsymbols3-getfieldtypeandoffset.md) | The GetFieldTypeAndOffset method returns the type of a field and its offset within a container. |
| [dbgeng.IDebugSymbols3.GetFieldTypeAndOffsetWide](nf-dbgeng-idebugsymbols3-getfieldtypeandoffsetwide.md) | The GetFieldTypeAndOffsetWide method returns the type of a field and its offset within a container. |
| [dbgeng.IDebugSymbols3.GetFunctionEntryByOffset](nf-dbgeng-idebugsymbols3-getfunctionentrybyoffset.md) | The GetFunctionEntryByOffset method returns the function entry information for a function. |
| [dbgeng.IDebugSymbols3.GetImagePath](nf-dbgeng-idebugsymbols3-getimagepath.md) | The GetImagePath method returns the executable image path. |
| [dbgeng.IDebugSymbols3.GetImagePathWide](nf-dbgeng-idebugsymbols3-getimagepathwide.md) | The GetImagePathWide method returns the executable image path. |
| [dbgeng.IDebugSymbols3.GetLineByOffset](nf-dbgeng-idebugsymbols3-getlinebyoffset.md) | The GetLineByOffset method returns the source filename and the line number within the source file of an instruction in the target. |
| [dbgeng.IDebugSymbols3.GetLineByOffsetWide](nf-dbgeng-idebugsymbols3-getlinebyoffsetwide.md) | The GetLineByOffsetWide method returns the source filename and the line number within the source file of an instruction in the target. |
| [dbgeng.IDebugSymbols3.GetModuleByIndex](nf-dbgeng-idebugsymbols3-getmodulebyindex.md) | The GetModuleByIndex method returns the location of the module with the specified index. |
| [dbgeng.IDebugSymbols3.GetModuleByModuleName](nf-dbgeng-idebugsymbols3-getmodulebymodulename.md) | The GetModuleByModuleName method searches through the target's modules for one with the specified name. |
| [dbgeng.IDebugSymbols3.GetModuleByModuleName2](nf-dbgeng-idebugsymbols3-getmodulebymodulename2.md) | The GetModuleByModuleName2 method searches through the process's modules for one with the specified name. |
| [dbgeng.IDebugSymbols3.GetModuleByModuleName2Wide](nf-dbgeng-idebugsymbols3-getmodulebymodulename2wide.md) | The GetModuleByModuleName2Wide method searches through the process's modules for one with the specified name. |
| [dbgeng.IDebugSymbols3.GetModuleByModuleNameWide](nf-dbgeng-idebugsymbols3-getmodulebymodulenamewide.md) | The GetModuleByModuleNameWide method searches through the target's modules for one with the specified name. |
| [dbgeng.IDebugSymbols3.GetModuleByOffset](nf-dbgeng-idebugsymbols3-getmodulebyoffset.md) | The GetModuleByOffset method searches through the target's modules for one whose memory allocation includes the specified location. |
| [dbgeng.IDebugSymbols3.GetModuleByOffset2](nf-dbgeng-idebugsymbols3-getmodulebyoffset2.md) | The GetModuleByOffset2 method searches through the process's modules for one whose memory allocation includes the specified location. |
| [dbgeng.IDebugSymbols3.GetModuleNames](nf-dbgeng-idebugsymbols3-getmodulenames.md) | The GetModuleNames method returns the names of the specified module. |
| [dbgeng.IDebugSymbols3.GetModuleNameString](nf-dbgeng-idebugsymbols3-getmodulenamestring.md) | The GetModuleNameString method returns the name of the specified module. |
| [dbgeng.IDebugSymbols3.GetModuleNameStringWide](nf-dbgeng-idebugsymbols3-getmodulenamestringwide.md) | The GetModuleNameStringWide method returns the name of the specified module. |
| [dbgeng.IDebugSymbols3.GetModuleParameters](nf-dbgeng-idebugsymbols3-getmoduleparameters.md) | The GetModuleParameters method returns parameters for modules in the target. |
| [dbgeng.IDebugSymbols3.GetModuleVersionInformation](nf-dbgeng-idebugsymbols3-getmoduleversioninformation.md) | The GetModuleVersionInformation method returns version information for the specified module. |
| [dbgeng.IDebugSymbols3.GetModuleVersionInformationWide](nf-dbgeng-idebugsymbols3-getmoduleversioninformationwide.md) | The GetModuleVersionInformationWide method returns version information for the specified module. |
| [dbgeng.IDebugSymbols3.GetNameByOffset](nf-dbgeng-idebugsymbols3-getnamebyoffset.md) | The GetNameByOffset method returns the name of the symbol at the specified location in the target's virtual address space. |
| [dbgeng.IDebugSymbols3.GetNameByOffsetWide](nf-dbgeng-idebugsymbols3-getnamebyoffsetwide.md) | The GetNameByOffsetWide method returns the name of the symbol at the specified location in the target's virtual address space. |
| [dbgeng.IDebugSymbols3.GetNearNameByOffset](nf-dbgeng-idebugsymbols3-getnearnamebyoffset.md) | The GetNearNameByOffset method returns the name of a symbol that is located near the specified location. |
| [dbgeng.IDebugSymbols3.GetNearNameByOffsetWide](nf-dbgeng-idebugsymbols3-getnearnamebyoffsetwide.md) | The GetNearNameByOffsetWide method returns the name of a symbol that is located near the specified location. |
| [dbgeng.IDebugSymbols3.GetNextSymbolMatch](nf-dbgeng-idebugsymbols3-getnextsymbolmatch.md) | The GetNextSymbolMatch method returns the next symbol found in a symbol search. |
| [dbgeng.IDebugSymbols3.GetNextSymbolMatchWide](nf-dbgeng-idebugsymbols3-getnextsymbolmatchwide.md) | The GetNextSymbolMatchWide method returns the next symbol found in a symbol search. |
| [dbgeng.IDebugSymbols3.GetNumberModules](nf-dbgeng-idebugsymbols3-getnumbermodules.md) | The GetNumberModules method returns the number of modules in the current process's module list. |
| [dbgeng.IDebugSymbols3.GetOffsetByLine](nf-dbgeng-idebugsymbols3-getoffsetbyline.md) | The GetOffsetByLine method returns the location of the instruction that corresponds to a specified line in the source code. |
| [dbgeng.IDebugSymbols3.GetOffsetByLineWide](nf-dbgeng-idebugsymbols3-getoffsetbylinewide.md) | The GetOffsetByLineWide method returns the location of the instruction that corresponds to a specified line in the source code. |
| [dbgeng.IDebugSymbols3.GetOffsetByName](nf-dbgeng-idebugsymbols3-getoffsetbyname.md) | The GetOffsetByName method returns the location of a symbol identified by name. |
| [dbgeng.IDebugSymbols3.GetOffsetByNameWide](nf-dbgeng-idebugsymbols3-getoffsetbynamewide.md) | The GetOffsetByNameWide method returns the location of a symbol identified by name. |
| [dbgeng.IDebugSymbols3.GetOffsetTypeId](nf-dbgeng-idebugsymbols3-getoffsettypeid.md) | The GetOffsetTypeId method returns the type ID of the symbol closest to the specified memory location. |
| [dbgeng.IDebugSymbols3.GetScope](nf-dbgeng-idebugsymbols3-getscope.md) | The GetScope method returns information about the current scope. |
| [dbgeng.IDebugSymbols3.GetScopeSymbolGroup](nf-dbgeng-idebugsymbols3-getscopesymbolgroup.md) | The GetScopeSymbolGroup method returns a symbol group containing the symbols in the current target's scope. |
| [dbgeng.IDebugSymbols3.GetScopeSymbolGroup2](nf-dbgeng-idebugsymbols3-getscopesymbolgroup2.md) | The GetScopeSymbolGroup2 method returns a symbol group containing the symbols in the current target's scope. |
| [dbgeng.IDebugSymbols3.GetSourceEntriesByLine](nf-dbgeng-idebugsymbols3-getsourceentriesbyline.md) | The GetSourceEntriesByLine method queries symbol information and returns locations in the target's memory that correspond to lines in a source file. |
| [dbgeng.IDebugSymbols3.GetSourceEntriesByLineWide](nf-dbgeng-idebugsymbols3-getsourceentriesbylinewide.md) | The GetSourceEntriesByLineWide method queries symbol information and returns locations in the target's memory that correspond to lines in a source file. |
| [dbgeng.IDebugSymbols3.GetSourceEntriesByOffset](nf-dbgeng-idebugsymbols3-getsourceentriesbyoffset.md) | Queries symbol information and returns locations in the target's memory by using an offset. |
| [dbgeng.IDebugSymbols3.GetSourceEntryBySourceEntry](nf-dbgeng-idebugsymbols3-getsourceentrybysourceentry.md) | Allows navigation within the source entries. |
| [dbgeng.IDebugSymbols3.GetSourceEntryOffsetRegions](nf-dbgeng-idebugsymbols3-getsourceentryoffsetregions.md) | Returns all memory regions known to be associated with a source entry. |
| [dbgeng.IDebugSymbols3.GetSourceEntryString](nf-dbgeng-idebugsymbols3-getsourceentrystring.md) | Queries symbol information and returns locations in the target's memory. |
| [dbgeng.IDebugSymbols3.GetSourceEntryStringWide](nf-dbgeng-idebugsymbols3-getsourceentrystringwide.md) | Queries symbol information and returns locations in the target's memory. |
| [dbgeng.IDebugSymbols3.GetSourceFileLineOffsets](nf-dbgeng-idebugsymbols3-getsourcefilelineoffsets.md) | The GetSourceFileLineOffsets method maps each line in a source file to a location in the target's memory. |
| [dbgeng.IDebugSymbols3.GetSourceFileLineOffsetsWide](nf-dbgeng-idebugsymbols3-getsourcefilelineoffsetswide.md) | The GetSourceFileLineOffsetsWide method maps each line in a source file to a location in the target's memory. |
| [dbgeng.IDebugSymbols3.GetSourcePath](nf-dbgeng-idebugsymbols3-getsourcepath.md) | The GetSourcePath method returns the source path. |
| [dbgeng.IDebugSymbols3.GetSourcePathElement](nf-dbgeng-idebugsymbols3-getsourcepathelement.md) | The GetSourcePathElement method returns an element from the source path. |
| [dbgeng.IDebugSymbols3.GetSourcePathElementWide](nf-dbgeng-idebugsymbols3-getsourcepathelementwide.md) | The GetSourcePathElementWide method returns an element from the source path. |
| [dbgeng.IDebugSymbols3.GetSourcePathWide](nf-dbgeng-idebugsymbols3-getsourcepathwide.md) | The GetSourcePathWide method returns the source path. |
| [dbgeng.IDebugSymbols3.GetSymbolEntriesByName](nf-dbgeng-idebugsymbols3-getsymbolentriesbyname.md) | The GetSymbolEntriesByName method returns the symbols whose names match a given pattern. |
| [dbgeng.IDebugSymbols3.GetSymbolEntriesByNameWide](nf-dbgeng-idebugsymbols3-getsymbolentriesbynamewide.md) | The GetSymbolEntriesByNameWide method returns the symbols whose names match a given pattern. |
| [dbgeng.IDebugSymbols3.GetSymbolEntriesByOffset](nf-dbgeng-idebugsymbols3-getsymbolentriesbyoffset.md) | The GetSymbolEntriesByOffset method returns the symbols which are located at a specified address. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryBySymbolEntry](nf-dbgeng-idebugsymbols3-getsymbolentrybysymbolentry.md) | Allows navigation within the symbol entry hierarchy. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryByToken](nf-dbgeng-idebugsymbols3-getsymbolentrybytoken.md) | Looks up a symbol by using a managed metadata token. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryInformation](nf-dbgeng-idebugsymbols3-getsymbolentryinformation.md) | The GetSymbolEntryInformation method returns the symbol entry information for a symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryOffsetRegions](nf-dbgeng-idebugsymbols3-getsymbolentryoffsetregions.md) | Returns all the memory regions known to be associated with a symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryString](nf-dbgeng-idebugsymbols3-getsymbolentrystring.md) | The GetSymbolEntryString method returns string information for the specified symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolEntryStringWide](nf-dbgeng-idebugsymbols3-getsymbolentrystringwide.md) | The GetSymbolEntryStringWide method returns string information for the specified symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolModule](nf-dbgeng-idebugsymbols3-getsymbolmodule.md) | The GetSymbolModule method returns the base address of module which contains the specified symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolModuleWide](nf-dbgeng-idebugsymbols3-getsymbolmodulewide.md) | The GetSymbolModuleWide method returns the base address of module which contains the specified symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolOptions](nf-dbgeng-idebugsymbols3-getsymboloptions.md) | The GetSymbolOptions method returns the engine's global symbol options. |
| [dbgeng.IDebugSymbols3.GetSymbolPath](nf-dbgeng-idebugsymbols3-getsymbolpath.md) | The GetSymbolPath method returns the symbol path. |
| [dbgeng.IDebugSymbols3.GetSymbolPathWide](nf-dbgeng-idebugsymbols3-getsymbolpathwide.md) | The GetSymbolPathWide method returns the symbol path. |
| [dbgeng.IDebugSymbols3.GetSymbolTypeId](nf-dbgeng-idebugsymbols3-getsymboltypeid.md) | The GetSymbolTypeId method returns the type ID and module of the specified symbol. |
| [dbgeng.IDebugSymbols3.GetSymbolTypeIdWide](nf-dbgeng-idebugsymbols3-getsymboltypeidwide.md) | The GetSymbolTypeIdWide method returns the type ID and module of the specified symbol. |
| [dbgeng.IDebugSymbols3.GetTypeId](nf-dbgeng-idebugsymbols3-gettypeid.md) | The GetTypeId method looks up the specified type and return its type ID. |
| [dbgeng.IDebugSymbols3.GetTypeIdWide](nf-dbgeng-idebugsymbols3-gettypeidwide.md) | The GetTypeIdWide method looks up the specified type and return its type ID. |
| [dbgeng.IDebugSymbols3.GetTypeName](nf-dbgeng-idebugsymbols3-gettypename.md) | The GetTypeName method returns the name of the type symbol specified by its type ID and module. |
| [dbgeng.IDebugSymbols3.GetTypeNameWide](nf-dbgeng-idebugsymbols3-gettypenamewide.md) | The GetTypeNameWide method returns the name of the type symbol specified by its type ID and module. |
| [dbgeng.IDebugSymbols3.GetTypeOptions](nf-dbgeng-idebugsymbols3-gettypeoptions.md) | The GetTypeOptions method returns the type formatting options for output generated by the engine. |
| [dbgeng.IDebugSymbols3.GetTypeSize](nf-dbgeng-idebugsymbols3-gettypesize.md) | The GetTypeSize method returns the number of bytes of memory an instance of the specified type requires. |
| [dbgeng.IDebugSymbols3.IsManagedModule](nf-dbgeng-idebugsymbols3-ismanagedmodule.md) | Checks whether the engine is using managed debugging support when it retrieves information for a module. |
| [dbgeng.IDebugSymbols3.OutputSymbolByOffset](nf-dbgeng-idebugsymbols3-outputsymbolbyoffset.md) | The OutputSymbolByOffset method looks up a symbol by address and prints the symbol name and other symbol information to the debugger console. |
| [dbgeng.IDebugSymbols3.OutputTypedDataPhysical](nf-dbgeng-idebugsymbols3-outputtypeddataphysical.md) | The OutputTypedDataPhysical method formats the contents of a variable in the target computer's physical memory, and then sends this to the output callbacks. |
| [dbgeng.IDebugSymbols3.OutputTypedDataVirtual](nf-dbgeng-idebugsymbols3-outputtypeddatavirtual.md) | The OutputTypedDataVirtual method formats the contents of a variable in the target's virtual memory, and then sends this to the output callbacks. |
| [dbgeng.IDebugSymbols3.ReadTypedDataPhysical](nf-dbgeng-idebugsymbols3-readtypeddataphysical.md) | The ReadTypedDataPhysical method reads the value of a variable from the target computer's physical memory. |
| [dbgeng.IDebugSymbols3.ReadTypedDataVirtual](nf-dbgeng-idebugsymbols3-readtypeddatavirtual.md) | The ReadTypedDataVirtual method reads the value of a variable in the target's virtual memory. |
| [dbgeng.IDebugSymbols3.Reload](nf-dbgeng-idebugsymbols3-reload.md) | The Reload method deletes the engine's symbol information for the specified module and reload these symbols as needed. |
| [dbgeng.IDebugSymbols3.ReloadWide](nf-dbgeng-idebugsymbols3-reloadwide.md) | The ReloadWide method deletes the engine's symbol information for the specified module and reload these symbols as needed. |
| [dbgeng.IDebugSymbols3.RemoveSymbolOptions](nf-dbgeng-idebugsymbols3-removesymboloptions.md) | The RemoveSymbolOptions method turns off some of the engine's global symbol options. |
| [dbgeng.IDebugSymbols3.RemoveSyntheticModule](nf-dbgeng-idebugsymbols3-removesyntheticmodule.md) | The RemoveSyntheticModule method removes a synthetic module from the module list the debugger maintains for the current process. |
| [dbgeng.IDebugSymbols3.RemoveSyntheticSymbol](nf-dbgeng-idebugsymbols3-removesyntheticsymbol.md) | The RemoveSyntheticSymbol method removes a synthetic symbol from a module in the current process. |
| [dbgeng.IDebugSymbols3.RemoveTypeOptions](nf-dbgeng-idebugsymbols3-removetypeoptions.md) | The RemoveTypeOptions method turns off some type formatting options for output generated by the engine. |
| [dbgeng.IDebugSymbols3.ResetScope](nf-dbgeng-idebugsymbols3-resetscope.md) | The ResetScope method resets the current scope to the default scope of the current thread. |
| [dbgeng.IDebugSymbols3.SetImagePath](nf-dbgeng-idebugsymbols3-setimagepath.md) | The SetImagePath method sets the executable image path. |
| [dbgeng.IDebugSymbols3.SetImagePathWide](nf-dbgeng-idebugsymbols3-setimagepathwide.md) | The SetImagePathWide method sets the executable image path. |
| [dbgeng.IDebugSymbols3.SetScope](nf-dbgeng-idebugsymbols3-setscope.md) | The SetScope method sets the current scope. |
| [dbgeng.IDebugSymbols3.SetScopeFrameByIndex](nf-dbgeng-idebugsymbols3-setscopeframebyindex.md) | The SetScopeFrameByIndex method sets the current scope to the scope of one of the frames on the call stack. |
| [dbgeng.IDebugSymbols3.SetScopeFromJitDebugInfo](nf-dbgeng-idebugsymbols3-setscopefromjitdebuginfo.md) | Recovers just-in-time (JIT) debugging information and sets current debugger scope context based on that information. |
| [dbgeng.IDebugSymbols3.SetScopeFromStoredEvent](nf-dbgeng-idebugsymbols3-setscopefromstoredevent.md) | The SetScopeFromStoredEvent method sets the current scope to the scope of the stored event. |
| [dbgeng.IDebugSymbols3.SetSourcePath](nf-dbgeng-idebugsymbols3-setsourcepath.md) | The SetSourcePath method sets the source path. |
| [dbgeng.IDebugSymbols3.SetSourcePathWide](nf-dbgeng-idebugsymbols3-setsourcepathwide.md) | The SetSourcePathWide method sets the source path. |
| [dbgeng.IDebugSymbols3.SetSymbolOptions](nf-dbgeng-idebugsymbols3-setsymboloptions.md) | The SetSymbolOptions method changes the engine's global symbol options. |
| [dbgeng.IDebugSymbols3.SetSymbolPath](nf-dbgeng-idebugsymbols3-setsymbolpath.md) | The SetSymbolPath method sets the symbol path. |
| [dbgeng.IDebugSymbols3.SetSymbolPathWide](nf-dbgeng-idebugsymbols3-setsymbolpathwide.md) | The SetSymbolPathWide method sets the symbol path. |
| [dbgeng.IDebugSymbols3.SetTypeOptions](nf-dbgeng-idebugsymbols3-settypeoptions.md) | The SetTypeOptions method changes the type formatting options for output generated by the engine. |
| [dbgeng.IDebugSymbols3.StartSymbolMatch](nf-dbgeng-idebugsymbols3-startsymbolmatch.md) | The StartSymbolMatch method initializes a search for symbols whose names match a given pattern. |
| [dbgeng.IDebugSymbols3.StartSymbolMatchWide](nf-dbgeng-idebugsymbols3-startsymbolmatchwide.md) | The StartSymbolMatchWide method initializes a search for symbols whose names match a given pattern. |
| [dbgeng.IDebugSymbols3.WriteTypedDataPhysical](nf-dbgeng-idebugsymbols3-writetypeddataphysical.md) | The WriteTypedDataPhysical method writes the value of a variable in the target computer's physical memory. |
| [dbgeng.IDebugSymbols3.WriteTypedDataVirtual](nf-dbgeng-idebugsymbols3-writetypeddatavirtual.md) | The WriteTypedDataVirtual method writes data to the target's virtual address space. The number of bytes written is the size of the specified type. |

## Remarks



## Requirements
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Windows Driver kit version** |  |
| **Target platform** | Windows |
| **Minimum UMDF version** |  |
| **Header** | dbgeng.h (include Dbgeng.h) |
| **DLL** |  |

    ## See Also

        <dl>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols.md">IDebugSymbols</a>
</dt>
<dt>
<a href="..\dbgeng\nn-dbgeng-idebugsymbols2.md">IDebugSymbols2</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [debugger\debugger]:%20IDebugSymbols3 interface%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>