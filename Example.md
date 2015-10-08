# Case Study #
_For options information see_<a href='https://code.google.com/p/peframe/wiki/Usage'>Usage</a> page.

## Automatic Analysis  (--auto) ##

  * **$ python peframe.py --auto malware.exe**
_Output too long, click_<a href='http://pastebin.com/yWNUCnC9'>here</a> on Pastebin. Or click <a href='http://pastebin.com/XHJQE1cP'>here</a> for Hesperbot Decrypted auto analysis.

## Hash file  (--hash) ##

  * **$ python peframe.py --hash malware.exe**

| MD5 : |  6e7e945aad40616e680d871c4ff1fa89 |
|:------|:----------------------------------|
| SHA1: |  4917a906864f35c02cbe589f5fb65e856c3db0a9 |

## First information (--info) ##

  * **$ python peframe.py --info malware.exe**

| Optional Header:	|	0x400000  |
|:-----------------|:----------|
| Address Of Entry Point: |		0x4f00   |
| Compile Time:	   |		1999-10-25 18:37:55 |
| Subsystem:		     |	IMAGE\_SUBSYSTEM\_WINDOWS\_GUI |
| Required CPU type:	|	IMAGE\_FILE\_MACHINE\_I386 |
| Number of RVA and Sizes: |	16        |
| DLL:		           |		False    |
| Number of Sections:	|	10        |

## Search for meta information (--meta) ##

  * **$ python peframe.py --meta malware.exe**

| LegalCopyright: | © 1997-2010 Kaspersky Lab ZAO. |
|:----------------|:-------------------------------|
| InternalName:   | klwtblfs                       |
| FileVersion:    | 2.6.8.3                        |
| CompanyName:    | WestByte                       |
| ProductName:    | Kaspersky Anti-Virus 1: Kaspersky™ Anti-Virus ®  is registered trademark of Kaspersky Lab ZAO. |
| ProductVersion: | 3.7.9.8                        |
| FileDescription:| WebToolBar component           |
| Translation:    | 0x0409 0x0000                  |

## Search for packer information (--peid) ##

  * **$ python peframe.py --peid malware.exe**

| PEID Signature Match(es): | [['Borland Delphi 3.0 (???)']] |
|:--------------------------|:-------------------------------|

## Sections analyzer (--sections) ##

  * **$ python peframe.py --sections malware.exe**

| Section | VirtualAddress | VirtualSize | SizeofRawData |	Suspicious |
|:--------|:---------------|:------------|:--------------|:-----------|
| .iVaz   | 0x1000         | 0x5a9       | 1536          | NO         |
| .XWp    | 0x2000         | 0x5e1       | 1536          | NO         |
| .qJlSa  | 0x3000         | 0x754       | 2048          | NO         |
| .text   | 0x4000         | 0x3499      | 13824         | NO         |
| .rdata  | 0x8000         | 0x13ff      | 5120          | NO         |
| .svqUa  | 0xa000         | 0x6eca      | 1536          | NO         |
| .sWc	   | 0x11000        | 0x1b2b      | 2560          | NO         |
| .xmz	   | 0x13000        | 0x9c04      | 2048          | NO         |
| .data   | 0x1d000        | 0x1b144     |	11264         | NO         |
| .rsrc   | 0x39000        | 0x2539c     |	152576        | YES        |

## Functions analyzer (--functions) ##

  * **$ python peframe.py --functions malware.exe**

|Imported DLLs and API:|
|:---------------------|
| `[1]` ADVAPI32.dll     |                      |
|                      | 0x408000 RegCreateKeyExW|
|                      | 0x408004 RegQueryValueExA|
|                      | 0x408008 RegQueryValueExW|
|                      | 0x40800c RegSetValueExA|
|                      | 0x408010 RegOpenKeyExW|
|                      | 0x408014 RegCloseKey |
| `[2]` KERNEL32.dll     |                      |
|                      | 0x40801c GetConsoleProcessList|
|                      | 0x408020 HeapCreate  |
|                      | 0x408024 SetConsoleLocalEUDC|
|                      | 0x408028 SetConsoleCursorPosition|
|                      | 0x40802c CreateJobObjectA|
|                      | 0x408030 AddAtomA    |
|                      | 0x408034 GetLocaleInfoA|
|                      | 0x408038 LocalFree   |
|                      | 0x40803c EnumTimeFormatsW|
|                      | 0x408040 GetVersionExA|
|                      | 0x408044 SetEndOfFile|
|                      | 0x408048 GetTimeFormatW|
|                      | 0x40804c GetConsoleMode|
|                      | 0x408050 SetConsoleCtrlHandler|
|                      | 0x408054 SetEnvironmentVariableA|
|                      | 0x408058 SetConsoleMode|
|                      | 0x40805c GetOEMCP    |
|                      | 0x408060 GetCommandLineA|
|                      | 0x408064 HeapFree    |
|                      | 0x408068 GetThreadPriorityBoost|
|                      | 0x40806c IsDBCSLeadByte|
|                      | 0x408070 SetThreadUILanguage|
|                      | 0x408074 GetCommProperties|
|                      | 0x408078 GetLastError|
|                      | 0x40807c GetFullPathNameA|
|                      | 0x408080 SetThreadPriorityBoost|
|                      | 0x408084 GetLocaleInfoW|
|                      | 0x408088 lstrcpy     |
|                      | 0x40808c WaitForSingleObject|
|                      | 0x408090 CreatePipe  |
|                      | 0x408094 ExitProcess |
|                      | 0x408098 SetFilePointer|
|                      | 0x40809c LCMapStringW|
|                      | 0x4080a0 EnumSystemLocalesA|
|                      | 0x4080a4 SetFirmwareEnvironmentVariableW|
|                      | 0x4080a8 GlobalMemoryStatusEx|
|                      | 0x4080ac SetCurrentDirectoryA|
|                      | 0x4080b0 WinExec     |
|                      | 0x4080b4 UnhandledExceptionFilter|
|                      | 0x4080b8 IsBadCodePtr|
|                      | 0x4080bc GetNumberOfConsoleInputEvents|
|                      | 0x4080c0 GetStringTypeW|
|                      | 0x4080c4 RtlUnwind   |
|                      | 0x4080c8 GetSystemTimeAsFileTime|
|                      | 0x4080cc FreeEnvironmentStringsA|
|                      | 0x4080d0 IsValidLocale|
|                      | 0x4080d4 GetDriveTypeA|
|                      | 0x4080d8 GetFileAttributesA|
|                      | 0x4080dc RtlMoveMemory|
|                      | 0x4080e0 GetPrivateProfileStructW|
|                      | 0x4080e4 CreateFileMappingA|
|                      | 0x4080e8 HeapUnlock  |
|                      | 0x4080ec GetConsoleScreenBufferInfo|
|                      | 0x4080f0 GetUserDefaultLCID|
|                      | 0x4080f4 MoveFileExW |
|                      | 0x4080f8 HeapReAlloc |
|                      | 0x4080fc GetComPlusPackageInstallStatus|
|                      | 0x408100 MultiByteToWideChar|
|                      | 0x408104 FileTimeToSystemTime|
|                      | 0x408108 GetEnvironmentStringsW|
|                      | 0x40810c GetConsoleTitleA|
|                      | 0x408110 Thread32Next|
|                      | 0x408114 SetConsoleDisplayMode|
|                      | 0x408118 CompareStringA|
|                      | 0x40811c TerminateProcess|
|                      | 0x408120 GetTimeZoneInformation|
|                      | 0x408124 CreateFileW |
|                      | 0x408128 WriteConsoleW|
|                      | 0x40812c LocalAlloc  |
|                      | 0x408130 GetFileType |
|                      | 0x408134 SetStdHandle|
|                      | 0x408138 GetSystemDefaultLCID|
|                      | 0x40813c GetPrivateProfileSectionNamesA|
|                      | 0x408140 MoveFileW   |
|                      | 0x408144 PeekConsoleInputA|
|                      | 0x408148 CreateFileA |
|                      | 0x40814c CreateFileMappingW|
|                      | 0x408150 BaseCheckAppcompatCache|
|                      | 0x408154 MapViewOfFileEx|
|                      | 0x408158 ReadFile    |
|                      | 0x40815c lstrcmpW    |
|                      | 0x408160 MapViewOfFile|
|                      | 0x408164 CloseHandle |
|                      | 0x408168 HeapDestroy |
|                      | 0x40816c AddLocalAlternateComputerNameA|
|                      | 0x408170 DosPathToSessionPathW|
|                      | 0x408174 VirtualAlloc|
|                      | 0x408178 GetConsoleCommandHistoryLengthA|
|                      | 0x40817c CreateProcessA|
|                      | 0x408180 GetSystemInfo|
|                      | 0x408184 WideCharToMultiByte|
|                      | 0x408188 GetStringTypeA|
|                      | 0x40818c GetEnvironmentVariableA|
|                      | 0x408190 VirtualQuery|
|                      | 0x408194 WaitForSingleObject|
|                      | 0x408198 VirtualFree |
|                      | 0x40819c CompareStringW|
|                      | 0x4081a0 FreeEnvironmentStringsW|
|                      | 0x4081a4 GetUserDefaultUILanguage|
|                      | 0x4081a8 GetConsoleSelectionInfo|
|                      | 0x4081ac WriteProfileStringA|
|                      | 0x4081b0 HeapAlloc   |
|                      | 0x4081b4 Beep        |
|                      | 0x4081b8 IsValidCodePage|
|                      | 0x4081bc GetConsoleCommandHistoryLengthW|
|                      | 0x4081c0 GlobalGetAtomNameA|
|                      | 0x4081c4 _hread_|
|                      | 0x4081c8 ScrollConsoleScreenBufferA|
|                      | 0x4081cc SetComputerNameW|
|                      | 0x4081d0 CloseProfileUserMapping|
|                      | 0x4081d4 LCMapStringA|
|                      | 0x4081d8 SetMessageWaitingIndicator|
|                      | 0x4081dc GetProcessHeap|
|                      | 0x4081e0 WriteProfileSectionA|
|                      | 0x4081e4 GetModuleHandleA|
|                      | 0x4081e8 SetHandleCount|
|                      | 0x4081ec GetSystemWow64DirectoryW|
|                      | 0x4081f0 GetStartupInfoA|
|                      | 0x4081f4 GetSystemDefaultLangID|
|                      | 0x4081f8 DosDateTimeToFileTime|
|                      | 0x4081fc GetStdHandle|
|                      | 0x408200 GetACP      |
|                      | 0x408204 GetCPInfo   |
|                      | 0x408208 ReleaseSemaphore|
|                      | 0x40820c OpenJobObjectW|
|                      | 0x408210 ReadConsoleInputA|
|                      | 0x408214 GetCurrentDirectoryA|
|                      | 0x408218 GetDateFormatW|
|                      | 0x40821c FlushFileBuffers|
|                      | 0x408220 SetEnvironmentVariableW|
| `[3]` USER32.dll       |                      |
|                      | 0x408228 wsprintfW   |
|                      | 0x40822c LoadStringW |
|                      | 0x408230 CharPrevA   |
|                      | 0x408234 LoadStringA |
| `[4]` MPR.dll          |                      |
|                      | 0x40823c WNetGetLastErrorW|
|                      | 0x408240 WNetGetConnectionA|
|                      | 0x408244 WNetEnumResourceA|
|                      | 0x408248 WNetCloseEnum|
|                      | 0x40824c WNetCancelConnection2A|
|                      | 0x408250 WNetGetConnection2A|
|                      | 0x408254 WNetAddConnection2A|
|                      | 0x408258 WNetOpenEnumW|
| `[5]` NTDLL.DLL        |                      |
|                      | 0x408260 RtlUnicodeStringToOemString|
|                      | 0x408264 NtClose     |
|                      | 0x408268 RtlOemStringToUnicodeString|
|                      | 0x40826c NtOpenFile  |
|                      | 0x408270 _strcmpi_|
|                      | 0x408274 RtlInitUnicodeString|
|                      | 0x408278 NtFsControlFile|
| `[6]` CFGMGR32.DLL     |                      |
|                      | 0x408280 CM\_Create\_DevNodeW|
|                      | 0x408284 CM\_Set\_HW\_Prof\_Flags\_ExA|
|                      | 0x408288 CM\_Disable\_DevNode|
|                      | 0x40828c CM\_Get\_Parent|
|                      | 0x408290 CM\_Query\_And\_Remove\_SubTreeW|
|                      | 0x408294 CM\_Find\_Range|
|                      | 0x408298 CM\_Get\_HW\_Prof\_Flags\_ExW|
|                      | 0x40829c CM\_Get\_Device\_Interface\_ListW|
|                      | 0x4082a0 CM\_Get\_Sibling|
|                      | 0x4082a4 CM\_Query\_Arbitrator\_Free\_Data\_Ex|
|                      | 0x4082a8 CM\_Add\_Range|
|                      | 0x4082ac CM\_Delete\_Class\_Key\_Ex|
|                      | 0x4082b0 CM\_Get\_First\_Log\_Conf\_Ex|
|                      | 0x4082b4 CM\_Add\_Res\_Des\_Ex|
|                      | 0x4082b8 CM\_Free\_Resource\_Conflict\_Handle|
|                      | 0x4082bc CM\_Set\_HW\_Prof\_FlagsW|

## Search for suspicious API and Sections (--suspicious) ##

  * **$ python peframe.py --suspicious malware.exe**

| API Functions: | |
|:---------------|:|
|	               | WinExec |
|	               | CreateProcessA |
|                | |
| Anti Debug:    | |
|                | UnhandledExceptionFilter |
|                | |
| Sections:      | |
|	               | .rsrc|

## Dumping all the information (--dump) ##

  * **$ python peframe.py --dump malware.exe**

_Output too long_

## Extract all the string (--strings) ##

  * **$ python peframe.py --strings malware.exe**

_Output too long_

## Extract File Name and Url (--url (or --file-url with peframe ≥ 0.4.1)) ##

  * **$ python peframe.py --url malware.exe**
For peframe ≥ 0.4.1 use option --file-url
  * **$ python peframe.py --file-url malware.exe**

| `http://ocsp.verisign.com0` |
|:----------------------------|
| `http://crl.verisign.com/tss-ca.crl0` |
| `http://ocsp.verisign.com0` |
| `http://crl.verisign.com/ThawteTimestampingCA.crl0` |
| `https://www.verisign.com/rpa` |
| `http://csc3-2009-2-crl.verisign.com/CSC3-2009-2.crl0D` |
| `https://www.verisign.com/rpa0` |
| `http://ocsp.verisign.com0?` |
| `http://csc3-2009-2-aia.verisign.com/CSC3-2009-2.cer0` |
| `https://www.verisign.com/rpa` |
| `https://www.verisign.com/cps0` |
| `https://www.verisign.com/rpa0` |
| `http://logo.verisign.com/vslogo.gif0` |
| `http://ocsp.verisign.com01` |
| `http://crl.verisign.com/pca3.crl0` |
| `http://crl.microsoft.com/pki/crl/products/MicrosoftCodeVerifRoot.crl0` |
| `https://www.verisign.com/rpa` |

## Reverse Hex Dump (--hexdump) ##

  * **$ python peframe.py --hexdump malware.exe**

_Output too long_