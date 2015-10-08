# Usage #
_From command-line:_

> python peframe.py `<opt>` `<file>`


# Options #
| **Option** | **Short description** |
|:-----------|:----------------------|
| -h, --help | _This help_           |
| -a, --auto | Show Auto analysis    |
| -i, --info | PE file attributes    |
| --hash     | Hash MD5 & SHA1       |
| --meta     | Version info & metadata |
| --peid     | PE Identifier Signature |
| --antivm   | Anti Virtual Machine  |
| --antidbg  | Anti Debug | Disassembler |
| --sections | Section analyzer      |
| --functions | Imported DLLs & API functions |
| --suspicious | Search for suspicious API & sections |
| --dump     | Dumping all the information |
| --strings  | Extract all the string |
| --file-url | Extract File Name and Url |
| --file-verbose |Discover potential file name |
| --hexdump  | Hex dump              |
| --import   | List Entry Import instances |
| --export   | List Entry Export instances |
| --resource |	List Entry Resource instances |
| --debug    | List Entry DebugData instances |