# MS16-032

C# version with [@FuzzySec](https://twitter.com/FuzzySec) powershell code which does not rely on powershell.exe. Instead it runs from a powershell runspace environment (.NET). Helpful in security restricted environments with GPO, SRP, App Locker.

### How to Compile it:

To compile MS16-032 you need to import this project within Microsoft Visual Studio or if you don't have access to a Visual Studio installation, you can compile it as follows:

To Compile as x86 binary:

```
cd C:\Windows\Microsoft.NET\Framework64\v4.0.30319 (Or newer .NET version folder)

csc.exe /unsafe /reference:"C:\path\to\System.Management.Automation.dll" /reference:System.IO.Compression.dll /out:C:\users\public\MS16-032x86.exe /platform:x86 "C:\path\to\MS16-032\MS16-032\*.cs"
```

To Compile as x64 binary:

```
cd C:\Windows\Microsoft.NET\Framework64\v4.0.30319 (Or newer .NET version folder)

csc.exe /unsafe /reference:"C:\path\to\System.Management.Automation.dll" /reference:System.IO.Compression.dll /out:C:\users\public\MS16-032x64.exe /platform:x64 "C:\path\to\MS16-032\MS16-032\*.cs"
```

MS16-032 uses the System.Management.Automation namespace, so make sure you have the System.Management.Automation.dll within your source path when compiling outside of Visual Studio.

### Credits:

All credits go to [@FuzzySec](https://github.com/FuzzySecurity/PowerShell-Suite/blob/master/Invoke-MS16-032.ps1).
