---
title: ICorDebugDataTarget (Interfaz)
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget
helpviewer_keywords:
- ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: df5f05be-bed7-4f3c-bc89-dbb435d79a0b
topic_type:
- apiref
ms.openlocfilehash: 54272dd18a12715bab58ec1b1a4c1dc00e4bf12b
ms.sourcegitcommit: fff146ba3fd1762c8c432d95c8b877825ae536fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/08/2020
ms.locfileid: "82976530"
---
# <a name="icordebugdatatarget-interface"></a>ICorDebugDataTarget (Interfaz)
Proporciona una interfaz de devolución de llamada que brinda acceso a un proceso de destino determinado.  
  
## <a name="methods"></a>Métodos  
  
|Método|Descripción|  
|------------|-----------------|  
|[Método GetPlatform](icordebugdatatarget-getplatform-method.md)|Proporciona información sobre la plataforma, incluida la arquitectura del procesador y el sistema operativo, en la que se ejecuta el proceso de destino.|  
|[Método ReadVirtual](icordebugdatatarget-readvirtual-method.md)|Obtiene un bloque de memoria contigua que comienza en la dirección especificada y lo devuelve en el búfer proporcionado.|  
|[GetThreadContext (Método)](icordebugdatatarget-getthreadcontext-method.md)|Solicita el contexto del subproceso actual para el subproceso especificado.|  
  
## <a name="remarks"></a>Observaciones  
 `ICorDebugDataTarget`y sus métodos tienen las siguientes características:  
  
- Los servicios de depuración llaman a métodos en esta interfaz para tener acceso a la memoria y a otros datos en el proceso de destino.  
  
- El cliente del depurador debe implementar esta interfaz según corresponda para el destino determinado (por ejemplo, un proceso activo o un volcado de memoria).  
  
- Los `ICorDebugDataTarget` métodos solo se pueden invocar desde los métodos implementados en `ICorDebug*` otras interfaces. Esto garantiza que el cliente del depurador tenga control sobre el subproceso en el que se invoca y cuándo.  
  
- La `ICorDebugDataTarget` implementación siempre debe devolver información actualizada sobre el destino.  
  
 El proceso de destino debe detenerse y no cambiarse de `ICorDebug*` ninguna manera mientras se `ICorDebugDataTarget` llama a las interfaces (y, por lo tanto, a los métodos). Si el destino es un proceso activo y su estado cambia, se debe llamar de nuevo al método [ICLRDebugging:: openvirtualprocess (](iclrdebugging-openvirtualprocess-method.md) para proporcionar una instancia de ICorDebugProcess de reemplazo.  
  
> [!NOTE]
> Esta interfaz no admite que se la llame de forma remota, ya sea entre procesos o entre equipos.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Vea [Requisitos de sistema](../../get-started/system-requirements.md).  
  
 **Encabezado:** CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **.NET Framework versiones:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Consulte también

- [Interfaces para depuración](debugging-interfaces.md)
- [Depuración](index.md)
