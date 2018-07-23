# [CrcCheckCopy version history/Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
All notable changes to this project will be documented in this file.

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

[CrcCheckCopy website](https://www.starmessagesoftware.com/crccheckcopy).  
[CrcCheckCopy distribution on GitHub](https://github.com/starmessage/CrcCheckCopy).  

## [1.4] - 2018-07-23

### Added
- MacOS edition. CrcCheckCopy is now a cross platform command line utility: Runs under Windows and Mac OSX  
- Short switch parameters "/s", "/v" that you can also use instead of "/scan", "/verify"

### Changed
- Internal improvements


## [1.3.1] - 2018-07-13

### Fixed
- 32 bit compatibility restored


## [1.3] - 2018-07-12

### Fixed
- Bug in the performance statistics report for total sizes > 2GB

## [1.2] - 2018-07-10

### Added
- Performance statistics (kb/sec processed, files/sec processed).  
  These statistics can also be used to understand the computing power and the disk speed of your computer and compare it with another computer.  
  If you are comparing over the network, it will give you an indicatrion about the network speed.

### Changed
- Save the CRCs in HEX instead of decimal.  
  If you have CRC stamp files of previous versions (with decimal numbers) and you want to reuse those files in the future, then keep also a copy of CrcCheckCopy v1.1 that is able to read them.

## [1.1] - 2018-06-26

### Fixed
- Removed the dependency on "msvcp140.dll" & "vcruntime140.dll".  
  Now, no extra files are needed.
- Problems files/folders with unicode/Arabic/Persian/Greek file names.

## [1.0] - Initial public release

### Added
- Windows XP support
