---
title: How to Create an IP Address Control
description: This topic demonstrates how to create an instance of an IP address control.
ms.assetid: 'E4DBECA6-B3F2-405F-8D95-32FA2334114D'
---

# How to Create an IP Address Control

This topic demonstrates how to create an instance of an IP address control.

## What you need to know

### Technologies

-   [Windows Controls](window-controls.md)

### Prerequisites

-   C/C++
-   Windows User Interface Programming

## Instructions

### 

Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](initcommoncontrolsex.md). Then use the [**CreateWindow**](https://msdn.microsoft.com/library/windows/desktop/ms632679) or the [**CreateWindowEx**](https://msdn.microsoft.com/library/windows/desktop/ms632680) function to create an instance IP address control. The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md#wc-ipaddress). Use the [**WS\_CHILD**](https://msdn.microsoft.com/library/windows/desktop/ms632600#ws-child) style, because there is no specific style constant associated with the IP address control.

In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](initcommoncontrolsex.md) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](initcommoncontrolsex-4vvx.md) structure to [**ICC\_INTERNET\_CLASSES**](initcommoncontrolsex-4vvx.md#icc-internet-classes), which specifies the IP address class. It then calls [**CreateWindowEx**](https://msdn.microsoft.com/library/windows/desktop/ms632680) to create an instance of the IP address control.


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&amp;icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## Related topics

<dl> <dt>

[IP Address Control Reference](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[About IP Address Controls](ip-address-controls.md)
</dt> <dt>

[Using IP Address Controls](using-ip-address-controls.md)
</dt> </dl>

 

 



