# [CrcCheckCopy Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
All notable changes to this project will be documented in this file.

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

[CrcCheckCopy website](https://www.starmessagesoftware.com/crccheckcopy).  
[CrcCheckCopy distribution on GitHub](https://github.com/starmessage/CrcCheckCopy).  

## [upcoming versions] - Unreleased

### Changed
- Save the CRCs in HEX instead of decimal

## [1.2] - Unreleased

### Added
- Performance statistics (kb/sec processed, files/sec processed).  
  These statistics can also be used to understand the computing power and the disk speed of your computer and compare it with another computer.

## [1.1] - 2018-06-26

### Fixed
- Removed the dependency on "msvcp140.dll" & "vcruntime140.dll".  
  Now, no extra files are needed.
- Problems files/folders with unicode/Arabic/Persian/Greek file names.

## [1.0] - Initial public release

### Added
- Windows XP support
