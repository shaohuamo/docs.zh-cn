---
title: 活动库
ms.date: 03/30/2017
ms.assetid: 5323e9d4-71d6-47eb-bfa6-31feac62044d
ms.openlocfilehash: 15260fc2ad96e1761a8a41ccc84b2c199e3d448a
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2019
ms.locfileid: "74283157"
---
# <a name="activity-library"></a>活动库
本部分包含演示 Windows Workflow Foundation （WF）中的高级自定义活动的示例。  
  
## <a name="in-this-section"></a>本节内容

 [SendMail 自定义活动](sendmail-custom-activity.md)  
 演示如何创建派生自 <xref:System.Activities.AsyncCodeActivity> 的自定义活动，以使用 SMTP 发送邮件供在工作流应用程序内使用。  
  
 [限制并行 ForEach](throttled-parallel-foreach.md)  
 演示 `ThrottleParallelForEach` 活动与 <xref:System.Activities.Statements.ParallelForEach%601> 活动的相似之处，二者的不同之处在于，前者允许设置一个并发因子来限制要同时执行的分支的数量。
  
 [数据库访问活动](database-access-activities.md)  
 演示如何创建活动，以允许访问数据库以检索或修改信息，并使用[ADO.NET](https://go.microsoft.com/fwlink/?LinkId=166081)来访问数据库。  
  
 [.NET Framework 4.5 中的外部化策略活动](externalized-policy-activity-in-net-framework-4-5.md)  
 演示 ExternalizedPolicy4 活动如何通过使用在 WF 3.5 中随附的规则引擎直接在 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] （WF 4.5）的 Windows Workflow Foundation 中的 .NET Framework 3.5 （WF 3.5） <xref:System.Workflow.Activities.Rules.RuleSet> 对象中执行现有 Windows Workflow Foundation。 
  
 [非泛型 ForEach](non-generic-foreach.md)  
 演示了如何创建非泛型版本的 <xref:System.Activities.Statements.ForEach%601> 活动。  
  
 [非泛型 ParallelForEach](non-generic-parallelforeach.md)  
 演示了如何创建非泛型版本的 <xref:System.Activities.Statements.ParallelForEach%601> 活动。  
  
 [获取 WorkflowInstanceId](get-workflowinstanceid.md)  
 演示如何使用自定义活动 `GetWorkflowInstanceId` 返回工作流实例 ID。
