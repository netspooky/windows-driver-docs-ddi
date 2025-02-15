---
UID: NF:ntifs.CcIsThereDirtyDataEx
title: CcIsThereDirtyDataEx function (ntifs.h)
description: The CcIsThereDirtyDataEx routine determines whether a volume contains any files that have dirty data in the system cache.
old-location: ifsk\ccistheredirtydataex.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["CcIsThereDirtyDataEx function"]
ms.keywords: CcIsThereDirtyDataEx, CcIsThereDirtyDataEx routine [Installable File System Drivers], ccref_13ae1f3e-b2ea-4bc6-a1cb-0101afd58d04.xml, ifsk.ccistheredirtydataex, ntifs/CcIsThereDirtyDataEx
req.header: ntifs.h
req.include-header: Ntifs.h, FltKernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - CcIsThereDirtyDataEx
 - ntifs/CcIsThereDirtyDataEx
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - CcIsThereDirtyDataEx
---

# CcIsThereDirtyDataEx function


## -description

The <b>CcIsThereDirtyDataEx</b> routine determines whether a volume contains any files that have dirty data in the system cache.

## -parameters

### -param Vpb [in]


A pointer to a volume parameter block (VPB) for the volume.

### -param NumberOfDirtyPages [in, optional]


An optional pointer to an unsigned long buffer that receives the number of dirty pages on the volume (associated with the Vpb parameter).

## -returns

The <b>CcIsThereDirtyDataEx</b> routine returns <b>TRUE</b> if the volume contains one or more cached files whose data has been modified in the cache, but not yet flushed to disk. Otherwise, this routine returns <b>FALSE</b>.

## -remarks

This routine will return <b>TRUE</b> if any dirty pages exist including temporary files (<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccistheredirtydata">CcIsThereDirtyData</a> ignores temporary files).  It will also return <b>TRUE</b> if there is any data currently queued to the volume.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccflushcache">CcFlushCache</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccistheredirtydata">CcIsThereDirtyData</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccpurgecachesection">CcPurgeCacheSection</a>
