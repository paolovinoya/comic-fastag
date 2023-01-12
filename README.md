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
`
structured
├── 01
│   ├── 01-001.0-001.jpg
│   ├── 01-001.0-002.jpg
│   ├── 01-001.0-003.jpg
|    ...
└── 02
    ├── 02-005.0-001.jpg
    ├── 02-005.0-002.jpg
    ├── 02-005.0-003.jpg
    ...
    └── 02-009.0-033.jpg
 `   
    
    
