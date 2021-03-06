---
title: 调试结构
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged structures [.NET Framework], debugging
- debugging structures [.NET Framework]
- structures [.NET Framework debugging]
ms.assetid: 173ba2c2-ab34-49ae-b6a8-e5c49882bf05
ms.openlocfilehash: 05a321d5025f03d6a0378b462178bf06c0291f48
ms.sourcegitcommit: 559fcfbe4871636494870a8b716bf7325df34ac5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73123024"
---
# <a name="debugging-structures"></a>调试结构

本节描述调试 API 使用的非托管结构。

## <a name="in-this-section"></a>本节内容
 [CLRDATA_ADDRESS_RANGE 结构](../../../../docs/framework/unmanaged-api/debugging/clrdata-address-range-structure.md)定义地址范围。

 [CLRDATA_IL_ADDRESS_MAP 结构](../../../../docs/framework/unmanaged-api/debugging/clrdata-il-address-map-structure.md)定义用于寻址映射的 IL

 [CLR_DEBUGGING_VERSION 结构](../../../../docs/framework/unmanaged-api/debugging/clr-debugging-version-structure.md)出于调试目的定义公共语言运行时（CLR）的产品版本。

 [CodeChunkInfo 结构](../../../../docs/framework/unmanaged-api/debugging/codechunkinfo-structure.md)表示内存中的单个代码块。

 [COR_ACTIVE_FUNCTION](cor-active-function-structure.md)包含有关线程帧中当前处于活动状态的函数的信息。

 [COR_ARRAY_LAYOUT 结构](../../../../docs/framework/unmanaged-api/debugging/cor-array-layout-structure.md)提供有关内存中数组对象的布局的信息。

 [COR_DEBUG_IL_TO_NATIVE_MAP](cor-debug-il-to-native-map-structure.md)包含用于将 Microsoft 中间语言（MSIL）代码映射到本机代码的偏移量。

 [COR_DEBUG_STEP_RANGE](cor-debug-step-range-structure.md)包含一系列代码的偏移信息。

 [COR_FIELD 结构](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md)提供有关对象中的字段的信息。

 [COR_GC_REFERENCE 结构](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md)包含有关要进行垃圾回收的对象的信息。

 [COR_HEAPINFO 结构](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md)提供有关垃圾回收堆的常规信息，包括是否可枚举。

 [COR_HEAPOBJECT 结构](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)提供有关托管堆上的对象的信息。

 [COR_IL_MAP](cor-il-map-structure.md)指定函数的相对偏移量中的更改。

 [COR_SEGMENT 结构](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md)包含有关托管堆中的内存区域的信息。

 [COR_TYPEID 结构](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)包含一个类型标识符。

 [COR_TYPE_LAYOUT 结构](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md)提供有关内存中对象的布局的信息。

 [COR_VERSION](cor-version-structure.md)存储公共语言运行时的由四个部分组成的标准版本号。

 [CorDebugBlockingObject 结构](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md)定义一个对象，该对象阻止线程，以及线程被阻止的原因。

 [CorDebugEHClause 结构](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md)表示给定中间语言（IL）部分的异常处理（EH）子句。

 [CorDebugExceptionObjectStackFrame 结构](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md)表示异常对象中的堆栈帧信息。

 [CorDebugGuidToTypeMapping 结构](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md)将 Windows 运行时 GUID 映射到其对应的[ICorDebugType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-interface.md)对象。

 [DacpGetModuleAddress 结构](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md)定义模块地址请求的容器。

 [DacpMethodDescData 结构](../../../../docs/framework/unmanaged-api/debugging/dacpmethoddescdata-structure.md)定义方法的运行时信息的传输缓冲区。

 [DacpModuleData 结构](../../../../docs/framework/unmanaged-api/debugging/dacpmoduledata-structure.md)定义模块的运行时信息的传输缓冲区。

 [DacpReJitData 结构](../../../../docs/framework/unmanaged-api/debugging/dacprejitdata-structure.md)定义有关给定探查器检测到的方法的基本信息。

 [StackTrace_SimpleContext 结构](../../../../docs/framework/unmanaged-api/debugging/stacktrace-simplecontext-structure.md)提供一个可用于代替完整 `CONTEXT` 结构的简单上下文。

## <a name="related-sections"></a>相关章节

 [调试组件类](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)

 [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)

 [调试全局静态函数](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)

 [调试枚举](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)

 [调试](../../../../docs/framework/unmanaged-api/debugging/index.md)
