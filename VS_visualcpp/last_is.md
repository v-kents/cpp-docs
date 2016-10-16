---
title: "last_is"
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
ms.topic: language-reference
ms.assetid: 9e045ac0-fa38-4249-af55-67bde5d0a58c
caps.latest.revision: 9
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
# last_is
Specifies the index of the last array element to be transmitted.  
  
## Syntax  
  
```  
  
      [ last_is(  
   "expression"  
) ]  
```  
  
#### Parameters  
 *expression*  
 One or more C-language expressions. Empty argument slots are allowed.  
  
## Remarks  
 The **last_is** C++ attribute has the same functionality as the [last_is](http://msdn.microsoft.com/library/windows/desktop/aa367066) MIDL attribute.  
  
## Example  
 See [first_is](../VS_visualcpp/first_is.md) for an example of how to specify a section of an array.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Field in `struct` or **union**, interface parameter, interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../VS_visualcpp/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../VS_visualcpp/IDL-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../VS_visualcpp/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Parameter Attributes](../VS_visualcpp/Parameter-Attributes.md)   
 [first_is](../VS_visualcpp/first_is.md)   
 [max_is](../VS_visualcpp/max_is.md)   
 [length_is](../VS_visualcpp/length_is.md)   
 [size_is](../VS_visualcpp/size_is.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)