---
title: 如何：获取或设置画布定位属性
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
ms.openlocfilehash: 294b49d427a67da849ce930cf29a48f1735bf135
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33551975"
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a>如何：获取或设置画布定位属性
此示例演示如何使用的定位方法<xref:System.Windows.Controls.Canvas>元素来定位子内容。 此示例使用中的内容<xref:System.Windows.Controls.ListBoxItem>来表示定位值，并将值的实例转换为<xref:System.Double>，这是用于定位一个必需的参数。 然后重新转换为字符串和文本的形式显示值<xref:System.Windows.Controls.TextBlock>元素中的使用<xref:System.Windows.Controls.Canvas.GetLeft%2A>方法。  
  
## <a name="example"></a>示例  
 下面的示例创建<xref:System.Windows.Controls.ListBox>具有十一个可选择的元素<xref:System.Windows.Controls.ListBoxItem>元素。 <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged>事件触发器`ChangeLeft`自定义方法，后者在后续代码阻塞定义。  
  
 每个<xref:System.Windows.Controls.ListBoxItem>表示<xref:System.Double>值，该值的自变量之一是，<xref:System.Windows.Controls.Canvas.SetLeft%2A>方法<xref:System.Windows.Controls.Canvas>接受。 若要使用<xref:System.Windows.Controls.ListBoxItem>来表示的实例<xref:System.Double>，您必须先将转换<xref:System.Windows.Controls.ListBoxItem>到正确的数据类型。  
  
 [!code-xaml[CanvasPositioningProperties#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 当用户更改<xref:System.Windows.Controls.ListBox>选择时，它调用`ChangeLeft`自定义的方法。 此方法将传递<xref:System.Windows.Controls.ListBoxItem>到<xref:System.Windows.LengthConverter>对象，后者将转换<xref:System.Windows.Controls.ContentControl.Content%2A>的<xref:System.Windows.Controls.ListBoxItem>到实例<xref:System.Double>(请注意，此值已转换为<xref:System.String>使用<xref:System.Windows.Controls.Control.ToString%2A>方法）。 然后，此值会传递回<xref:System.Windows.Controls.Canvas.SetLeft%2A>和<xref:System.Windows.Controls.Canvas.GetLeft%2A>方法<xref:System.Windows.Controls.Canvas>以便更改的位置`text1`对象。  
  
 [!code-csharp[CanvasPositioningProperties#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Controls.Canvas>  
 <xref:System.Windows.Controls.ListBoxItem>  
 <xref:System.Windows.LengthConverter>  
 [面板概述](../../../../docs/framework/wpf/controls/panels-overview.md)
