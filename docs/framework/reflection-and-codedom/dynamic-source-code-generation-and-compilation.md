---
title: 动态源代码生成和编译
ms.date: 03/30/2017
helpviewer_keywords:
- Code Document Object Model
- System.CodeDom namespace
- language-independent source code modeling
- CodeDOM
- multiple languages supported by CodeDOM
- source code in multiple languages
- languages, multiple language support by CodeDOM
ms.assetid: d077a3e8-bd81-4bdf-b6a3-323857ea30fb
ms.openlocfilehash: a7e341bb5bfb5b4648a222409951275169a29b79
ms.sourcegitcommit: 559fcfbe4871636494870a8b716bf7325df34ac5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73130245"
---
# <a name="dynamic-source-code-generation-and-compilation"></a>动态源代码生成和编译
.NET Framework 包括一个名为代码文档对象模型 (CodeDOM) 的机制。通过该机制，发出源代码的程序开发者可基于一种表示要呈现的代码的单一模型，在运行时以多种编程语言生成源代码。  
  
 为表示源代码，CodeDOM 元素相互链接，构成一个名为 CodeDOM 图的数据结构。该数据结构对某些源代码的结构建模。  
  
 `System.CodeDom` 命名空间定义某些类型，这些类型可以表示源代码的逻辑结构，且不依赖特定编程语言。 `System.CodeDom.Compiler` 命名空间定义某些类型，用于从 CodeDOM 图中生成源代码，并管理使用支持语言的源代码的编译工作。 编译器供应商或开发人员可以扩展支持语言。  
  
 当程序需要为多种语言的程序模型或为某个不确定的目标语言生成源代码时，不依赖语言的源代码建模非常有用。 例如，某些设计器使用 CodeDOM 作为语言抽象接口生成使用正确编程语言的源代码，前提是 CodeDOM 支持该语言。  
  
 .NET Framework 包括适用于 <xref:Microsoft.CSharp.CSharpCodeProvider>、<xref:Microsoft.JScript.JScriptCodeProvider> 和 <xref:Microsoft.VisualBasic.VBCodeProvider> 的代码生成器和代码编译器。  
  
## <a name="in-this-section"></a>本节内容  
 [使用 CodeDOM](using-the-codedom.md)  
 介绍 CodeDOM 的常见用途，并演示如何使用 CodeDOM 构建一个简单的对象图。  
  
 [从 CodeDOM 图中生成源代码并编译程序](generating-and-compiling-source-code-from-a-codedom-graph.md)  
 介绍如何使用 `System.CodeDom.Compiler` 命名空间中定义的类，通过外部编译器生成源代码并编译生成的代码。  
  
 [如何：使用 CodeDOM 创建 XML 文档文件](how-to-create-an-xml-documentation-file-using-codedom.md)  
 介绍如何使用 CodeDOM 生成带有 XML 文档注释的代码，以及如何编译生成的代码以使其创建 XML 文档输出。  
  
 [如何：使用 CodeDOM 创建类](how-to-create-a-class-using-codedom.md)  
 介绍如何使用 CodeDOM 生成包含字段、属性、方法、构造函数和入口点的类。  
  
## <a name="reference"></a>参考  
 <xref:System.CodeDom>  
 定义采用面向公共语言运行时的编程语言表示代码元素的元素。  
  
 <xref:System.CodeDom.Compiler>  
 定义用于在运行时生成和编译代码的接口。  
  
## <a name="related-sections"></a>相关章节  
 [CodeDOM 快速参考](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/f1dfsbhc(v=vs.100))  
 为开发人员提供了一种方法，使其可以快速查找表示源代码元素的 CodeDOM 元素。
