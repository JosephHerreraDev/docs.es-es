---
ms.openlocfilehash: 49041ce906ab0bb8b9482b79c44302465c4ca788
ms.sourcegitcommit: 0926684d8d34f4c6b5acce58d2193db093cb9cf2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2020
ms.locfileid: "83702323"
---
### <a name="globalization-apis-use-icu-libraries-on-windows"></a>Las API de globalización usan bibliotecas de ICU en Windows

.NET 5.0 y versiones posteriores usan bibliotecas de [componentes internacionales para Unicode (ICU)](http://site.icu-project.org/home) para la funcionalidad de globalización cuando se ejecutan en la actualización de mayo de 2019 de Windows 10 o versiones posteriores.

#### <a name="change-description"></a>Descripción del cambio

Anteriormente, las bibliotecas de .NET usaban API de [compatibilidad con el idioma nacional (NLS)](/windows/win32/intl/national-language-support) para la funcionalidad de globalización. Por ejemplo, las funciones de NLS se usaban para obtener datos de referencia cultural, como modelos de formato de fecha y hora, comparar cadenas y aplicar mayúsculas y minúsculas en las cadenas en la referencia cultural adecuada.

A partir de .NET 5.0, si una aplicación se ejecuta en la actualización de mayo de 2019 de Windows 10 o posterior, las bibliotecas de .NET usan las API de globalización de [ICU](http://site.icu-project.org/home). Las versiones de la actualización de mayo de 2019 de Windows 10 o posteriores incluyen la biblioteca nativa de ICU. Si el tiempo de ejecución de .NET no puede cargar ICU, utilizará NLS en su lugar.

Este cambio se introdujo por dos motivos:

- Las aplicaciones tienen el mismo comportamiento de globalización en distintas plataformas, como Linux, macOS y Windows.
- Las aplicaciones pueden controlar el comportamiento de la globalización mediante el uso de bibliotecas ICU personalizadas.

#### <a name="version-introduced"></a>Versión introducida

.NET 5.0 (versión preliminar 4)

#### <a name="recommended-action"></a>Acción recomendada

No se requiere ninguna acción por parte del desarrollador. Sin embargo, si desea seguir usando las API de globalización de NLS, puede establecer un [modificador en tiempo de ejecución](../../../../docs/core/run-time-config/globalization.md#nls) para revertir a ese comportamiento.

#### <a name="category"></a>Categoría

Globalización

#### <a name="affected-apis"></a>API afectadas

- <xref:System.Span%601?displayProperty=fullName>
- <xref:System.String?displayProperty=fullName>
- La mayoría de tipos del espacio de nombres <xref:System.Globalization?displayProperty=fullName>

<!--

#### Affected APIs

- `T:System.Span%601`
- `T:System.String`
- `N:System.Globalization`

-->
