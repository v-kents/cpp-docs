---
title: "Compiler Warning C4867"
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
ms.topic: error-reference
ms.assetid: 8a257d70-c3a7-462d-b285-e57c952a8bf7
caps.latest.revision: 16
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
# Compiler Warning C4867
'function': function call missing argument list; use 'call' to create a pointer to member  
  
 A pointer to member function was initialized incorrectly.  
  
 This warning can be generated as a result of compiler conformance work that was done for Visual C++ 2005: enhanced pointer-to-member conformance.  Code that compiled prior to Visual C++ 2005 will now generate C4867.  
  
 This warning is always issued as an error. Use the [warning](../VS_visualcpp/warning.md) pragma to disable this warning. For more information about C4867 and MFC/ATL, see [_ATL_ENABLE_PTM_WARNING](../Topic/_ATL_ENABLE_PTM_WARNING.md).  
  
## Example  
 The following sample generates C4867.  
  
```  
// C4867.cpp  
// compile with: /c  
class A {  
public:  
   void f(int) {}  
  
   typedef void (A::*TAmtd)(int);  
  
   struct B {  
      TAmtd p;  
   };  
  
   void g() {  
      B b = {f};   // C4867  
      B b2 = {&A::f};   // OK  
   }  
};  
```