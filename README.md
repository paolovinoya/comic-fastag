# comic-fastag
Quickly tag all zip files into a pre-set Series-name, Writer, Penciller and Inker. The tool kcc-c2e will identify the title of the epub/mobi file with the Series field name. Writer, Penciller and Inker will be considered as authors of the same series. 

Comictagger command-line syntax was difficult replicate against multiple comic books. This script is meant to prepare the details together and perform a bulk-change of xml tags on all comic books in the same directory.

## Required/Dependencies
### Python projects
- [comictagger](https://github.com/comictagger/comictagger)
- [kcc-c2e](https://github.com/ciromattia/kcc)
### Linux commands used
- rename
- 7zip/p7zip

## First Time Run
To make the script function for the first time in any directory, it needs to deposit its blank configuration as a hidden file.
- Run `comic-fastag init`
- See the contents by typing `cat .bulk-rename.conf`

## Directory structure
```
user@testbuild:~/ebook-workshop/structured$ comic-fastag zipall
Title of series is :  Test Comic Series name
Writer is :  Mr Writer
Penciller is :  Mr Inker
Inker is :  Mr Inker

7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C.UTF-8,Utf16=on,HugeFiles=on,64 bits,8 CPUs AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx   (810F81),ASM,AES-NI)

Scanning the drive:
1 folder, 164 files, 148136231 bytes (142 MiB)

Creating archive: vol01.zip

Items to compress: 165


Files read from disk: 164
Archive size: 142636545 bytes (137 MiB)
Everything is Ok

7-Zip [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C.UTF-8,Utf16=on,HugeFiles=on,64 bits,8 CPUs AMD Ryzen 5 3500U with Radeon Vega Mobile Gfx   (810F81),ASM,AES-NI)

Scanning the drive:
1 folder, 162 files, 197740861 bytes (189 MiB)

Creating archive: vol02.zip

Items to compress: 163


Files read from disk: 162
Archive size: 193643625 bytes (185 MiB)
Everything is Ok
user@testbuild:~/ebook-workshop/structured$ ls
vol01  vol01.zip  vol02  vol02.zip
user@testbuild:~/ebook-workshop/structured$
```
    
