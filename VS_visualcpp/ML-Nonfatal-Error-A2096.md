---
title: "ML Nonfatal Error A2096"
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
ms.assetid: bab0b5ee-b39f-4e44-a41a-3f949fab4297
caps.latest.revision: 6
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
# ML Nonfatal Error A2096
**segment, group, or segment register expected**  
  
 A segment or group was expected but was not found.  
  
 One of the following occurred:  
  
-   The left operand specified with the segment override operator (**:**) was not a segment register (CS, DS, SS, ES, FS, or GS), group name, segment name, or segment expression.  
  
-   The [ASSUME](../VS_visualcpp/ASSUME.md) directive was given a segment register without a valid segment address, segment register, group, or the special **FLAT** group.  
  
## See Also  
 [ML Error Messages](../VS_visualcpp/ML-Error-Messages.md)