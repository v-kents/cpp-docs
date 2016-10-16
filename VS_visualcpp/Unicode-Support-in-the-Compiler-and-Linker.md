---
title: "Unicode Support in the Compiler and Linker"
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
ms.assetid: acc1d322-56b9-4696-a30e-2af891a4e288
caps.latest.revision: 10
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
# Unicode Support in the Compiler and Linker
This topic describes Unicode support in the Visual C++ build tools.  
  
 Filenames  
 Filenames specified on the command line or in compiler directives (such as #include) may now contain Unicode characters.  
  
 Source code files  
 Unicode characters are now supported in identifiers, macros, string and character literals, and in comments.  Universal character names are also now supported.  
  
 Unicode can be input into a source code file in the following encodings:  
  
-   UTF-16 little endian with or without byte order mark (BOM)  
  
-   UTF-16 big endian with or without BOM  
  
-   UTF-8 with BOM  
  
 Output  
 During compilation, compiler outputs diagnostics to the console in UTF-16.  The characters that can be displayed at your console depend on the console window properties.  Compiler output redirected to a file is in the current ANSI console codepage.  
  
 Linker response files and .DEF files  
 Response files and DEF files can be either UTF-16 with a Byte Order Mark or ANSI.  Previously only ANSI was supported.  
  
 .asm and .cod dumps  
 .asm and .cod dumps are in ANSI by default for compatibility with MASM.  Use /FAu to output UTF-8.  Note that if you specify /FAs, the intermingled source will just be directly printed and may look garbled, for example if source code is UTF-8 and you didn't specify /FAsu.  
  
 You can enable Unicode file names in the development environment (see  [How to: Open Project Property Pages](../Topic/How%20to:%20Open%20Project%20Property%20Pages.md)) by selecting the appropriate tool and by selecting the **Enable Unicode Response Files** property, which is enabled by default. One reason you might change this default is if you modify your development environment to use a compiler that does not have Unicode support.  
  
## See Also  
 [Building on the Command Line](../VS_visualcpp/Building-on-the-Command-Line.md)