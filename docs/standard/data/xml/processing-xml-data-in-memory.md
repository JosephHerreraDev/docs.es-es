---
title: Procesamiento de datos XML en memoria
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 1bbb4d05-ead7-4bda-8ece-f86d35c57ad4
ms.openlocfilehash: 06863d162a9f9fbf67f41cb12ea4fbb1935b424d
ms.sourcegitcommit: 33deec3e814238fb18a49b2a7e89278e27888291
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "84291284"
---
# <a name="processing-xml-data-in-memory"></a>Procesamiento de datos XML en memoria
Microsoft .NET Framework incluye tres modelos para el procesamiento de datos XML: la clase <xref:System.Xml.XmlDocument>, la clase <xref:System.Xml.XPath.XPathDocument> y [LINQ to XML (C#)](../../../csharp/programming-guide/concepts/linq/linq-to-xml-overview.md) y [LINQ to XML (Visual Basic)](../../../visual-basic/programming-guide/concepts/linq/linq-to-xml.md).  
  
 La clase <xref:System.Xml.XmlDocument> implementa el nivel 1 principal del Modelo de objetos de documento (DOM) y las recomendaciones principales del nivel 2 del DOM del W3C. El DOM es una representación de árbol en memoria (caché) de un documento XML. Con <xref:System.Xml.XmlDocument> y  sus clases relacionadas, puede construir documentos XML, cargar datos y tener acceso a ellos, modificar datos y guardar cambios.  
  
 La clase <xref:System.Xml.XPath.XPathDocument> es un almacén de datos en memoria y de solo lectura que se basa en el modelo de datos XPath. La clase <xref:System.Xml.XPath.XPathNavigator> ofrece diversas opciones de edición y capacidades de navegación utilizando un modelo de cursor sobre documentos XML contenidos en la clase <xref:System.Xml.XPath.XPathDocument> de solo lectura, así como en la clase <xref:System.Xml.XmlDocument>.  
  
 [LINQ to XML](../../../csharp/programming-guide/concepts/linq/linq-to-xml-overview.md) es un modelo que incorpora .NET Framework versión 3.5 para el procesamiento de datos XML. Es un modelo en memoria que usa [Language Integrated Query (LINQ)](../../../csharp/programming-guide/concepts/linq/index.md). LINQ amplía la sintaxis del lenguaje C# y Visual Basic para proporcionar nuevas capacidades de consulta.  
  
## <a name="in-this-section"></a>En esta sección  
 [Procesamiento de datos XML con el modelo DOM](process-xml-data-using-the-dom-model.md)  
 Describe el uso de <xref:System.Xml.XmlDocument> y sus clases relacionadas para procesar datos XML.  
  
 [Procesamiento de datos XML con el modelo de datos XPath](process-xml-data-using-the-xpath-data-model.md)  
 Describe el uso de las clases <xref:System.Xml.XPath.XPathDocument>, <xref:System.Xml.XmlDocument> y <xref:System.Xml.XPath.XPathNavigator> para procesar datos XML.  
  
 [Procesamiento de datos XML utilizando LINQ to XML](process-xml-data-using-linq-to-xml.md)  
 Propociona una descripción general acerca de LINQ to XML, así como vínculos que hacen referencia a la documentación de LINQ to XML.  
  
## <a name="related-sections"></a>Secciones relacionadas  
 [Documentos y datos XML](index.md)
