---
title: "set::erase (STL-CLR)"
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
H1: set::erase (STL/CLR)
ms.assetid: 0596514b-d4cd-4d2d-8223-3bee6980261c
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
# set::erase (STL-CLR)
Removes elements at specified positions.  
  
## Syntax  
  
```  
iterator erase(iterator where);  
iterator erase(iterator first, iterator last);  
size_type erase(key_type key)  
```  
  
#### Parameters  
 first  
 Beginning of range to erase.  
  
 key  
 Key value to erase.  
  
 last  
 End of range to erase.  
  
 where  
 Element to erase.  
  
## Remarks  
 The first member function removes the element of the controlled sequence pointed to by `where`, and returns an iterator that designates the first element remaining beyond the element removed, or [set::end (STL/CLR)](../VS_visualcpp/set--end--STL-CLR-.md)`()` if no such element exists. You use it to remove a single element.  
  
 The second member function removes the elements of the controlled sequence in the range `[``first``,` `last``)`, and returns an iterator that designates the first element remaining beyond any elements removed, or `end()` if no such element exists.. You use it to remove zero or more contiguous elements.  
  
 The third member function removes any element of the controlled sequence whose key has equivalent ordering to `key`, and returns a count of the number of elements removed. You use it to remove and count all elements that match a specified key.  
  
 Each element erasure takes time proportional to the logarithm of the number of elements in the controlled sequence.  
  
## Example  
  
```  
// cliext_set_erase.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::set<wchar_t> Myset;   
int main()   
    {   
    Myset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase an element and reinspect   
    System::Console::WriteLine("erase(begin()) = {0}",   
        *c1.erase(c1.begin()));   
  
// add elements and display " b c d e"   
    c1.insert(L'd');   
    c1.insert(L'e');   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// erase all but end   
    Myset::iterator it = c1.end();   
    System::Console::WriteLine("erase(begin(), end()-1) = {0}",   
        *c1.erase(c1.begin(), --it));   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
  **a b c**  
**erase(begin()) = b**  
 **b c d e**  
**erase(begin(), end()-1) = e**  
**size() = 1**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [set (STL/CLR)](../VS_visualcpp/set--STL-CLR-.md)   
 [set::clear (STL/CLR)](../VS_visualcpp/set--clear--STL-CLR-.md)