---
title: 表达式 - C# 编程指南
ms.custom: seodec18
ms.date: 05/11/2017
helpviewer_keywords:
- expressions [C#]
- C# language, expressions
ms.assetid: c7d8feb0-0e58-4f94-8bf6-4d070550a832
ms.openlocfilehash: e08220362c0acec6060ade75131e34a6b3fb7390
ms.sourcegitcommit: 14ad34f7c4564ee0f009acb8bfc0ea7af3bc9541
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "73417698"
---
# <a name="expressions-c-programming-guide"></a>表达式（C# 编程指南）

表达式是由一个或多个操作数以及零个或多个[运算符](../../language-reference/operators/index.md)组成的序列，其计算结果为一个值、对象、方法或命名空间  。 表达式可以包含文本值、方法调用、运算符及其操作数，或简单名称  。 简单名称可以是变量名、类型成员名、方法参数名、命名空间名或类型名。  
  
 表达式可以使用运算符（运算符又可使用其他表达式作为参数）或方法调用（方法调用的参数又可以是其他方法调用），因此表达式可以非常简单，也可以极其复杂。 下面是表达式的两个示例：  
  
```csharp  
((x < 10) && ( x > 5)) || ((x > 20) && (x < 25));

System.Convert.ToInt32("35");  
```  
  
## <a name="expression-values"></a>表达式值

 在大部分使用表达式的上下文中（例如在语句或方法参数中），表达式的计算结果应为某个值。 如果 x 和 y 是整数，表达式 `x + y` 的计算结果为一个数值。 表达式 `new MyClass()` 的计算结果为对 `MyClass` 类的新实例的引用。 表达式 `myClass.ToString()` 的计算结果为一个字符串，因为字符串是该方法的返回类型。 然而，虽然命名空间名称归类为表达式，但它的计算结果不是一个值，因此绝不会作为任何表达式的最终结果。 命名空间名称不得传递给方法参数，不能用在新表达式中，也不能赋给变量。 命名空间名称只能用作较大表达式的子表达式。 同样如此的还有类型（与 <xref:System.Type?displayProperty=nameWithType> 对象不同）、方法组名称（与特定方法不同）以及事件 [add](../../language-reference/keywords/add.md) 和 [remove](../../language-reference/keywords/remove.md) 访问器。  
  
 每个值都有关联的类型。 例如，如果 x 和 y 都是 `int` 类型的变量，则表达式 `x + y` 的值也属于 `int` 类型。 如果将该值赋给不同类型的变量，或者如果 x 和 y 是不同的类型，则应用类型转换规则。 若要详细了解如何进行这种转换，请参阅[强制转换和类型转换](../types/casting-and-type-conversions.md)。  
  
## <a name="overflows"></a>溢出

 如果值大于值类型的最大值，数值表达式可能导致溢出。 有关详细信息，请参阅[内置数值转换](../../language-reference/builtin-types/numeric-conversions.md)一文的 [Checked 和 Unchecked](../../language-reference/keywords/checked-and-unchecked.md) 和[显式数值转换](../../language-reference/builtin-types/numeric-conversions.md#explicit-numeric-conversions)部分。
  
## <a name="operator-precedence-and-associativity"></a>运算符优先级和关联性

 计算表达式的方式取决于关联性和运算符优先级规则。 有关详细信息，请参阅[运算符](../../language-reference/operators/index.md)。  
  
 除赋值表达式和方法调用表达式之外，大部分表达式都必须嵌在语句中。 有关详细信息，请参阅[语句](./statements.md)。  
  
## <a name="literals-and-simple-names"></a>文本和简单名称

 最简单的两种表达式类型是文本和简单名称。 文本是没有名称的常数值。 例如，在以下代码示例中，`5` 和 `"Hello World"` 都是文本值：  
  
 [!code-csharp[csProgGuideStatements#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#2)]  
  
 有关文本的详细信息，请参阅[类型](/dotnet/csharp/language-reference/keywords)。  
  
 在前面的示例中，`i` 和 `s` 都是用于标识局部变量的简单名称。 在表达式中使用这些变量时，变量名称计算为当前在该变量的内存位置所存储的值。 下面的示例对此进行了演示：  
  
 [!code-csharp[csProgGuideStatements#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideStatements/CS/Statements.cs#3)]

## <a name="invocation-expressions"></a>调用表达式

 在下面的代码示例中，对 `DoWork` 的调用是一个调用表达式。  
  
```csharp
DoWork();  
```  
  
 方法调用需要方法的名称（如之前的示例中那样作为名称，或作为其他表达式的结果），后跟括号和任意方法参数。 有关详细信息，请参阅[方法](../classes-and-structs/methods.md)。 委托调用使用委托的名称和括号内的方法参数。 有关详细信息，请参阅[委托](../delegates/index.md)。 如果方法返回值，则方法调用和委托调用的计算结果为该方法的返回值。 返回 void 的方法不能替代表达式中的值。  

## <a name="query-expressions"></a>查询表达式

 针对常规表达式的规则同样适用于查询表达式。 有关详细信息，请参阅 [LINQ](../../linq/index.md)。  
  
## <a name="lambda-expressions"></a>Lambda 表达式

 Lambda 表达式表示没有名称但可以具有输入参数和多个语句的“内联方法”。 它们在 LINQ 中广泛用于向方法传递参数。 Lambda 表达式会编译为委托或表达式树，具体取决于使用它们的上下文。 有关详细信息，请参阅 [Lambda 表达式](lambda-expressions.md)。  
  
## <a name="expression-trees"></a>表达式树

使用表达式树可将表达式表示为数据结构。 表达式树由 LINQ 提供程序广泛使用，用来将查询表达式转换为在其他某些上下文（如 SQL 数据库）中有意义的代码。 有关详细信息，请参阅[表达式树 (C#)](../concepts/expression-trees/index.md)。
  
## <a name="expression-body-definitions"></a>表达式主体定义

C# 支持“Expression-Bodied 成员”  ，这允许为方法、构造函数、终结器、属性和索引器提供简洁的表达式主体定义。 有关详细信息，请参阅 [Expression-bodied members](expression-bodied-members.md)（Expression-bodied 成员）。

## <a name="remarks"></a>备注

 只要从表达式中识别到变量、对象属性或对象索引器访问，该项的值都会用作表达式的值。 只要表达式的最终计算结果是所需的类型，表达式就可以置于 C# 中任何需要值或对象的位置。  

## <a name="c-language-specification"></a>C# 语言规范

有关详细信息，请参阅 [C# 语言规范](~/_csharplang/spec/introduction.md)中的[表达式](~/_csharplang/spec/expressions.md)部分。

## <a name="see-also"></a>请参阅

- [C# 编程指南](../index.md)
- [运算符](../../language-reference/operators/index.md)
- [方法](../classes-and-structs/methods.md)
- [委托](../delegates/index.md)
- [类型](../types/index.md)
- [LINQ](../../linq/index.md)
