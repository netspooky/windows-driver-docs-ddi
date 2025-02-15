---
UID: NS:d3d12umddi.D3D12DDI_D3D12_OPTIONS_DATA_0041
title: D3D12DDI_D3D12_OPTIONS_DATA_0041 (d3d12umddi.h)
description: The D3D12DDI_D3D12_OPTIONS_DATA_0041 structure contains display options data used by user-mode display driver functions.
ms.date: 10/19/2018
keywords: ["D3D12DDI_D3D12_OPTIONS_DATA_0041 structure"]
ms.keywords: D3D12DDI_D3D12_OPTIONS_DATA_0041, D3D12DDI_D3D12_OPTIONS_DATA_0041,
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12DDI_D3D12_OPTIONS_DATA_0041
targetos: Windows
tech.root: display
ms.custom: 19H1
f1_keywords:
 - D3D12DDI_D3D12_OPTIONS_DATA_0041
 - d3d12umddi/D3D12DDI_D3D12_OPTIONS_DATA_0041
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12umddi.h
api_name:
 - D3D12DDI_D3D12_OPTIONS_DATA_0041
product:
 - Windows
dev_langs:
 - c++
---

# D3D12DDI_D3D12_OPTIONS_DATA_0041 structure


## -description

Display options data.

## -struct-fields

### -field ResourceBindingTier

Resource binding tier.

### -field ConservativeRasterizationTier

Conservative rasterization tier.

### -field TiledResourcesTier

Tiled resource tier.

### -field CrossNodeSharingTier

Cross node sharing tier.

### -field VPAndRTArrayIndexFromAnyShaderFeedingRasterizerSupportedWithoutGSEmulation

VP and RT array index from any shader feeding rasterizer supported without GS emulation.

### -field OutputMergerLogicOp

Output merger logic option.

### -field ResourceHeapTier

Resource heap tier.

### -field DepthBoundsTestSupported

Depth bounds test supported.

### -field ProgrammableSamplePositionsTier

Programmable sample positions tier.

### -field CopyQueueTimestampQueriesSupported

Copy queue timestamp queries supported.

### -field WriteBufferImmediateQueueFlags

Write buffer immediate queue flags.

### -field ViewInstancingTier

View instancing tier.

### -field BarycentricsSupported

Barycentrics supported.

### -field ReservedBufferPlacementSupported

Reserved buffer placement supported. Supports only just 64KB aligned MSAA.

### -field Deterministic64KBUndefinedSwizzle

Deterministic 64KB undefined swizzle.

