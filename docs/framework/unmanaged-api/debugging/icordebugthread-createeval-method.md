---
title: ICorDebugThread::CreateEval (Método)
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateEval
helpviewer_keywords:
- CreateEval method [.NET Framework debugging]
- ICorDebugThread::CreateEval method [.NET Framework debugging]
ms.assetid: 36605067-33d3-4579-9c72-fb0e551ab0f1
topic_type:
- apiref
ms.openlocfilehash: f66ef88646c314502dcb610cec8ce822cab1fca2
ms.sourcegitcommit: d6bd7903d7d46698e9d89d3725f3bb4876891aa3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "83379280"
---
# <a name="icordebugthreadcreateeval-method"></a>ICorDebugThread::CreateEval (Método)
Crea un objeto ICorDebugEval que recopila y expone la funcionalidad de esta expresión ICorDebugThread.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
## <a name="parameters"></a>Parámetros  
 `ppEval`  
 enuncia Puntero a la dirección de un `ICorDebugEval` objeto que recopila y expone la funcionalidad de este subproceso.  
  
## <a name="remarks"></a>Observaciones  
 El objeto de evaluación hará que se inserte una nueva cadena en el subproceso antes de realizar su cálculo. Esto interrumpe el cálculo que se está llevando a cabo en el subproceso hasta que se completa la evaluación.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Vea [Requisitos de sistema](../../get-started/system-requirements.md).  
  
 **Encabezado:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **.NET Framework versiones:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
