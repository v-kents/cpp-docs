---
title: "Using C or C++ Symbols in __asm Blocks"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "__asm keyword [C++], syntax"
  - "symbols, in __asm blocks"
  - "Visual C, symbols in __asm blocks"
  - "__asm keyword [C++], C/C++ elements in"
  - "Visual C++, in __asm blocks"
ms.assetid: 0758ffdc-dfe9-41c8-a5e1-fd395bcac328
caps.latest.revision: 8
ms.author: "corob"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Using C or C++ Symbols in __asm Blocks
## Microsoft Specific  
 An `__asm` block can refer to any C or C++ symbol in scope where the block appears. (C and C++ symbols are variable names, function names, and labels; that is, names that aren't symbolic constants or `enum` members. You cannot call C++ member functions.)  
  
 A few restrictions apply to the use of C and C++ symbols:  
  
-   Each assembly-language statement can contain only one C or C++ symbol. Multiple symbols can appear in the same assembly instruction only with **LENGTH**, **TYPE**, and **SIZE** expressions.  
  
-   Functions referenced in an `__asm` block must be declared (prototyped) earlier in the program. Otherwise, the compiler cannot distinguish between function names and labels in the `__asm` block.  
  
-   An `__asm` block cannot use any C or C++ symbols with the same spelling as MASM reserved words (regardless of case). MASM reserved words include instruction names such as **PUSH** and register names such as SI.  
  
-   Structure and union tags are not recognized in `__asm` blocks.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Using C or C++ in __asm Blocks](../intrinsics/using-c-or-c---in-__asm-blocks.md)