## CrcCheckCopy: Compare a big number of files by using their CRC stamps

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

More info at the [CrcCheckCopy website](https://www.StarMessageSoftware.com/crccheckcopy)

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


### Operating system compatibility:
- Windows XP and later, 32/64 bit

### Version history
- [CrcCheckCopy Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
