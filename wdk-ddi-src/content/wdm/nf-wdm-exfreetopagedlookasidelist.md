---
UID: NF:wdm.ExFreeToPagedLookasideList
title: ExFreeToPagedLookasideList function (wdm.h)
description: The ExFreeToPagedLookasideList routine returns a pageable entry to the given lookaside list or to paged pool.
old-location: kernel\exfreetopagedlookasidelist.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["ExFreeToPagedLookasideList function"]
ms.keywords: ExFreeToPagedLookasideList, ExFreeToPagedLookasideList routine [Kernel-Mode Driver Architecture], k102_2d09255c-391a-4937-a991-99d88adf4233.xml, kernel.exfreetopagedlookasidelist, wdm/ExFreeToPagedLookasideList
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - ExFreeToPagedLookasideList
 - wdm/ExFreeToPagedLookasideList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - ExFreeToPagedLookasideList
---

# ExFreeToPagedLookasideList function


## -description

The <b>ExFreeToPagedLookasideList</b> routine returns a pageable entry to the given lookaside list or to paged pool.

## -parameters

### -param Lookaside [in, out]


A pointer to the <a href="/windows-hardware/drivers/kernel/eprocess">PAGED_LOOKASIDE_LIST</a> structure for the lookaside list, which the caller already initialized with <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-exinitializepagedlookasidelist">ExInitializePagedLookasideList</a>, which the caller already initialized with <b>ExInitializePagedLookasideList</b>.

### -param Entry [in]


A pointer to the entry to be freed. The caller obtained this pointer from a preceding call to <a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-exallocatefrompagedlookasidelist">ExAllocateFromPagedLookasideList</a>.

## -remarks

<b>ExFreeToPagedLookasideList</b> is the reciprocal of <b>ExAllocateFromPagedLookasideList</b>. It releases a caller-allocated entry back to the caller's lookaside list or to paged pool when that entry is no longer in use.

The same entry can be reallocated or another entry can be allocated later with a subsequent call to <b>ExAllocateFromPagedLookasideList</b>. The user of a lookaside list can allocate and free such entries dynamically, as needed, until it calls <b>ExDeletePagedLookasideList</b>. <b>ExDeletePagedLookasideList</b> releases any outstanding entries in the list before it clears the system state for the given lookaside list and returns control.

If the specified lookaside list has not yet reached the system-determined maximum number of entries, <b>ExFreeToPagedLookasideList</b> inserts the given entry at the front of the list. Otherwise, the buffer at <i>Entry</i> is released back to paged pool using the caller-supplied <i>Free</i> routine, if any, that was set up when the lookaside list was initialized or <b>ExFreePool</b>.

On Windows 2000, drivers must use the <b>-D_WIN2K_COMPAT_SLIST_USAGE</b> switch to successfully link code that uses <b>ExFreeToPagedLookasideList</b>.

For more information, see <a href="/windows-hardware/drivers/kernel/using-lookaside-lists">Using Lookaside Lists</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-exallocatefrompagedlookasidelist">ExAllocateFromPagedLookasideList</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-exdeletepagedlookasidelist">ExDeletePagedLookasideList</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-exinitializepagedlookasidelist">ExInitializePagedLookasideList</a>



<a href="/windows-hardware/drivers/kernel/eprocess">PAGED_LOOKASIDE_LIST</a>
