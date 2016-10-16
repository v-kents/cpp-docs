---
title: "Manifest Resources"
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
ms.topic: article
ms.assetid: 8615334c-22a0-44c0-93e0-5924528c9917
caps.latest.revision: 10
manager: ghogen
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Manifest Resources
Manifest resources are XML files that describe the dependencies that an application uses. For example, in Visual Studio, the MFC wizard-generated manifest file defines which of the Windows common control DLLs the application should use, version 5.0 or 6.0:  
  
```  
<description>Your app description here</description>   
<dependency>   
    <dependentAssembly>   
        <assemblyIdentity   
            type="win32"   
            name="Microsoft.Windows.Common-Controls"   
            version="6.0.0.0"   
            processorArchitecture="X86"   
            publicKeyToken="6595b64144ccf1df"   
            language="*"   
        />   
    </dependentAssembly>   
</dependency>   
```  
  
 For a Windows XP or Windows Vista application, the manifest resource not only specifies that the application use the most current version of the Windows common controls (v6.0, as seen above) but it also supports the [Syslink control](http://msdn.microsoft.com/library/windows/desktop/bb760706).  
  
 To view the version and type information contained in a manifest resource, you can open the file in an XML viewer or in the Visual Studio [Text Editor](assetId:///508e1f18-99d5-48ad-b5ad-d011b21c6ab1). For more information, see [Opening a manifest resource in the Visual Studio Text Editor](../VS_visualcpp/How-to--Open-a-Manifest-Resource.md).  
  
 For information on adding resources to managed projects, please see [Resources in Applications](../Topic/Resources%20in%20Desktop%20Apps.md) in the *.NET Framework Developer's Guide.* For information on manually adding resource files to managed projects, accessing resources, displaying static resources, and assigning resources strings to properties, see  [Walkthrough: Using Resources for Localization with ASP.NET](../Topic/Walkthrough:%20Using%20Resources%20for%20Localization%20with%20ASP.NET.md).  
  
## Limitations  
 You can only have one manifest resource per module.  
  
## Requirements  
 Win32  
  
## See Also  
 [Controls](../VS_visualcpp/Controls--MFC-.md)   
 [Working with Resource Files](../VS_visualcpp/Working-with-Resource-Files.md)