# comic-fastag
Quickly tag all zip files into a pre-set Series-name, Author, Penciller and Inker

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
