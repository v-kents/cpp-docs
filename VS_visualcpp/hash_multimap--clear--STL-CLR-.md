---
title: "hash_multimap::clear (STL-CLR)"
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
H1: hash_multimap::clear (STL/CLR)
ms.assetid: 8ad99f08-93b3-42b7-be07-f9a8ec556554
caps.latest.revision: 12
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
# hash_multimap::clear (STL-CLR)
Removes all elements.  
  
## Syntax  
  
```  
void clear();  
```  
  
## Remarks  
 The member function effectively calls [hash_multimap::erase (STL/CLR)](../VS_visualcpp/hash_multimap--erase--STL-CLR-.md)`(` [hash_multimap::begin (STL/CLR)](../VS_visualcpp/hash_multimap--begin--STL-CLR-.md)`(),` [hash_multimap::end (STL/CLR)](../VS_visualcpp/hash_multimap--end--STL-CLR-.md)`())`. You use it to ensure that the controlled sequence is empty.  
  
## Example  
  
```  
// cliext_hash_multimap_clear.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
    c1.insert(Myhash_multimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(Myhash_multimap::make_value(L'a', 1));   
    c1.insert(Myhash_multimap::make_value(L'b', 2));   
  
// display contents " [a 1] [b 2]"   
    for each (Myhash_multimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **[a 1] [b 2] [c 3]**  
**size() = 0**  
 **[a 1] [b 2]**  
**size() = 0**   
## Requirements  
 **Header:** <cliext/hash_map>  
  
 **Namespace:** cliext  
  
## See Also  
 [hash_multimap (STL/CLR)](../VS_visualcpp/hash_multimap--STL-CLR-.md)   
 [hash_multimap::erase (STL/CLR)](../VS_visualcpp/hash_multimap--erase--STL-CLR-.md)