---
title: Llamar a métodos asincrónicos mediante IAsyncResult
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- ending asynchronous operations
- waiting for asynchronous operations
- asynchronous method calling
- calling asynchronous methods
- asynchronous programming, calling asynchronous methods
- IAsyncResult interface, calling asynchronous methods
- stopping asynchronous operations
ms.assetid: 07fba116-045b-473c-a0b7-acdbeb49861f
ms.openlocfilehash: 88ca1b5bfbb8bfbdfef01dea8af07c5d56784c5c
ms.sourcegitcommit: 33deec3e814238fb18a49b2a7e89278e27888291
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "84289920"
---
# <a name="calling-asynchronous-methods-using-iasyncresult"></a>Llamar a métodos asincrónicos mediante IAsyncResult
Los tipos de .NET Framework y las bibliotecas de clases de terceros pueden proporcionar métodos que permiten la continuidad de la ejecución de una aplicación mientras se realizan las operaciones asincrónicas en subprocesos distintos del subproceso de aplicación principal. En las secciones siguientes se describen y proporcionan ejemplos de código que muestran las diferentes formas en que se puede llamar a métodos asincrónicos que usan el modelo de diseño <xref:System.IAsyncResult>.  
  
- [Bloquear la ejecución de una aplicación al finalizar una operación asincrónica](blocking-application-execution-by-ending-an-async-operation.md)  
  
- [Bloquear la ejecución de una aplicación mediante AsyncWaitHandle](blocking-application-execution-using-an-asyncwaithandle.md)  
  
- [Sondear el estado de una operación asincrónica](polling-for-the-status-of-an-asynchronous-operation.md)  
  
- [Utilizar un delegado AsyncCallback para finalizar una operación asincrónica](using-an-asynccallback-delegate-to-end-an-asynchronous-operation.md)  
  
## <a name="see-also"></a>Vea también

- [Modelo asincrónico basado en eventos (EAP)](event-based-asynchronous-pattern-eap.md)
- [Event-based Asynchronous Pattern Overview](event-based-asynchronous-pattern-overview.md) (Información general sobre el modelo asincrónico basado en eventos)
