## Windows Locations

GAC - Global Assembly Cache.

```bash
%windir%\Microsoft.NET\assembly
```

Patch cache, installer patch cache.

```bash
%WINDIR%\Installer\$PatchCache$
```

Finding service exe files.

```bash
Regedit > HKEY_LOCAL_MACHINE > SYSTEM > CurrentControlSet > Services 
```

ODBC Data Source Administrator.

```bash
%SystemRoot%\SysWOW64 > odbcad32.exe
```

ILDasm IL Disassembler

```bash
%HomeDrive%\Program Files (x86)\Microsoft SDKs\Windows\v10.0A\bin\NETFX 4.6 Tools > ildasm.exe
```
