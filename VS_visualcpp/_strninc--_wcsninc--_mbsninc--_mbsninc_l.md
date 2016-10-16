---
title: "_strninc, _wcsninc, _mbsninc, _mbsninc_l"
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
  - _mbsninc
  - _mbsninc_l
  - _wcsninc
  - _strninc
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
  - api-ms-win-crt-multibyte-l1-1-0.dll
apitype: DLLExport
ms.assetid: 6caace64-f9e4-48c0-afa8-ea51824ad723
caps.latest.revision: 19
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
# _strninc, _wcsninc, _mbsninc, _mbsninc_l
Advances a string pointer by `n` characters.  
  
> [!IMPORTANT]
>  `_mbsninc` and `_mbsninc_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *_strninc(  
   const char *str,  
   size_t count   
);  
wchar_t *_wcsninc(  
   const wchar_t *str,  
   size_t count   
);  
unsigned char *_mbsninc(  
   const unsigned char *str,  
   size_t count   
);  
unsigned char *_mbsninc(  
   const unsigned char *str,  
   size_t count,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 Source string.  
  
 `count`  
 Number of characters to increment a string pointer.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these routines returns a pointer to `str` after `str` has been incremented by `count` characters or `NULL` if the supplied pointer is `NULL`. If `count` is greater than or equal to the number of characters in `str`, the result is undefined.  
  
## Remarks  
 The `_mbsninc` function increments `str` by `count` multibyte characters. `_mbsninc` recognizes multibyte-character sequences according to the [multibyte code page](../VS_visualcpp/Code-Pages.md) currently in use.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsninc`|`_strninc`|`_mbsninc`|`_wcsninc`|  
  
 `_strninc` and `_wcsninc` are single-byte–character string and wide-character string versions of `_mbsninc`. `_wcsninc` and `_strninc` are provided only for this mapping and should not be used otherwise. For more information, see [Using Generic-Text Mappings](../VS_visualcpp/Using-Generic-Text-Mappings.md) and [Generic-Text Mappings](../VS_visualcpp/Generic-Text-Mappings.md).  
  
 `_mbsninc_l` is identical except that it uses the locale parameter passed in instead. For more information, see [Locale](../VS_visualcpp/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsninc`|<mbstring.h>|  
|`_mbsninc_l`|<mbstring.h>|  
|`_strninc`|<tchar.h>|  
|`_wcsninc`|<tchar.h>|  
  
 For more compatibility information, see [Compatibility](../VS_visualcpp/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## See Also  
 [String Manipulation](../VS_visualcpp/String-Manipulation--CRT-.md)   
 [Locale](../VS_visualcpp/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../VS_visualcpp/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_strdec, _wcsdec, _mbsdec, _mbsdec_l](../VS_visualcpp/_strdec--_wcsdec--_mbsdec--_mbsdec_l.md)   
 [_strinc, _wcsinc, _mbsinc, _mbsinc_l](../VS_visualcpp/_strinc--_wcsinc--_mbsinc--_mbsinc_l.md)   
 [_strnextc, _wcsnextc, _mbsnextc, _mbsnextc_l](../VS_visualcpp/_strnextc--_wcsnextc--_mbsnextc--_mbsnextc_l.md)