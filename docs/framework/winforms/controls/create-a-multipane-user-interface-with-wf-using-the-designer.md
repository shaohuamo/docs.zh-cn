---
title: 如何：通过使用设计器使用 Windows 窗体创建多窗格用户界面
ms.date: 03/30/2017
helpviewer_keywords:
- user interface [Windows Forms], multipane
- SplitContainer control [Windows Forms], using the designer
- multipane user interface
ms.assetid: c3f9294d-a26c-4198-9242-f237f55f7573
ms.openlocfilehash: 97888a77dfc731be591d5f0284e87f45ef7dc437
ms.sourcegitcommit: 68653db98c5ea7744fd438710248935f70020dfb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2019
ms.locfileid: "69930168"
---
# <a name="how-to-create-a-multipane-user-interface-with-windows-forms-using-the-designer"></a>如何：通过使用设计器使用 Windows 窗体创建多窗格用户界面
在下面的过程中, 你将创建一个多窗格用户界面, 该用户界面类似于在 Microsoft Outlook 中使用的用户界面, 其中包含**文件夹**列表、**邮件**窗格和**预览**窗格。 这种方式是通过窗体的停靠控件主要实现的。

 停靠控件时, 可以确定控件所固定到的父容器的边缘。 因此, 如果将<xref:System.Windows.Forms.SplitContainer.Dock%2A>属性设置为<xref:System.Windows.Forms.DockStyle.Right>, 则控件的右边缘将停靠在其父控件的右边缘。 此外, 控件的停靠边缘的大小会调整, 以匹配其容器控件的边缘。 有关此属性的<xref:System.Windows.Forms.SplitContainer.Dock%2A>工作原理的详细信息, 请参阅[如何:将控件停靠在](how-to-dock-controls-on-windows-forms.md)Windows 窗体上。

 此过程侧重于对窗<xref:System.Windows.Forms.SplitContainer>体上的和其他控件进行排列, 而不是添加功能以使应用程序模拟 Microsoft Outlook。

 若要创建此用户界面, 请将所有控件放在<xref:System.Windows.Forms.SplitContainer>控件内, 其中包含<xref:System.Windows.Forms.TreeView>左侧面板中的控件。 <xref:System.Windows.Forms.SplitContainer>控件的右侧面板包含一个控件上<xref:System.Windows.Forms.RichTextBox>有<xref:System.Windows.Forms.ListView>控件的<xref:System.Windows.Forms.SplitContainer>另一个控件。 这些<xref:System.Windows.Forms.SplitContainer>控件允许独立调整窗体上的其他控件的大小。 您可以调整此过程中的技术, 以创建自己的自定义用户界面。

## <a name="to-create-an-outlook-style-user-interface-at-design-time"></a>在设计时创建 Outlook 样式的用户界面

1. 创建新的 Windows 应用程序项目 **(文件** > **新** > **项目** > **视觉C#对象**或**Visual Basic** > **经典桌面** >  **Windows 窗体应用程序**)。

2. 将控件从工具箱拖到窗体上。 <xref:System.Windows.Forms.SplitContainer> 在“属性” 窗口中，将 <xref:System.Windows.Forms.SplitContainer.Dock%2A> 属性设置为 <xref:System.Windows.Forms.DockStyle.Fill>。

3. 将控件从 "**工具箱**" 拖动到<xref:System.Windows.Forms.SplitContainer>控件的左侧面板。 <xref:System.Windows.Forms.TreeView> 在 "**属性**" 窗口中, <xref:System.Windows.Forms.SplitContainer.Dock%2A>通过单击<xref:System.Windows.Forms.DockStyle.Left>在单击向下箭头时显示的值编辑器中的左侧面板, 将属性设置为。

4. 从工具箱<xref:System.Windows.Forms.SplitContainer>中拖动另一个控件, 将其放在添加到窗体的<xref:System.Windows.Forms.SplitContainer>控件的右窗格中。 在 "**属性**" 窗口中, <xref:System.Windows.Forms.SplitContainer.Dock%2A>将<xref:System.Windows.Forms.SplitContainer.Orientation%2A>属性<xref:System.Windows.Forms.DockStyle.Fill>设置为, 并<xref:System.Windows.Forms.Orientation.Horizontal>将属性设置为。

5. 将控件从工具箱拖动到添加到窗体的第二<xref:System.Windows.Forms.SplitContainer>个控件的上方面板。 <xref:System.Windows.Forms.ListView> 将 <xref:System.Windows.Forms.SplitContainer.Dock%2A> 控件的 <xref:System.Windows.Forms.ListView> 属性设置为 <xref:System.Windows.Forms.DockStyle.Fill>。

6. 将控件从**工具箱**拖到第二个<xref:System.Windows.Forms.SplitContainer>控件的下面板。 <xref:System.Windows.Forms.RichTextBox> 将 <xref:System.Windows.Forms.SplitContainer.Dock%2A> 控件的 <xref:System.Windows.Forms.RichTextBox> 属性设置为 <xref:System.Windows.Forms.DockStyle.Fill>。

     此时, 如果按 F5 运行应用程序, 窗体将显示由三个部分组成的用户界面, 类似于 Microsoft Outlook。

    > [!NOTE]
    > 当将鼠标指针放在<xref:System.Windows.Forms.SplitContainer>控件内的任一拆分器上方时, 可以调整内部尺寸的大小。

在应用程序开发中的这一点, 您已经创建了一个复杂的用户界面。 下一步是通过将<xref:System.Windows.Forms.TreeView>控件和<xref:System.Windows.Forms.ListView>控件连接到某种类型的数据源, 继续对应用程序本身进行编程。 有关将控件连接到数据的详细信息, 请参阅[数据绑定和 Windows 窗体](../data-binding-and-windows-forms.md)。

## <a name="see-also"></a>请参阅

- <xref:System.Windows.Forms.SplitContainer>
- [SplitContainer 控件](splitcontainer-control-windows-forms.md)
