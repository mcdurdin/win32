---
Description: Launches the Passport Wizard when used with Rundll32.exe.
title: PassportWizardRunDll function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# PassportWizardRunDll function

\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.\]

Launches the Passport Wizard when used with Rundll32.exe.

## Syntax


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## Parameters

<dl> <dt>

*hwndStub* \[in\]
</dt> <dd>

Type: **HWND**

A handle to an owner window. This parameter is typically set to **NULL**.

</dd> <dt>

*hAppInstance* \[in\]
</dt> <dd>

Type: **HINSTANCE**

A handle to the library file, obtained as a return value from [**LoadLibrary**](https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65)("netplwiz").

</dd> <dt>

*lpszCmdLine* \[in\]
</dt> <dd>

Type: **LPTSTR**

Argument data. This value will always be empty.

</dd> <dt>

*nCmdShow* \[in\]
</dt> <dd>

Type: **int**

Sets the display mode for the window.

</dd> </dl>

## Return value

None.

## Remarks

The Passport Wizard is used to obtain a default Passport for Windows. A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address. Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.

**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:

**rundll32.exe netplwiz.dll, PassportWizardRunDll**

Using an entry point function with Rundll32.exe does not resemble a normal function call. The function name and the name of the .dll file where it is stored are used only as command-line parameters. The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32. The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32. **PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.

## Requirements



|                                     |                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                                                     |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                                            |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (version 5.60 or later)</dt> </dl> |



 

 



