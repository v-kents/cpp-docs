---
title: "How to: Handle Events Using WRL"
ms.custom: na
ms.date: 10/04/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 1c77543f-7b0c-4a94-93bf-e3225885ed76
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
# How to: Handle Events Using WRL
This document shows how to use the Windows Runtime C++ Template Library (WRL) to subscribe to and handle the events of a Windows Runtime object.  
  
 For a more basic example that creates an instance of that component and retrieves a property value, see [How to: Activate and Use a Windows Runtime Component](../VS_visualcpp/How-to--Activate-and-Use-a-Windows-Runtime-Component-Using-WRL.md).  
  
## Subscribing to and Handling Events  
 The following steps start an `ABI::Windows::System::Threading::IDeviceWatcher` object and use event handlers to monitor progress. The `IDeviceWatcher` interface enables you to enumerate devices asynchronously, or in the background, and receive notification when devices are added, removed, or changed. The [Callback](../VS_visualcpp/Callback-Function--Windows-Runtime-C---Template-Library-.md) function is an important part of this example because it enables it to specify event handlers that process the results of the background operation. The complete example follows.  
  
> [!WARNING]
>  Although you typically use the WRL in a Windows 8.x Store app, this example uses a console app for illustration. Functions such as `wprintf_s` are not available from a Windows 8.x Store app. For more information about the types and functions that you can use in a Windows 8.x Store app, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx) and [Win32 and COM for Windows Store apps](http://msdn.microsoft.com/library/windows/apps/br205757.aspx).  
  
1.  Include (`#include`) any required Windows Runtime, WRL, or standard C++ library headers.  
  
     [!CODE [wrl-consume-event#2](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#2)]  
  
     Windows.Devices.Enumeration.h declares the types that are required to enumerate devices.  
  
     We recommend that you utilize the `using namespace` directive in your .cpp file to make the code more readable.  
  
2.  Declare the local variables for the app. This example holds count of the number of enumerated devices and registration tokens that enable it to later unsubscribe from events.  
  
     [!CODE [wrl-consume-event#7](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#7)]  
  
3.  Initialize the Windows Runtime.  
  
     [!CODE [wrl-consume-event#3](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#3)]  
  
4.  Create an [Event](../VS_visualcpp/Event-Class--Windows-Runtime-C---Template-Library-.md) object that synchronizes the completion of the enumeration process to the main app.  
  
     [!CODE [wrl-consume-event#4](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#4)]  
  
    > [!NOTE]
    >  This event is for demonstration only as part of a console app. This example uses the event to ensure that an async operation completes before the app exits. In most apps, you typically don’t wait for async operations to complete.  
  
5.  Create an activation factory for the `IDeviceWatcher` interface.  
  
     [!CODE [wrl-consume-event#5](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#5)]  
  
     The Windows Runtime uses fully-qualified names to identify types. The `RuntimeClass_Windows_Devices_Enumeration_DeviceInformation` parameter is a string that's provided by the Windows Runtime and contains the required runtime class name.  
  
6.  Create the `IDeviceWatcher` object.  
  
     [!CODE [wrl-consume-event#6](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#6)]  
  
7.  Use the `Callback` function to subscribe to the `Added`, `EnumerationCompleted`, and `Stopped` events.  
  
     [!CODE [wrl-consume-event#8](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#8)]  
  
     The `Added` event handler increments the count of enumerated devices. It stops the enumeration process after ten devices are found.  
  
     The `Stopped` event handler removes the event handlers and sets the completion event.  
  
     The `EnumerationCompleted` event handler stops the enumeration process. We handle this event in case there are fewer than ten devices.  
  
    > [!TIP]
    >  This example uses a lambda expression to define the callbacks. You can also use function objects (functors), function pointers, or [std::function](../VS_visualcpp/function-Class.md) objects. For more information about lambda expressions, see [Lambda Expressions](../VS_visualcpp/Lambda-Expressions-in-C--.md).  
  
8.  Start the enumeration process.  
  
     [!CODE [wrl-consume-event#9](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#9)]  
  
9. Wait for the enumeration process to complete and then print a message. All `ComPtr` and RAII objects leave scope and are released automatically.  
  
     [!CODE [wrl-consume-event#10](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#10)]  
  
 Here is the complete example:  
  
 [!CODE [wrl-consume-event#1](../CodeSnippet/VS_Snippets_Misc/wrl-consume-event#1)]  
  
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `wrl-consume-events.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe wrl-consume-events.cpp runtimeobject.lib**  
  
## See Also  
 [Windows Runtime C++ Template Library (WRL)](../VS_visualcpp/Windows-Runtime-C---Template-Library--WRL-.md)