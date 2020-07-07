---
title: DataGrid
ms.date: 03/30/2017
helpviewer_keywords:
- DataGrid column types [WPF]
- DataGrid scenarios [WPF]
- DataGrid control [WPF]
- controls [WPF], DataGrid
- DataGrid [WPF], common tasks for
- DataGrid [WPF], customizing the appearance of
- DataGrid columns [WPF], using
ms.assetid: bf89ea63-79b6-422b-bc9f-0485ad803216
ms.openlocfilehash: cdf4bfff8182b62d55f56b823c7ff129de4f9f1c
ms.sourcegitcommit: 62285ec11fa8e8424bab00511a90760c60e63c95
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/20/2020
ms.locfileid: "81646121"
---
# <a name="datagrid"></a>DataGrid
El control <xref:System.Windows.Controls.DataGrid> le permite mostrar y editar datos de muchos orígenes diferentes, como desde una base de datos SQL, una consulta LINQ o cualquier otro origen de datos enlazable. Para más información, consulte [Binding Sources Overview](../data/binding-sources-overview.md) (Introducción a los orígenes de enlace).  
  
 Las columnas pueden mostrar texto, controles, como un <xref:System.Windows.Controls.ComboBox> , o cualquier otro contenido de WPF, como imágenes, botones o cualquier contenido contenido en una plantilla. Puede utilizar <xref:System.Windows.Controls.DataGridTemplateColumn> para mostrar los datos definidos en una plantilla. En la tabla siguiente se enumeran los tipos de columna que se proporcionan de forma predeterminada.  
  
|Tipo de columna generado|Tipo de datos|  
|---------------------------|---------------|  
|<xref:System.Windows.Controls.DataGridTextColumn>|<xref:System.String>|  
|<xref:System.Windows.Controls.DataGridCheckBoxColumn>|<xref:System.Boolean>|  
|<xref:System.Windows.Controls.DataGridComboBoxColumn>|<xref:System.Enum>|  
|<xref:System.Windows.Controls.DataGridHyperlinkColumn>|<xref:System.Uri>|  
  
 <xref:System.Windows.Controls.DataGrid> se puede personalizar en apariencia, como fuente de celda, color y tamaño. <xref:System.Windows.Controls.DataGrid> admite todas las funciones de estilo y plantillas de otros controles WPF. <xref:System.Windows.Controls.DataGrid> también incluye comportamientos predeterminados y personalizables para editar, ordenar y validar.  
  
 En la tabla siguiente se enumeran algunas de las tareas comunes para el <xref:System.Windows.Controls.DataGrid> y cómo realizarlas. Al ver la API relacionada, puede encontrar más información y código de ejemplo.  
  
|Escenario|Enfoque|  
|--------------|--------------|  
|Colores de fondo alternativos|Establezca <xref:System.Windows.Controls.ItemsControl.AlternationIndex%2A> la propiedad en 2 o <xref:System.Windows.Media.Brush> más <xref:System.Windows.Controls.DataGrid.RowBackground%2A> y, a continuación, asigne una a las propiedades y. <xref:System.Windows.Controls.DataGrid.AlternatingRowBackground%2A>|  
|Definir el comportamiento de selección de celdas y filas|Establezca las propiedades <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> y <xref:System.Windows.Controls.DataGrid.SelectionUnit%2A>.|  
|Personalizar la apariencia visual de encabezados, celdas y filas|Aplique una <xref:System.Windows.Style> nueva <xref:System.Windows.Controls.DataGrid.ColumnHeaderStyle%2A> <xref:System.Windows.Controls.DataGrid.RowHeaderStyle%2A>a <xref:System.Windows.Controls.DataGrid.CellStyle%2A>las <xref:System.Windows.Controls.DataGrid.RowStyle%2A> propiedades , , , o .|  
|Establecer opciones de tamaño|Establezca <xref:System.Windows.FrameworkElement.Height%2A>las <xref:System.Windows.FrameworkElement.MaxHeight%2A> <xref:System.Windows.FrameworkElement.MinHeight%2A>propiedades <xref:System.Windows.FrameworkElement.Width%2A> <xref:System.Windows.FrameworkElement.MaxWidth%2A>, <xref:System.Windows.FrameworkElement.MinWidth%2A> , , , , o . Para obtener más información, vea [Opciones de tamaño en el control DataGrid](sizing-options-in-the-datagrid-control.md).|  
|Acceder a los elementos seleccionados|Compruebe <xref:System.Windows.Controls.DataGrid.SelectedCells%2A> la propiedad para obtener <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems%2A> las celdas seleccionadas y la propiedad para obtener las filas seleccionadas. Para obtener más información, vea <xref:System.Windows.Controls.DataGrid.SelectedCells%2A>.|  
|Personalizar las interacciones del usuario final|Establezca <xref:System.Windows.Controls.DataGrid.CanUserAddRows%2A>las <xref:System.Windows.Controls.DataGrid.CanUserDeleteRows%2A> <xref:System.Windows.Controls.DataGrid.CanUserReorderColumns%2A>propiedades <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A> <xref:System.Windows.Controls.DataGrid.CanUserResizeRows%2A>, <xref:System.Windows.Controls.DataGrid.CanUserSortColumns%2A> , , , , y .|  
|Cancelar o cambiar columnas generadas automáticamente|Controle <xref:System.Windows.Controls.DataGrid.AutoGeneratingColumn> el evento.|  
|Congelar una columna|Establezca <xref:System.Windows.Controls.DataGrid.FrozenColumnCount%2A> la propiedad en 1 y mueva la columna <xref:System.Windows.Controls.DataGridColumn.DisplayIndex%2A> a la posición más a la izquierda estableciendo la propiedad en 0.|  
|Utilice datos XML como origen de datos|Enlazar <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> el <xref:System.Windows.Controls.DataGrid> en la a la XPath consulta que representa la colección de elementos. Cree cada columna <xref:System.Windows.Controls.DataGrid>en el archivo . Enlazar cada columna estableciendo el XPath en el enlace a la consulta que obtiene la propiedad en el origen del elemento. Para obtener un ejemplo, consulte <xref:System.Windows.Controls.DataGridTextColumn>.|  
  
## <a name="related-topics"></a>Temas relacionados  
  
|Title|Descripción|  
|-----------|-----------------|  
|[Tutorial: Mostrar los datos de una base de datos de SQL Server en un control DataGrid](walkthrough-display-data-from-a-sql-server-database-in-a-datagrid-control.md)|Describe cómo configurar un nuevo proyecto WPFWPF, agregar un elemento de Entity Framework, establecer el origen y mostrar los datos en un <xref:System.Windows.Controls.DataGrid>archivo .|  
|[Procedimiento para agregar detalles de fila a un control DataGrid](how-to-add-row-details-to-a-datagrid-control.md)|Describe cómo crear detalles <xref:System.Windows.Controls.DataGrid>de fila para un archivo .|  
|[Procedimiento para implementar la validación con el control DataGrid](how-to-implement-validation-with-the-datagrid-control.md)|Describe cómo validar valores <xref:System.Windows.Controls.DataGrid> en celdas y filas y mostrar comentarios de validación.|  
|[Comportamiento predeterminado de teclado y mouse en el control DataGridView](default-keyboard-and-mouse-behavior-in-the-datagrid-control.md)|Describe cómo interactuar con <xref:System.Windows.Controls.DataGrid> el control mediante el teclado y el mouse.|  
|[Procedimiento para agrupar, ordenar y filtrar datos en el control DataGrid](how-to-group-sort-and-filter-data-in-the-datagrid-control.md)|Describe cómo ver los <xref:System.Windows.Controls.DataGrid> datos de diferentes maneras agrupando, ordenando y filtrando los datos.|  
|[Opciones de ajuste de tamaño en el control DataGrid](sizing-options-in-the-datagrid-control.md)|Describe cómo controlar el tamaño absoluto <xref:System.Windows.Controls.DataGrid>y automático en el archivo .|  
  
## <a name="see-also"></a>Consulte también

- <xref:System.Windows.Controls.DataGrid>
- [Aplicar estilos y plantillas](../../../desktop-wpf/fundamentals/styles-templates-overview.md)
- [Descripción general del enlace de datos](../../../desktop-wpf/data/data-binding-overview.md)
- [Información general sobre plantillas de datos](../data/data-templating-overview.md)
- [Controles](index.md)
- [Modelo de contenido de WPF](wpf-content-model.md)
