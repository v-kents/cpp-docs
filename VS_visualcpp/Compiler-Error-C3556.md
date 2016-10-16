---
title: "Compiler Error C3556"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b002dcc-494e-414f-9587-20c2a0a39333
caps.latest.revision: 6
manager: douge
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
# Compiler Error C3556
'expression': incorrect argument to 'decltype'  
  
 The compiler cannot deduce the type of the expression that is the argument to the `decltype(``expression``)` type specifier. In the following code example, the compiler cannot deduce the type of the `myFunction` argument because `myFunction` is overloaded.  
  
```  
void myFunction();  
void myFunction(int);  
decltype(myFunction); // C3556  
```