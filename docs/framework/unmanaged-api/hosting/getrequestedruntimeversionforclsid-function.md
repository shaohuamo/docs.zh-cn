---
title: GetRequestedRuntimeVersionForCLSID 函数
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersionForCLSID
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersionForCLSID
helpviewer_keywords:
- GetRequestedRuntimeVersionForCLSID function [.NET Framework hosting]
ms.assetid: 5bb12f9a-0612-434b-b4ed-2db636a20bec
topic_type:
- apiref
ms.openlocfilehash: ce0c6307defd93dcf63ac4e9051fc798041475f3
ms.sourcegitcommit: 559fcfbe4871636494870a8b716bf7325df34ac5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73127056"
---
# <a name="getrequestedruntimeversionforclsid-function"></a>GetRequestedRuntimeVersionForCLSID 函数
获取具有指定 `CLSID`的类的相应公共语言运行时（CLR）版本信息。  
  
 此函数已在 .NET Framework 4 中弃用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetRequestedRuntimeVersionForCLSID (  
    [in]  REFCLSID   rclsid,   
    [out]  LPWSTR     pVersion,   
    [in]  DWORD      cchBuffer,   
    [out] DWORD*     dwLength,   
    [in]  CLSID_RESOLUTION_FLAGS dwResolutionFlags  
);  
```  
  
## <a name="parameters"></a>参数  
 `rclsid`  
 中 组件的 `CLSID`。  
  
 `pVersion`  
 弄 一个缓冲区，其中包含成功完成后的版本号字符串。  
  
 `cchBuffer`  
 中 `pVersion` 缓冲区的大小（宽字符）。  
  
 `dwLength`  
 弄返回的缓冲区的长度（以字节为单位）。  
  
 `dwResolutionFlags`  
 中 CLSID_RESOLUTION_FLAGS 值之一。 支持以下值：  
  
- CLSID_RESOLUTION_DEFAULT：（0x0）指定应使用默认的互操作行为。  
  
- CLSID_RESOLUTION_REGISTERED：（0x1）指定应搜索注册表并应用填充程序策略。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|描述|  
|-------------|-----------------|  
|S_OK|函数已成功返回。|  
|E_INVALIDARG|其中一个参数的类型或格式无效。|  
|ERROR_INSUFFICIENT_BUFFER|`pVersion` 缓冲区不够大，无法容纳整个版本字符串。|  
|REGDB_E_CLASSNOTREG|没有用指定 `CLSID`注册的类。|  
|E_POINTER|`dwLength` 为 null，或者 `cchBuffer` 足以容纳版本字符串，但 `pVersion` 为 null。|  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **.NET Framework 版本：** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [弃用的 CLR 承载函数](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
