---
title: ICorDebugAssembly 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
ms.openlocfilehash: dea3231e3bbb361b56254756c6d99b115f73e792
ms.sourcegitcommit: 559fcfbe4871636494870a8b716bf7325df34ac5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73133972"
---
# <a name="icordebugassembly-interface"></a>ICorDebugAssembly 接口

表示一个程序集。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[EnumerateModules 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|获取包含在程序集中的模块的枚举器。|  
|[GetAppDomain 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|获取一个接口指针，该指针指向包含此 `ICorDebugAssembly` 实例的应用程序域。|  
|[GetCodeBase 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|未在 .NET Framework 的当前版本中实现。|  
|[GetName 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|获取程序集的名称。|  
|[GetProcess 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|获取在其中运行程序集的 ICorDebugProcess 实例。|  
  
## <a name="remarks"></a>备注  
  
> [!NOTE]
> 此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
