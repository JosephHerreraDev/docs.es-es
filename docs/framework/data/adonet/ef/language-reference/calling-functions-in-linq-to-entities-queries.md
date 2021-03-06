---
title: Llamar a funciones en consultas de LINQ to Entities
description: Use estos artículos para ver cómo las clases EntityFunctions y SqlFunctions proporcionan acceso a las funciones canónicas y de base de datos como parte de la Entity Framework.
ms.date: 03/30/2017
ms.assetid: 12a525a9-727c-4464-a0c7-71a0ef541792
ms.openlocfilehash: faa6406713592f10e5e7371cd73f29bec4b03b7b
ms.sourcegitcommit: 33deec3e814238fb18a49b2a7e89278e27888291
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "84286862"
---
# <a name="calling-functions-in-linq-to-entities-queries"></a>Llamar a funciones en consultas de LINQ to Entities
Los temas de esta sección describen cómo realizar llamadas a funciones en consultas de LINQ to Entities.  
  
 Las clases <xref:System.Data.Objects.EntityFunctions> y <xref:System.Data.Objects.SqlClient.SqlFunctions> proporcionan acceso a funciones canónicas y de base de datos como parte de Entity Framework. Para obtener más información, vea [Cómo: llamar a funciones canónicas](how-to-call-canonical-functions.md) y [Cómo: llamar a funciones de base de datos](how-to-call-database-functions.md).  
  
 El proceso para llamar a una función personalizada requiere tres pasos básicos:  
  
1. Defina una función en su modelo conceptual o declare una función en su modelo de almacenamiento.  
  
2. Agregue un método a su aplicación y asígnelo a la función del modelo con un <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute>.  
  
3. Llame a la función en una consulta LINQ to Entities.  
  
 Para obtener más información, vea los temas de esta sección.  
  
## <a name="in-this-section"></a>En esta sección  
 [Procedimiento para llamar a funciones canónicas](how-to-call-canonical-functions.md)  
  
 [Procedimiento para llamar a funciones de base de datos](how-to-call-database-functions.md)  
  
 [Procedimiento para llamar a funciones de base de datos personalizadas](how-to-call-custom-database-functions.md)  
  
 [Procedimiento para llamar a funciones definidas por el modelo en consultas](how-to-call-model-defined-functions-in-queries.md)  
  
 [Procedimiento para llamar a funciones definidas por el modelo como métodos de objeto](how-to-call-model-defined-functions-as-object-methods.md)  
  
## <a name="see-also"></a>Consulte también

- [Consultas en LINQ to Entities](queries-in-linq-to-entities.md)
- [Funciones canónicas](canonical-functions.md)
- [.edmx, Información general sobre el archivo](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100))
- [Cómo: Definir funciones personalizadas en el modelo conceptual](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456812(v=vs.100))
