---
title: EnumImportTypes (Método)
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
ms.openlocfilehash: ca7c7570aff63aa328dddc0626648fa74397addc
ms.sourcegitcommit: 9a39f2a06f110c9c7ca54ba216900d038aa14ef3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "74448735"
---
# <a name="enumimporttypes-method"></a>EnumImportTypes (Método)

Enumera cada tipo de cada ámbito.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT EnumImportTypes(
    HALINKENUM   hEnum,
    DWORD        dwMax,
    mdTypeDef    aTypeDefs[],
    DWORD*       pdwCount
) PURE;
```

## <a name="parameters"></a>Parámetros

`hEnum`\
Identificador del enumerador.

`dwMax`\
Número máximo de tipos que se van a recuperar.

`aTypeDefs`\
Recibe tokens de tipo, no supera `dwMax`.

`pdwCount`\
Recibe el número real de tipo en `aTypeDefs`.

## <a name="return-value"></a>Valor devuelto

Devuelve S_OK si el método se ejecuta correctamente.

## <a name="requirements"></a>Requisitos

Requiere ALink. h

## <a name="see-also"></a>Vea también

- [IALink (interfaz)](ialink-interface.md)
- [IALink2 (interfaz)](ialink2-interface.md)
- [API de ALink](index.md)
