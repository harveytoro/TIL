## CLR : Common Language Runtime

- Virtual Runtime Environment.
- Memory Management.
- Security Subsystem.
- Code Verification.

> .NET Framework
>> CLR
>>> ECMA
>>>> Common Lanaguage Infrastructure

- Portable executable file.
- Start address point to MSCOREE.dll
  + Initialise correct version of CLR
  + Loads and initialises CLR
  
- Types within Assemblies.
  + Types are housed in modules.
  + 1 Assembly one or more modules.
- Application domains = isolation boundry
  + Security
  + Resources / Cross domain marshalling
  + CLR always creates 3 applications domains
    + System : Precreates exceptions instances (e.g out of memory exceptions)
    + Shared : Contains MSCORELIB.dll, basic types, non-user mode code
    + Default : User code / assemblies

- Assemblies 
  + primary building block (.exe .dll)
  + Primary deployment unit
  + Assemblies are self describing
    + Reflection can be used to access all data
  + Contain one or more modules
  + Two Types
    + Shared Assemblies
      Used by multiple applications.
      Stored in the GAC.
      Strongly named.
    + Private Assemblies
      Local to same folder of application.
      Do not require strong names.
  + Assemblies located by identity
    + Strong name requires signing
    + Assembly identity: Assembly name + Version (Major.Minor.Build.Revision) + Culture + Public Key + Processor Architecture
