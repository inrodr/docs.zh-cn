---
title: 用户定义的函数
ms.date: 03/30/2017
ms.assetid: 3304c9b2-5c7a-4a95-9d45-4f260dcb606e
ms.openlocfilehash: f1222d9332d365c9c3c6ca2aa28cbb48e92c04e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33363594"
---
# <a name="user-defined-functions"></a>用户定义的函数
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 在您的对象模型中使用方法来表示用户定义的函数。 您可以通过应用 <xref:System.Data.Linq.Mapping.FunctionAttribute> 属性和 <xref:System.Data.Linq.Mapping.ParameterAttribute> 属性（如果需要）将方法指定为函数。 有关详细信息，请参阅[LINQ to SQL 对象模型](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)。  
  
 为避免出现 <xref:System.InvalidOperationException>，[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中用户定义的函数必须采用以下形式之一：  
  
-   包装为具有正确映射属性的方法调用的函数。 有关详细信息，请参阅[基于属性的映射](../../../../../../docs/framework/data/adonet/sql/linq/attribute-based-mapping.md)。  
  
-   特定于 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 的静态 SQL 方法。  
  
-   [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] 方法支持的函数。  
  
 本节中的主题说明了在你自行编写代码的情况下，如何在你的应用程序中构建和调用这些方法。 使用 Visual Studio 的开发人员通常会使用[!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)]来映射用户定义的函数。  
  
## <a name="in-this-section"></a>本节内容  
 [如何：使用标量值用户定义的函数](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-scalar-valued-user-defined-functions.md)  
 介绍如何实现返回标量值的函数。  
  
 [如何：使用表值用户定义的函数](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-table-valued-user-defined-functions.md)  
 介绍如何实现返回表值的函数。  
  
 [如何：以内联方式调用用户定义的函数](../../../../../../docs/framework/data/adonet/sql/linq/how-to-call-user-defined-functions-inline.md)  
 介绍如何对函数进行内联调用，以及进行内联调用时在执行方面的差异。
