---
title: Procedimiento para dibujar una línea con extremos de línea
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], drawing
- pens [Windows Forms], drawing lines
- drawing lines [Windows Forms], line caps
ms.assetid: eb68c3e1-c400-4886-8a04-76978a429cb6
ms.openlocfilehash: 34abfc86e980a24ebb835cfd88d2522f8372c68d
ms.sourcegitcommit: b1cfd260928d464d91e20121f9bdba7611c94d71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67506024"
---
# <a name="how-to-draw-a-line-with-line-caps"></a>Procedimiento para dibujar una línea con extremos de línea
Puede dibujar el inicio o final de una línea en una de varias formas llamadas extremos de línea. GDI + admite varios extremos de línea, como round, cuadrado, rombo y punta de flecha.  
  
## <a name="example"></a>Ejemplo  
 Puede especificar extremos de línea para el inicio de una línea (extremo inicial), el final de una línea (extremo final) o los guiones de una línea discontinua (dash CAP.).  
  
 El ejemplo siguiente dibuja una línea con una punta de flecha en un extremo y un extremo redondeado en el otro extremo. La ilustración muestra la línea resultante:  
  
 ![Ilustración que muestra una línea con un extremo redondeado.](./media/how-to-draw-a-line-with-line-caps/line-cap-arrowhead-example.gif)  
  
 [!code-csharp[System.Drawing.UsingAPen#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.UsingAPen#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a>Compilar el código  
  
- Crear un formulario de Windows y controlar el formato <xref:System.Windows.Forms.Control.Paint> eventos. Pegue el código de ejemplo en el <xref:System.Windows.Forms.Control.Paint> controlador de eventos pasando `e` como <xref:System.Windows.Forms.PaintEventArgs>.  
  
## <a name="see-also"></a>Vea también

- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Drawing2D.LineCap?displayProperty=nameWithType>
- [Gráficos y dibujos en Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Utilizar lápiz para dibujar líneas y formas](using-a-pen-to-draw-lines-and-shapes.md)
