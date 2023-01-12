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

## Command Tasks
```
Tool for generating bulk tagging for chapters and volumes

 tagvol - Tag all volumes
 tagchap - Tag all chapters
 tagart - Tag all files with artist name
 renchap - Rename all chapters according to config file
 renvol - Rename all volumes according to config file
 renart - Insert artist on all cbz filenames
 zipall - Zip all directories as separate files according to filename
 zip2cbz - Rename all zip to cbz
 cbz2zip - Rename all cbz to zip
 editconf - Edit configuration file
 generateLRmobi - Batch convert all cbz to mobi (Western Mode)
 generateRLmobi - Batch convert all cbz to mobi (Manga Mode)
 generatewebmobi - Batch convert all cbz to mobi using webtoon mode
 delXML - Remove all ComicInfo.xml from all cbz files
 init - Create a config file for editing
```
- tagvol - Tag all volumes found in the current directory. Note that only cbz files with vol prefix name will be tagged.
- tagchap - Tag all chapters found in the current directory. Note that only cbz files with c prefix name will be tagged.
- tagart - Tag all cbz files found in the current directory. Series tag will be ignored. Instead, the title name will be used as the series name.
- renvol - Rename the filename of any volXX.cbz files with format "[Artist] Series name VXX.cbz"
- renchap - Rename the filename of any cXXX.cbz files with format "[Artist] Series name cXXX.cbz"
- renart - Rename the filename of any cbz file with format "[Artist] Filename.cbz"

## Directory structure
```
user@testbuild:~/ebook-workshop/structured$ ls
vol01  vol02
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
    
