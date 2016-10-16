---
title: "_heapchk"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _heapchk
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr100_clr0400.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr120_clr0400.dll
  - ucrtbase.dll
  - api-ms-win-crt-heap-l1-1-0.dll
apitype: DLLExport
ms.assetid: 859619a5-1e35-4f02-9e09-11d9fa266ec0
caps.latest.revision: 11
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
# _heapchk
Runs consistency checks on the heap.  
  
## Syntax  
  
```  
int _heapchk( void );  
```  
  
## Return Value  
 `_heapchk` returns one of the following integer manifest constants defined in Malloc.h.  
  
 `_HEAPBADBEGIN`  
 Initial header information is bad or cannot be found.  
  
 `_HEAPBADNODE`  
 Bad node has been found or heap is damaged.  
  
 `_HEAPBADPTR`  
 Pointer into heap is not valid.  
  
 `_HEAPEMPTY`  
 Heap has not been initialized.  
  
 `_HEAPOK`  
 Heap appears to be consistent.  
  
 In addition, if an error occurs, `_heapchk` sets `errno` to `ENOSYS`.  
  
## Remarks  
 The `_heapchk` function helps debug heap-related problems by checking for minimal consistency of the heap. If the operating system does not support `_heapchk`(for example, Windows 98), the function returns `_HEAPOK` and sets `errno` to `ENOSYS`.  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_heapchk`|<malloc.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../VS_visualcpp/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_heapchk.c  
// This program checks the heap for  
// consistency and prints an appropriate message.  
  
#include <malloc.h>  
#include <stdio.h>  
  
int main( void )  
{  
   int  heapstatus;  
   char *buffer;  
  
   // Allocate and deallocate some memory  
   if( (buffer = (char *)malloc( 100 )) != NULL )  
      free( buffer );  
  
   // Check heap status  
   heapstatus = _heapchk();  
   switch( heapstatus )  
   {  
   case _HEAPOK:  
      printf(" OK - heap is fine\n" );  
      break;  
   case _HEAPEMPTY:  
      printf(" OK - heap is empty\n" );  
      break;  
   case _HEAPBADBEGIN:  
      printf( "ERROR - bad start of heap\n" );  
      break;  
   case _HEAPBADNODE:  
      printf( "ERROR - bad node in heap\n" );  
      break;  
   }  
}  
```  
  
  **OK - heap is fine**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## See Also  
 [Memory Allocation](../VS_visualcpp/Memory-Allocation.md)   
 [_heapadd](../VS_visualcpp/_heapadd.md)   
 [_heapmin](../VS_visualcpp/_heapmin.md)   
 [_heapset](../VS_visualcpp/_heapset.md)   
 [_heapwalk](../VS_visualcpp/_heapwalk.md)