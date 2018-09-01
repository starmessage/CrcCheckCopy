# [CrcCheckCopy version history/Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
All notable changes to this project will be documented in this file.

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

[CrcCheckCopy website](https://www.starmessagesoftware.com/crccheckcopy).  
[CrcCheckCopy distribution on GitHub](https://github.com/starmessage/CrcCheckCopy).  


## [1.5] - Unreleased

### Added
- Sorting of filepaths.  
The CRC stamps file contains now a sorted list of filepaths. Up to v1.4 the sequence of the files was unspecified (provided by the underlying directory table of the disk).  
Having a sorted list of filepaths, allows you to compare two CRC stamp files.  
Some power users might prefer to compate the CRC stamp files, instead of using the /verify mode of CrcCheckCopy.  
For example, this trick allows you to run the /scan mode on two disks at the same time. Normally, you would need to wait for the /scan mode to complete before you can proceed to the /veify mode.  
You can disable the sorting using the switch "/ns" (no sorting).

- Keep the computer awake while the program runs (No sleep functionality).  
The computer will not enter low power (sleep) mode. This is useful for crc scans that take a lot of time and the computer goes to idle mode and the file comparison pauses.  
You can disable the sorting using the switch "/as" (allow sleep).

- Show progress.  
The program will show a file counter next to the "Ok" indicator, e.g. 1293/187471, meaning it is processing the 1293th file of a total of 187471 files.  
During the CRC verification mode, the total files are not shown.  
You can enable the progress indicator using the switch "/sp" (show progress).

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
