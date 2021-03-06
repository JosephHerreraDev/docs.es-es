---
title: Migración de una base de datos de SQL Server a Azure
description: Aprenda a migrar una base de datos de SQL Server de un entorno local a Azure.
ms.topic: how-to
ms.date: 05/27/2020
ms.openlocfilehash: ed5d6ef9395dca14d8e0ecba82d3fc18cb3d629a
ms.sourcegitcommit: a241301495a84cc8c64fe972330d16edd619868b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "84241453"
---
# <a name="migrate-a-sql-server-database-to-azure"></a>Migración de una base de datos de SQL Server a Azure

En este artículo, se proporciona un breve esquema de las dos opciones para migrar una base de datos de SQL Server a Azure. Azure tiene tres opciones principales para migrar una base de datos de SQL Server de producción. Este artículo se centra en las dos opciones siguientes:

1. [SQL Server en Máquinas virtuales de Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-iaas-overview): una instancia de SQL Server instalada y hospedada en una máquina Virtual Windows que se ejecuta en Azure, también conocida como Infraestructura como servicio (IaaS).
2. [Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-technical-overview): un servicio de base de datos de Azure SQL completamente administrado, también conocido como Plataforma como servicio (PaaS).

Ambos tiene ventajas y desventajas que debe evaluar antes de migrar. La tercera opción es [Instancias administradas de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance).

## <a name="get-started"></a>Primeros pasos

Las siguientes guías de migración será útiles, según qué servicio use:

* [Migración de una base de datos SQL Server a SQL Server en una VM de Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-migrate-sql)
* [Migración de una base de datos de SQL Server a Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-migrate-your-sql-server-database)

Además, los vínculos siguientes a contenido conceptual le ayudarán a comprender mejor las máquinas virtuales:

* [Alta disponibilidad y recuperación ante desastres para SQL Server en Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-high-availability-dr)
* [Prácticas recomendadas para mejorar el rendimiento para SQL Server en Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-performance)
* [Estrategias de desarrollo y patrones de aplicación de SQL Server en Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-app-patterns-dev-strategies)

Y los vínculos siguientes le ayudarán a comprender mejor Azure SQL Database:

* [Creación y administración de servidores y bases de datos de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-servers-databases)
* [Unidades de transacción de bases de datos (DTU) y unidades de transacción de bases de datos elásticas (eDTU)](https://docs.microsoft.com/azure/sql-database/sql-database-what-is-a-dtu)
* [Límites de recursos de Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-resource-limits)

## <a name="choosing-iaas-or-paas"></a>Elección de IaaS o PaaS

Al evaluar dónde quiere migrar la base de datos, decida qué es lo más adecuado: IaaS o PaaS.

**Elija SQL Server en máquinas virtuales de Azure si:**

* Desea migrar mediante “lift and shift” la base de datos y las aplicaciones ningún cambio, o muy pocos.
* Prefiere tener control total sobre el servidor de base de datos y la máquina virtual donde se ejecuta.
* Ya tiene licencias de SQL Server y Windows Server, y tiene previsto usarlas.

**Elija Azure SQL Database si:**

* Desea modernizar las aplicaciones y va a realizar la migración para usar otros servicios de PaaS en Azure.
* No desea administrar el servidor de base de datos y la máquina virtual donde se ejecuta.
* No tiene licencias de SQL Server o Windows Server, o tiene previsto dejar que las licencias que tiene expiren.

En la tabla siguiente se describen las diferencias entre cada servicio según los distintos escenarios.

| Escenario | SQL Server en máquinas virtuales de Azure | Azure SQL Database |
|----------|-------------------------|--------------------|
| Migración | Requiere cambios mínimos en la base de datos. | Puede requerir cambios en la base de datos si usa características no disponibles en Azure SQL, según determine el [Asistente para la migración de datos](https://www.microsoft.com/download/details.aspx?id=53595), o si tiene otras dependencias tales como archivos ejecutables instalados localmente.|
| Administración de la disponibilidad, la recuperación y las actualizaciones | La disponibilidad y la recuperación se configuran manualmente. Las actualizaciones se pueden automatizar con [VM Scale Sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-upgrade). | Se administra automáticamente. |
| Configuración del sistema operativo subyacente | Configuración manual. | Se administra automáticamente. |
| Administración del tamaño de base de datos | Admite hasta 256 TB de almacenamiento por cada instancia de SQL Server. | Admite 8 TB de almacenamiento antes de necesitar una partición horizontal. |
| Administración de los costos | Debe administrar los costos de las licencias de SQL Server, los costos de las licencias de Windows Server y los costos de las máquinas virtuales (en función del número de núcleos, la memoria RAM y el almacenamiento). | Debe administrar los costos del servicio (en función del número de [eDTU o DTU](https://docs.microsoft.com/azure/sql-database/sql-database-what-is-a-dtu), el almacenamiento y el número de bases de datos si usa un grupo elástico). También debe administrar el costo de los SLA. |

Para obtener más información sobre las diferencias entre ambas, consulte [Elegir la opción de implementación adecuada en Azure SQL](https://docs.microsoft.com/azure/sql-database/sql-database-paas-vs-sql-server-iaas).

## <a name="faq"></a>Preguntas más frecuentes

* **¿Puedo seguir usando herramientas como SQL Server Management Studio y SQL Server Reporting Services (SSRS) con SQL Server on Azure VMs o con Azure SQL Database?**

    Sí. Todas las herramientas de Microsoft SQL funcionan con ambos servicios. Sin embargo, SSRS no forma parte de Azure SQL Database. Se recomienda ejecutarlo en una máquina virtual de Azure y, a continuación, hacer que apunte a la instancia de base de datos.

* **Quiero cambiar a PaaS pero no estoy seguro de si mi base de datos es compatible. ¿Hay alguna herramienta que pueda ayudar?**

    Sí. El [Asistente para la migración de datos](https://www.microsoft.com/download/details.aspx?id=53595) es una herramienta que se usa como parte de la migración a Azure SQL Database. [Azure Database Migration Service](https://azure.microsoft.com/campaigns/database-migration/) es un servicio en versión preliminar que puede usar para IaaS o PaaS.

* **¿Puedo calcular los costos?**

    Sí. Puede usar la [Calculadora de precios de Azure](https://azure.microsoft.com/pricing/calculator/) para calcular los costos de todos los servicios de Azure, incluidos los servicios de máquinas virtuales y base de datos.

## <a name="next-steps"></a>Pasos siguientes

> [!div class="nextstepaction"]
> [Elección de la opción de hospedaje de Azure correcta](choose.md)
