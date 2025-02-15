---
UID: NF:ntifs.RtlValidSid
title: RtlValidSid function (ntifs.h)
description: The RtlValidSid routine validates a security identifier (SID) by verifying that the revision number is within a known range and that the number of subauthorities is less than the maximum.
old-location: ifsk\rtlvalidsid.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["RtlValidSid function"]
ms.keywords: RtlValidSid, RtlValidSid routine [Installable File System Drivers], ifsk.rtlvalidsid, ntifs/RtlValidSid, rtlref_8d79344c-bb78-433f-be34-84e314b232a0.xml
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: 
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
req.dll: NtosKrnl.exe (kernel mode); Ntdll.dll (user mode)
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - RtlValidSid
 - ntifs/RtlValidSid
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
 - Ntdll.dll
api_name:
 - RtlValidSid
---

# RtlValidSid function


## -description

The <b>RtlValidSid</b> routine validates a security identifier (SID) by verifying that the revision number is within a known range and that the number of subauthorities is less than the maximum.

## -parameters

### -param Sid [in]


Pointer to the SID structure to validate.

## -returns

<b>RtlValidSid</b> returns <b>TRUE</b> if the security descriptor is valid, <b>FALSE</b> otherwise.

## -remarks

For more information about security and access control, see the documentation on these topics in the Microsoft Windows SDK.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlequalprefixsid">RtlEqualPrefixSid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlequalsid">RtlEqualSid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlinitializesid">RtlInitializeSid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtllengthrequiredsid">RtlLengthRequiredSid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtllengthsid">RtlLengthSid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlsubauthoritysid">RtlSubAuthoritySid</a>



<a href="/windows-hardware/drivers/ddi/ntifs/ns-ntifs-_sid">SID</a>
