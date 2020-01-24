## CrcCheckCopy: Compare a big number of files by using their CRC stamps

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

More info at the [CrcCheckCopy website](https://www.StarMessageSoftware.com/crccheckcopy)

## Download
- [Windows executable](https://github.com/starmessage/CrcCheckCopy/raw/master/Windows/CrcCheckCopy.exe) | See the [antivirus scan results (VirusTotal)](https://www.virustotal.com/gui/url/55b511074a6b1c49e1139951f4bd00c61297977f0dd09c38d8ea7e08b26d8e54/detection)
- [MacOS executable](https://github.com/starmessage/CrcCheckCopy/raw/master/MacOS/CrcCheckCopy) | See the [antivirus scan results (VirusTotal)](https://www.virustotal.com/gui/url/7bb3be975da3cbda8dd6051810811f352877630ff0398ebfa72737e97bbf9e3d/detection)

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


### Operating system compatibility:
- Windows XP and later, 32/64 bit
- MacOS

### Version history
- [CrcCheckCopy Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
