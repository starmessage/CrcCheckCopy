# [CrcCheckCopy version history/Changelog](https://github.com/starmessage/CrcCheckCopy/blob/master/ChangeLog.md)
All notable changes to this project will be documented in this file.

CheckCopy is a command line utility that lets you compare/verify a large number of files. 
It generates a single CRC-stamps file that contains the CRCs of each file. 
This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 

[CrcCheckCopy website](https://www.starmessagesoftware.com/crccheckcopy).  
[CrcCheckCopy distribution on GitHub](https://github.com/starmessage/CrcCheckCopy).  


## [2.7] - 2024-04-27
- Internal improvements
- Added Thumbs.db to the ignore list
- In the scan phase, when a file cannot be read, a random CRC is given so that an error will be produced during verification
- Added error message if the "root" folder to scan or verify does not exist (mainly because of a typing mistake)

Compatibility:
 - Windows XP to Windows 11. Architectures: 32 and 64 bit.
 - MacOS.  Architectures: x86_64 and Arm64.

## [2.6.1] - 2023-05-30
- Fixed: when a filename or path contains the quote (") character the program still calculates the file's CRC but does not verify the CRC and reports an error instead. This can happen on MacOS.

## [2.6] - 2023-04-08
- New faster CRC algorithm increases speed to 20x when calculating the CRC from files on the local SSD drive
- CRCstamps.txt will now include the file modification date. This will allow future versions to complete the verification faster by specifying an optional flag to skip files that have the same modification date.
- Internal improvements

## [2.4.1] - 2021-03-15 (Windows only edition)

### Fixed
- Bug in reading the license file of the PRO edition under Windows.

## [2.4] - 2021-03-14

### Added
- Help information for the /d command ([find duplicate files](https://www.starmessagesoftware.com/crccheckcopy/find-duplicate-files-windows-mac)).

### Fixed
- Bug in reading the license file of the [PRO edition](https://www.starmessagesoftware.com/crccheckcopy/features#pro).

## [2.2] - 2021-02-26

### Added
- Find zero byte files.
- Find duplicate files by their filesize and CRC32 (The filename is not examined: only the file size and its contents are checked).
- New command-line switch /d to scan folders for duplicate files.  
CrcCheckCopy /d path-to-scan-for-duplicates  
The list of the zero sized files and the duplicate files is saved in a file named "CrcCheckCopy-report-duplicates.txt"  
You can consider the zero byte files as a special kind of duplicate files: They have the same file size kai same contents.  
- Donation reminder added. Please [donate!](https://www.starmessagesoftware.com/crccheckcopy/download#donate) It's good karma.

### Changed
- During the scan mode, (with the /scan switch) at the end of the CRCstamps.txt file, there is an extra section for the zero-bytes files and duplicate files for you to be notified about them. 

## [2.1] - 2020-09-29

### Added
- For the Windows edition: Digitally code-signed.

## [2.0] - 2020-07-20

### Fixed

- Under Windows XP and Windows server 2003 32bit, there was a warning about the filesizes that do not match. 
But the comparison was proceeding reliably, despite the warning message. Checking of the filesizes is now fixed.

### Changed
- When you turn ON or OFF the telemetry, the program will inform you where the INI file with your choise is stored.
- Better error message when the CRCstamps.txt cannot be created (while scanning the files)
- Better error message when the CRCstamps.txt file is not found or could not be opened (while verifying the files).

## [1.9] - 2020-02-04

### Fixed

- When the folder to scan does not exist, the CRCstamps.txt looks as invalid.

## [1.8] - 2019-08-19

### Fixed

- Bug of missing INI file under Windows

### Changed

- Internal improvements

## [1.7] - 2019-06-06

### Changed

- Internal improvements for large files (>4GB) under Windows
- Ignore empty lines in CRCstamps.txt

## [1.6] - 2019-06-05

### Changed
- Internal improvements

### Added
- Usage statistics.  
SoftMeter, our application usage analytics library was added in CrcCheckCopy.  
This is a completely anonymised solution that will help us deliver a better product to you.  
During the first run the program will ask for your consent to enable SoftMeter.  
More info at https://www.starmessagesoftware.com/softmeter/data

## [1.5] - 2018-09-02

### Added
- Sorting of filepaths.  
The CRC stamps file contains now a sorted list of filepaths. Up to v1.4 the sequence of the files was unspecified (provided by the underlying directory table of the disk).  
You can disable the sorting using the switch "/ns" (no sorting).  

Having a sorted list of filepaths, allows you to compare two CRC stamp files.  
Some power users might prefer to compate the CRC stamp files, instead of using the /verify mode of CrcCheckCopy.  
For example, this trick allows you to run the /scan mode on two disks at the same time. Normally, you would need to wait for the /scan mode to complete before you can proceed to the /verify mode.  


- Keep the computer awake while the program runs (No sleep functionality).  
The computer will not enter low power (sleep) mode. This is useful for crc scans that take a lot of time and the computer goes to idle mode and the file comparison pauses.  
You can allow the computer to go to idle state by using the switch "/as" (allow sleep).

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
