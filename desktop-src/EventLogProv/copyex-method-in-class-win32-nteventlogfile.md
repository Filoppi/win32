---
Description: 'Copies the logical file or directory specified in the Win32\_NTEventlogFile.Name property to the location specified by the FileName parameter.'
ms.assetid: '4996fdfb-556d-48b6-afe1-83734bc8df18'
title: 'CopyEx method of the Win32\_NTEventlogFile class'
---

# CopyEx method of the Win32\_NTEventlogFile class

The **CopyEx** [WMI class](https://msdn.microsoft.com/library/aa393244) method copies the logical file or directory specified in the **Win32\_NTEventlogFile.Name** property to the location specified by the *FileName* parameter. A copy is not supported if overwriting an existing logical file is required. This method is an extended version of the [**Copy**](https://msdn.microsoft.com/library/aa389347) method.

This topic uses Managed Object Format (MOF) syntax. For more information about using this method, see [Calling a Method](https://msdn.microsoft.com/library/aa384832).

## Syntax


```mof
uint32 CopyEx(
  [in]�����������string FileName,
  [out]����������string StopFileName,
  [in, optional]�string StartFileName,
  [in, optional]�boolean Recursive
);
```



## Parameters

<dl> <dt>

*FileName* \[in\]
</dt> <dd>

Fully qualified name of the copy of the file (or directory).

Example: c:\\temp\\newdirectory

</dd> <dt>

*StopFileName* \[out\]
</dt> <dd>

Name of the file or directory where the **CopyEx** method failed. This parameter is **null** if the method succeeds.

</dd> <dt>

*StartFileName* \[in, optional\]
</dt> <dd>

Names the child file or directory to use as a starting point for **CopyEx**. The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call. If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.

</dd> <dt>

*Recursive* \[in, optional\]
</dt> <dd>

If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](https://msdn.microsoft.com/library/aa387893) instance.

> [!Note]  
> For file instances, the *Recursive* input parameter is ignored.

�

</dd> </dl>

## Return value



| Return code                                                                       | Description                                                    |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | The request was successful.<br/>                         |
| <dl> <dt>**2**</dt> </dl>  | Access was denied.<br/>                                  |
| <dl> <dt>**8**</dt> </dl>  | An unspecified failure occurred.<br/>                    |
| <dl> <dt>**9**</dt> </dl>  | The name specified was not valid.<br/>                   |
| <dl> <dt>**10**</dt> </dl> | The object specified already exists.<br/>                |
| <dl> <dt>**11**</dt> </dl> | The file system is not NTFS.<br/>                        |
| <dl> <dt>**12**</dt> </dl> | The platform is not Windows.<br/>                        |
| <dl> <dt>**13**</dt> </dl> | The drive is not the same.<br/>                          |
| <dl> <dt>**14**</dt> </dl> | The directory is not empty.<br/>                         |
| <dl> <dt>**15**</dt> </dl> | There has been a sharing violation.<br/>                 |
| <dl> <dt>**16**</dt> </dl> | The start file specified was not valid.<br/>             |
| <dl> <dt>**17**</dt> </dl> | A privilege required for the operation is not held.<br/> |
| <dl> <dt>**21**</dt> </dl> | A parameter specified is not valid.<br/>                 |



�

## Requirements



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�XP<br/>                                                                |
| Minimum supported server<br/> | Windows Server�2003<br/>                                                       |
| Namespace<br/>                | Root\\CIMV2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Ntevt.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntevt.dll</dt> </dl> |



## See also

<dl> <dt>

[Operating System Classes](https://msdn.microsoft.com/library/aa392727)
</dt> <dt>

[**Win32\_NTEventlogFile**](win32-nteventlogfile.md)
</dt> </dl>

�

�



