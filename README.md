## CrcCheckCopy: Compare a big number of files by using their CRC stamps

CheckCopy is a free command line utility that lets you compare folders and verify their files. 
It generates a single file that contains the CRC hashes of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

More info at the [CrcCheckCopy website](https://www.StarMessageSoftware.com/crccheckcopy)

## Features
- Compare folders.
- Compare file contents and verify them.
- Finds duplicate files (since ver 2.2), even if they have different filenames and different extensions and are stored in completely different folders.
- Creates the CRC hash of each file (like a digital signature of the file).
- Creates a single file with the CRC hashes of every file. This file can be used to compare another folder, or to verify the same folder in the future: to make sure that no file was deleted in the meantime or has been altered. In this way, it adds a digital signature to the whole folder structure and its files.
- No need for concurrent access to the two folders that must be compared.
- No need for network connection or internet bandwidth when comparing folders on remote computers: Only the CRC signatures file needs to be transferred between them. The program will run locally.
- Ensure integrity of backups: Store the CRC file together with the backup and you will be able to validate the integrity of the files and their contents at any time in the future.
- Cross platform (Windows, MacOS)
- Portable app. No installation needed. 
- Continue the comparison on another Operating System: Lets you compare a folder structure on Windows with its backup copy on a Mac/Macbook.
- Creates a report file with the comparison results, the zero sized files and the duplicate files found.
- The report is in plain text so you can furher process or parse it with other tools, e.g. import in to excel.

## Donate
[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.starmessagesoftware.com/crccheckcopy/download#donate)

## Download
- [Windows executable](https://github.com/starmessage/CrcCheckCopy/raw/master/Windows/CrcCheckCopy.exe)
- [MacOS executable](https://github.com/starmessage/CrcCheckCopy/raw/master/MacOS/CrcCheckCopy)

## Instructions

The comparison is completed in two steps.

### Step1 (Source scanning): reads all files of the source folder and creates in the current working directory one CRC stamps file ("CRCstamps.txt").

Syntax:
```sh
CrcCheckCopy /scan <SourceFolder>
```
or using the short version of the switch
```sh
CrcCheckCopy /s <SourceFolder>
```
If the path contains spaces, then include the path in quotes, e.g. 
```sh
CrcCheckCopy /scan "C:\folder with spaces"
```

### Step2 (Verification): uses the CRC stamps file of Step1 to verify all the files at the destination folder.
Syntax:
```sh
CrcCheckCopy /verify <DestinationFolder>
```
or using the short version of the switch
```sh
CrcCheckCopy /v <DestinationFolder>
```
If the destination folder has additional files that do not exist in the source folder, then these files will not be checked nor be reported.

### Detailed guide
[How does it compare two folders](https://www.starmessagesoftware.com/crccheckcopy/how-it-works)

### Operating system compatibility:
- Windows XP and later, 32/64 bit
- MacOS

### Version history
- [CrcCheckCopy Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)

[![HitCount](http://hits.dwyl.io/starmessage/badges.svg)](https://www.starmessagesoftware.com/)
[![Analytics](https://ga-beacon.appspot.com/UA-385839-11/github.com/starmessage/CrcCheckCopy/README.md)](https://GitHub.com/starmessage/CrcCheckCopy)
