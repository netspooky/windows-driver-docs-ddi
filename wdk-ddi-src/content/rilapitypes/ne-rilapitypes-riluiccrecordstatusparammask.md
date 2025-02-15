---
UID: NE:rilapitypes.RILUICCRECORDSTATUSPARAMMASK
title: RILUICCRECORDSTATUSPARAMMASK (rilapitypes.h)
description: "Microsoft reserves the RILUICCRECORDSTATUSPARAMMASK enumeration for internal use only. Don't use this enumeration in your code."
old-location: netvista\riluiccrecordstatusparammask_2.htm
tech.root: netvista
ms.date: 02/26/2018
keywords: ["RILUICCRECORDSTATUSPARAMMASK enumeration"]
ms.keywords: RILUICCRECORDSTATUSPARAMMASK, RILUICCRECORDSTATUSPARAMMASK enumeration [Network Drivers Starting with Windows Vista], RIL_PARAM_URS_ALL, RIL_PARAM_URS_FILELOCKSTATUS, RIL_PARAM_URS_ITEMCOUNT, RIL_PARAM_URS_SIZE, netvista.riluiccrecordstatusparammask_2, rilapitypes/RILUICCRECORDSTATUSPARAMMASK, rilapitypes/RIL_PARAM_URS_ALL, rilapitypes/RIL_PARAM_URS_FILELOCKSTATUS, rilapitypes/RIL_PARAM_URS_ITEMCOUNT, rilapitypes/RIL_PARAM_URS_SIZE
req.header: rilapitypes.h
req.include-header: 
req.target-type: Windows
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
req.lib: NtosKrnl.exe
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RILUICCRECORDSTATUSPARAMMASK
req.product: Windows 10 or later.
f1_keywords:
 - RILUICCRECORDSTATUSPARAMMASK
 - rilapitypes/RILUICCRECORDSTATUSPARAMMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rilapitypes.h
api_name:
 - RILUICCRECORDSTATUSPARAMMASK
---

# RILUICCRECORDSTATUSPARAMMASK enumeration (rilapitypes.h)


## -description

This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.

## -enum-fields

### -field RIL_PARAM_URS_RECORDTYPE

### -field RIL_PARAM_URS_ITEMCOUNT

### -field RIL_PARAM_URS_SIZE

### -field RIL_PARAM_URS_FILELOCKSTATUS

### -field RIL_PARAM_URS_ALL

## -syntax

```cpp
typedef enum _RILUICCRECORDSTATUSPARAMMASK {
  RIL_PARAM_URS_ITEMCOUNT,
  RIL_PARAM_URS_SIZE,
  RIL_PARAM_URS_FILELOCKSTATUS,
  RIL_PARAM_URS_ALL
} RILUICCRECORDSTATUSPARAMMASK;
```

