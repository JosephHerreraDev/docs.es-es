---
title: ICorDebugBreakpoint::IsActive (Método)
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::IsActive
helpviewer_keywords:
- ICorDebugBreakpoint::IsActive method [.NET Framework debugging]
- IsActive method, ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: 06e583d6-d88a-4ff5-bb95-5c48618a461c
topic_type:
- apiref
ms.openlocfilehash: 64a30ca85a75ebd11918ff630daffbb85c97f6dc
ms.sourcegitcommit: 957c49696eaf048c284ef8f9f8ffeb562357ad95
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2020
ms.locfileid: "82894723"
---
# <a name="icordebugbreakpointisactive-method"></a>ICorDebugBreakpoint::IsActive (Método)
Obtiene un valor que indica si este `ICorDebugBreakpoint` está activo.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT IsActive (  
    [out] BOOL *pbActive  
);  
```  
  
## <a name="parameters"></a>Parámetros  
 `pbActive`  
 enuncia `true` si este punto de interrupción está activo; en caso `false`contrario,.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Vea [Requisitos de sistema](../../get-started/system-requirements.md).  
  
 **Encabezado:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **.NET Framework versiones:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
