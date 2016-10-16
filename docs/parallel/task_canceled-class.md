---
title: "task_canceled Class"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "concrt/concurrency::task_canceled"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "task_canceled class"
ms.assetid: c3f0b234-2cc1-435f-a48e-995f45b190be
caps.latest.revision: 10
ms.author: "mithom"
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
# task_canceled Class
This class describes an exception thrown by the PPL tasks layer in order to force the current task to cancel. It is also thrown by the `get()` method on [task](../Topic/Task%20Class%20-%20Internal%20Members.md), for a canceled task.  
  
## Syntax  
  
```
class task_canceled : public std::exception;
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[task_canceled::task_canceled Constructor](#task_canceled__task_canceled_constructor)|Overloaded. Constructs a `task_canceled` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `task_canceled`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="task_canceled__task_canceled_constructor"></a>  task_canceled::task_canceled Constructor  
 Constructs a `task_canceled` object.  
  
```
explicit _CRTIMP task_canceled(_In_z_ const char* _Message) throw();

task_canceled() throw();
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../parallel/concurrency-namespace.md)   
 [task::get Method](../parallel/task-class--concurrency-runtime-.md#task__get_method)   
 [cancel_current_task Method](../parallel/concurrency-namespace-functions.md)
