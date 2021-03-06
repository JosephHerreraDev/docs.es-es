---
title: Transferencia y serialización de datos
ms.date: 03/30/2017
helpviewer_keywords:
- data serialization [WCF]
- data transfer [WCF]
ms.assetid: 0f03c635-f3e7-4c5c-9463-3cb0135e221e
ms.openlocfilehash: b07937b0a94c24a934b17d6cf21b726ee0d4362e
ms.sourcegitcommit: cdb295dd1db589ce5169ac9ff096f01fd0c2da9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2020
ms.locfileid: "84593495"
---
# <a name="data-transfer-and-serialization"></a>Transferencia y serialización de datos
En un sistema conectado, los servicios y clientes dependen del intercambio de datos para realizar cualquier tarea. Como desarrollador de un servicio o cliente, también debe comprender cómo el Windows Communication Foundation (WCF) controla los datos y la serialización de datos con el fin de crear aplicaciones que sean eficientes y fáciles de mantener.  
  
## <a name="in-this-section"></a>En esta sección  
 [Especificación de transferencia de datos en contratos de servicio](specifying-data-transfer-in-service-contracts.md)  
 Describe los conceptos básicos de la transferencia de datos en los servicios.  
  
 [Utilización de contratos de datos](using-data-contracts.md)  
 Describe qué son los contratos de datos y cómo crearlos y utilizarlos.  
  
 [Serializador de contratos de datos](data-contract-serializer.md)  
 Describe cómo lograr la serialización de los datos con la clase <xref:System.Runtime.Serialization.DataContractSerializer> o cualquier extensión de la clase <xref:System.Runtime.Serialization.XmlObjectSerializer>.  
  
 [Utilización de la clase XmlSerializer](using-the-xmlserializer-class.md)  
 Describe cómo y por qué utilizar la clase <xref:System.Xml.Serialization.XmlSerializer>, una alternativa a la clase <xref:System.Runtime.Serialization.DataContractSerializer>.  
  
 [Usar contratos de mensaje](using-message-contracts.md)  
 Describe cómo permiten los contratos de mensajes un control estrecho sobre los mensajes SOAP.  
  
 [Uso de la clase de mensajes](using-the-message-class.md)  
 Describe cómo utilizar las características de la clase Message.  
  
 [Filtrado](filtering.md)  
 Describe el filtrado, que permite el preprocesado de un mensaje en función de varios criterios.  
  
 [Datos de gran tamaño y secuencias](large-data-and-streaming.md)  
 Describe cómo enviar un bloque grande de datos, como, por ejemplo, un archivo binario.  
  
 [Consideraciones de seguridad para datos](security-considerations-for-data.md)  
 Describe los elementos que se han de tener en cuenta a la hora de programar la transferencia y serialización de datos.  
  
 [Información general sobre la arquitectura de transferencia de datos](data-transfer-architectural-overview.md)  
 Describe una vista del diseño general de la transferencia de datos en WCF.  
  
## <a name="reference"></a>Referencia  
 <xref:System.ServiceModel>  
  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
  
 <xref:System.Xml.Serialization.XmlSerializer>  
  
 <xref:System.Runtime.Serialization>  
  
 <xref:System.Xml.Serialization>  
  
## <a name="related-sections"></a>Secciones relacionadas  
 [Extensión de codificadores y serializadores](../extending/extending-encoders-and-serializers.md)  
  
## <a name="see-also"></a>Vea también

- [Procedimientos recomendados: Versiones de contratos de datos](../best-practices-data-contract-versioning.md)
- [Control de versiones del servicio](../service-versioning.md)
