---
title: El tipo <typename> no es compatible con CLS
ms.date: 07/20/2015
f1_keywords:
- bc40041
- vbc40041
helpviewer_keywords:
- BC40041
ms.assetid: 634132c2-5646-44aa-98c6-f773e2e63882
ms.openlocfilehash: eacf5036ebc6fc31dfa0e8de39c4fb574c9072b3
ms.sourcegitcommit: f8c270376ed905f6a8896ce0fe25b4f4b38ff498
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "84386963"
---
# <a name="type-typename-is-not-cls-compliant"></a>El tipo \<typename> no es compatible con CLS
Una variable, una propiedad o un valor devuelto por una función se declara con un tipo de datos que no es conforme a CLS.  
  
 Para que una aplicación sea compatible con la [independencia del lenguaje y componentes independientes del lenguaje](../../../standard/language-independence-and-language-independent-components.md) (CLS), solo debe usar tipos conformes a CLS.  
  
 Los siguientes tipos de datos de Visual Basic no son conformes a CLS:  
  
- [Tipo de datos SByte](../data-types/sbyte-data-type.md)  
  
- [Tipo de datos UInteger](../data-types/uinteger-data-type.md)  
  
- [Tipo de datos ULong](../data-types/ulong-data-type.md)  
  
- [Tipo de datos UShort](../data-types/ushort-data-type.md)  
  
 **Identificador de error:** BC40041  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
- Si la aplicación debe ser conforme a CLS, cambie el tipo de datos de este elemento por el tipo conforme a CLS más próximo. Por ejemplo, en lugar de `UInteger` , quizá pueda usar `Integer` si no necesita que el intervalo de valores esté por encima de 2.147.483.647. Si necesita el intervalo extendido, puede reemplazar `UInteger` por `Long`.  
  
- Si la aplicación no necesita ser conforme a CLS, no es necesario cambiar nada. Sin embargo, debe tener en cuenta su incumplimiento.
