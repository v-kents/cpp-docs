---
title: "CWinFormsDialog Class"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: e3cec000-a578-448e-b06a-8af256312f61
caps.latest.revision: 22
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# CWinFormsDialog Class
A wrapper for an MFC dialog class that hosts a Windows Forms user control.  
  
## Syntax  
  
```  
template <typename TManagedControl>  
class CWinFormsDialog :   
    public CDialog  
```  
  
#### Parameters  
 `TManagedControl`  
 The .NET Framework user control to be displayed in the MFC application.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CWinFormsDialog::CWinFormsDialog](#cwinformsdialog__cwinformsdialog)|Constructs a `CWinFormsDialog` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CWinFormsDialog::GetControl](#cwinformsdialog__getcontrol)|Retrieves a reference to the Windows Forms user control.|  
|[CWinFormsDialog::GetControlHandle](#cwinformsdialog__getcontrolhandle)|Retrieves a window handle to the Windows Forms user control.|  
|[CWinFormsDialog::OnInitDialog](#cwinformsdialog__oninitdialog)|Initializes the MFC dialog box by creating and hosting a Windows Forms user control on it.|  
  
### Public Operators  
  
|Name||  
|----------|-|  
|[CWinFormsDialog::operator -&gt;](#cwinformsdialog__operator_-_gt_)|Replaces [CWinFormsDialog::GetControl](#cwinformsdialog__getcontrol) in expressions.|  
|[CWinFormsDialog::operator TManagedControl^](#cwinformsdialog__operator_tmanagedcontrol^)|Casts a type as a reference to a Windows Forms user control.|  
  
## Remarks  
 `CWinFormsDialog` is a wrapper for an MFC dialog class ( [CDialog](../VS_visualcpp/CDialog-Class.md)) that hosts a Windows Forms ( <xref:System.Windows.Forms.UserControl?qualifyHint=False>) user control. This allows the display of .NET Framework controls on a modal or modeless MFC dialog box.  
  
 For more information on using Windows Forms, see [Using a Windows Form User Control in MFC](../VS_visualcpp/Using-a-Windows-Form-User-Control-in-MFC.md) and [Hosting a Windows Form User Control as an MFC Dialog Box](../VS_visualcpp/Hosting-a-Windows-Form-User-Control-as-an-MFC-Dialog-Box.md).  
  
## Requirements  
 **Header:** afxwinforms.h  
  
##  <a name="cwinformsdialog__cwinformsdialog"></a>  CWinFormsDialog::CWinFormsDialog  
 Constructs a `CWinFormsDialog` object.  
  
```  
CWinFormsDialog(  
    UINT nIDTemplate = IDD );  
```  
  
### Parameters  
 `nIDTemplate`  
 Contains the ID of a dialog box template resource. Use the dialog editor to create the dialog template and store it in the application's resource script file. For more information on dialog templates, see [CDialog Class](../VS_visualcpp/CDialog-Class.md).  
  
##  <a name="cwinformsdialog__getcontrol"></a>  CWinFormsDialog::GetControl  
 Retrieves a reference to the Windows Forms user control.  
  
```  
inline TManagedControl^ GetControl() const;  
```  
  
### Return Value  
 Returns a reference to the <xref:System.Windows.Forms.UserControl?qualifyHint=False> control in the MFC dialog box.  
  
##  <a name="cwinformsdialog__getcontrolhandle"></a>  CWinFormsDialog::GetControlHandle  
 Retrieves a window handle to the Windows Forms user control.  
  
```  
inline HWND GetControlHandle() const throw();  
```  
  
### Return Value  
 Returns a window handle to the Windows Forms user control.  
  
##  <a name="cwinformsdialog__oninitdialog"></a>  CWinFormsDialog::OnInitDialog  
 Initializes the MFC dialog box by creating and hosting a Windows Forms user control on it.  
  
```  
virtual BOOL OnInitDialog();  
```  
  
### Return Value  
 A boolean value that specifies whether the application has set the input focus to one of the controls in the dialog box. If `OnInitDialog` returns nonzero, Windows sets the input focus to the first control in the dialog box. This method can return 0 only if the application has explicitly set the input focus to one of the controls in the dialog box.  
  
### Remarks  
 When the MFC dialog box is created (using the [Create](../VS_visualcpp/CDialog-Class.md#cdialog__create), [CreateIndirect](../VS_visualcpp/CDialog-Class.md#cdialog__createindirect), or [DoModal](../VS_visualcpp/CDialog-Class.md#cdialog__domodal) method inherited from [CDialog](../VS_visualcpp/CDialog-Class.md)), a `WM_INITDIALOG` message is sent and this method is called. It creates an instance of a <xref:System.Windows.Forms.UserControl?qualifyHint=False> control on the dialog box and adjusts the size of the dialog box to accommodate for the size of the user control. Then it hosts the new control in the MFC dialog box.  
  
 Override this member function if you need to perform special processing when the dialog box is initialized. For more information on using this method, see [CDialog::OnInitDialog](../VS_visualcpp/CDialog-Class.md#cdialog__oninitdialog).  
  
##  <a name="cwinformsdialog__operator_-_gt_"></a>  CWinFormsDialog::operator -&gt;  
 Replaces [CWinFormsDialog::GetControl](#cwinformsdialog__getcontrol) in expressions.  
  
```  
inline TManagedControl^ operator->() const throw();  
```  
  
### Remarks  
 This operator provides a convenient syntax that replaces `GetControl` in expressions.  
  
 For information on using Windows Forms, see [Using a Windows Form User Control in MFC](../VS_visualcpp/Using-a-Windows-Form-User-Control-in-MFC.md).  
  
##  <a name="cwinformsdialog__operator_tmanagedcontrol_xor"></a>  CWinFormsDialog::operator TManagedControl^  
 Casts a type as a reference to a Windows Forms user control.  
  
```  
inline operator TManagedControl^() const throw();  
```  
  
### Remarks  
 This operator casts a type as a reference to a <xref:System.Windows.Forms.UserControl?qualifyHint=False> control. It is used to pass a `CWinFormsDialog<``TManagedControl``>` dialog box to functions that accept a pointer to a Windows Forms user control object.  
  
## See Also  
 <xref:System.Windows.Forms.UserControl?qualifyHint=True>   
 [CWnd Class](../VS_visualcpp/CWnd-Class.md)   
 [CWinFormsView Class](../VS_visualcpp/CWinFormsView-Class.md)   
 [CDialog Class](../VS_visualcpp/CDialog-Class.md)