---
title: Inspección del árbol de actividades
ms.date: 03/30/2017
ms.assetid: 100d00e4-8c1d-4233-8fbb-dd443a01155d
ms.openlocfilehash: 692f36d993c3f9c27839122b388a24d0698a2b59
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/12/2020
ms.locfileid: "79183033"
---
# <a name="activity-tree-inspection"></a>Inspección del árbol de actividades
Los autores de la aplicación de flujo de trabajo usan la inspección del árbol de actividad para inspeccionar los flujos de trabajo hospedados por la aplicación. Al usar <xref:System.Activities.WorkflowInspectionServices>, se pueden buscar actividades secundarias concretas en flujos de trabajo, se pueden enumerar las actividades individuales y sus propiedades, y los metadatos en tiempo de ejecución de las actividades pueden estar almacenados en memoria caché en un momento concreto. En este tema se proporciona información general de <xref:System.Activities.WorkflowInspectionServices> y cómo usarlo para inspeccionar un árbol de actividad.  
  
## <a name="using-workflowinspectionservices"></a>Usar WorkflowInspectionServices  
 El método <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> se usa para enumerar todas las actividades en el árbol de actividad especificado. <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> devuelve un enumerable que toca todas las actividades dentro del árbol como elementos secundarios, controladores delegados, valores predeterminados, variables y expresiones de argumento. En el ejemplo siguiente, se crea una definición de flujo de trabajo mediante <xref:System.Activities.Statements.Sequence>, <xref:System.Activities.Statements.While>, <xref:System.Activities.Statements.ForEach%601>, <xref:System.Activities.Statements.WriteLine> y expresiones. Una vez creada la definición de flujo de trabajo, se invoca y, a continuación, se llama al método `InspectActivity`.  
  
 [!code-csharp[CFX_WorkflowApplicationExample#45](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_workflowapplicationexample/cs/program.cs#45)]  
  
 Se llama a <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> en la actividad raíz para enumerar las actividades y de nuevo de forma recursiva en cada actividad devuelta. En el siguiente ejemplo, el <xref:System.Activities.Activity.DisplayName%2A> de cada actividad y expresión en el árbol de actividad se escribe en la consola.  
  
 [!code-csharp[CFX_WorkflowApplicationExample#46](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_workflowapplicationexample/cs/program.cs#46)]  
  
 Este código de ejemplo proporciona el siguiente resultado:  
  
 **List Item 1**  
**Elemento**
de lista 2**Elemento de lista 3**
**Elemento de lista 4**
Elemento de**lista 5**
**Elementos agregados a la colección.** 
Cadena **de\<lista de<literal** **de secuencia**>>  
 **While**  
 **AddToCollection\<String>**  
 **>>de cadena\<ICollection<VariableValue**  
 **>\<de cadena de LambdaValue**  
 **<\<<cadena de lista de locationReferenceValue>>**  
 **>\<booleano de LambdaValue**  
 **<\<<cadena de lista de locationReferenceValue>>**  
 **ForEach\<String>**  
 **VariableValue<>>\<de cadena IEnumerable**  
 **WriteLine**  
 **ArgumentValue\<String>**  
 **Secuencia**  
 **WriteLine**  
 **Literal\<String>** Para recuperar una actividad específica en <xref:System.Activities.WorkflowInspectionServices.Resolve%2A> lugar de enumerar todas las actividades, se utiliza. <xref:System.Activities.WorkflowInspectionServices.Resolve%2A> y <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> realizan el almacenamiento en la memoria caché de los metadatos si no se ha llamado previamente a `WorkflowInspectionServices.CacheMetadata`. Si se ha llamado a <xref:System.Activities.WorkflowInspectionServices.CacheMetadata%2A>, <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> se basará en los metadatos existentes. Por consiguiente, si se han realizado cambios en el árbol desde la última llamada a <xref:System.Activities.WorkflowInspectionServices.CacheMetadata%2A>, los resultados de <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A> podrían ser inesperados. Si se han realizado cambios <xref:System.Activities.WorkflowInspectionServices.GetActivities%2A>en el flujo de trabajo <xref:System.Activities.Validation.ActivityValidationServices> <xref:System.Activities.Validation.ActivityValidationServices.Validate%2A> después de llamar a , los metadatos se pueden volver a almacenar en caché llamando al método. En la sección siguiente se trata el almacenamiento en la memoria caché de los metadatos.  
  
### <a name="caching-metadata"></a>Almacenar en memoria caché los metadatos  
 Almacenar en memoria caché los metadatos para una actividad compila y valida una descripción de los argumentos de la actividad, las variables, las actividades secundarias y los delegados de la actividad. De manera predeterminada, el tiempo de ejecución almacena los metadatos en la memoria caché cuando se prepara una actividad para que se ejecute. Si un autor de host de flujo de trabajo desea almacenar en memoria caché los metadatos para una actividad o árbol de actividad antes de esto como, por ejemplo, para calcular el costo inicial, se puede usar <xref:System.Activities.WorkflowInspectionServices.CacheMetadata%2A> para almacenar en memoria caché los metadatos en el momento deseado.
