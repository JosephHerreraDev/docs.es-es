---
title: Las instrucciones "#Region" y "#End Region" no son válidas en los cuerpos de método y operaciones lambda de varias líneas
ms.date: 07/20/2015
f1_keywords:
- bc32025
- vbc32025
helpviewer_keywords:
- BC32025
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
ms.openlocfilehash: 5652139ab139ea93258eb116f97ba21b76986a24
ms.sourcegitcommit: f8c270376ed905f6a8896ce0fe25b4f4b38ff498
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "84400388"
---
# <a name="region-and-end-region-statements-are-not-valid-within-method-bodiesmultiline-lambdas"></a>Las instrucciones '#Region' y '#End Region' no son válidas en los cuerpos de método y operaciones lambda de varias líneas
El `#Region` bloque se debe declarar en el nivel de clase, módulo o espacio de nombres. Una región contraíble puede incluir uno o varios procedimientos, pero no puede comenzar ni finalizar dentro de un procedimiento.  
  
 **Identificador de error:** BC32025  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
1. Asegúrese de que el procedimiento anterior finaliza correctamente con una `End Function` `End Sub` instrucción o.  
  
2. Asegúrese de que `#Region` las `#End Region` directivas y están en el mismo bloque de código.  
  
## <a name="see-also"></a>Consulte también

- [#Region (Directiva)](../directives/region-directive.md)
