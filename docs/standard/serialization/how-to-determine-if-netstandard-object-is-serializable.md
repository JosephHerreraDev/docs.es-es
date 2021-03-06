---
title: Procedimiento para determinar si un objeto de .NET Standard es serializable
description: Se explica cómo determinar si un tipo de .NET Standard se puede serializar en tiempo de ejecución.
ms.date: 10/20/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- serializing objects
- objects, serializing steps
ms.openlocfilehash: b6791ae0666aeb0ac02d8a38ca419d7de2b263cf
ms.sourcegitcommit: b16c00371ea06398859ecd157defc81301c9070f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2020
ms.locfileid: "84289608"
---
# <a name="how-to-determine-if-a-net-standard-object-is-serializable"></a>Procedimiento para determinar si un objeto de .NET Standard es serializable

.NET Standard es una especificación que define los tipos y miembros que debe haber en las implementaciones de .NET específicas que se ajusten a esa versión del estándar. Pero .NET Standard no define si un tipo es serializable. Los tipos definidos en la biblioteca de .NET Standard no están marcados con el atributo <xref:System.SerializableAttribute>. En su lugar, son las implementaciones de .NET específicas, como .NET Framework y .NET Core, las que deciden libremente si un tipo determinado es serializable.

Si ha desarrollado una biblioteca que tiene como destino .NET Standard, cualquier implementación de .NET que admita .NET Standard podrá usar esa biblioteca. Esto significa que no se puede saber con antelación si un tipo determinado es serializable; solo se sabrá en tiempo de ejecución.

Para determinar si un objeto es serializable en tiempo de ejecución, hay que recuperar el valor de la propiedad <xref:System.Type.IsSerializable> de un objeto <xref:System.Type> que representa el tipo de ese objeto. En el siguiente ejemplo se proporciona una implementación. En él se define un método de extensión `IsSerializable(Object)` que indica si cualquier instancia de <xref:System.Object> se puede serializar.

[!code-csharp[is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/csharp/program.cs#2)]
[!code-vb[is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/vb/library.vb#2)]

Después, se puede pasar cualquier objeto al método para determinar si se puede serializar y deserializar en la implementación actual de .NET, como se muestra en el ejemplo siguiente:

[!code-csharp[test-is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/csharp/program.cs#1)]
[!code-vb[test-is-a-type-serializable](~/samples/snippets/standard/serialization/is-serializable/vb/program.vb#1)]

## <a name="see-also"></a>Vea también

- [Serialización binaria](binary-serialization.md)
- <xref:System.SerializableAttribute?displayProperty=nameWithType>
- <xref:System.Type.IsSerializable?displayProperty=nameWithType>
