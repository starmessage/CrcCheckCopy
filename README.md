**CrcCheckCopy: Compare a big number of files by using their CRC stamps**

CheckCopy is a command line utility that lets you compare the files of different folders. 
It generates a CRC32 for each file and stores it in one CRCs stamps file. This small file can then be used to either check/compare another folder hierarchy, or be used as an integrity check of the same folder hierarchy. 
The files are compared in binary mode.

The comparison is completed in two steps.

- Step1 (Source scanning): reads all files of the source folder and creates in the current working directory one CRC stamps file ("CRCstamps.txt").
syntax:
  CrcCheckCopy /scan <SourceFolder>
If the path contains spaces, then include the path in quotes, e.g. 
  CrcCheckCopy /scan "C:\folder with spaces"

- Step2 (Verification): uses the CRC stamps file of Step1 to verify all the files at the destination folder.
syntax:
  CrcCheckCopy /verify <DestinationFolder>
If the destination folder has additional files that do not exist in the source folder, then these files will not be checked nor be reported.

- [CrcCheckCopy website](https://www.StarMessageSoftware.com/crccheckcopy)
- (c) StarMessage Software
 
**Operating system compatibility:**
- Windows XP and later, 32/64 bit

**Version history**
1.1
	Fixed: Removed the dependency on "msvcp140.dll" & "vcruntime140.dll". 
	Now, no extra files are needed.
	Fixed: Problems files/folders with unicode/Arabic/Persian/Greek file names.

1.0
	Initial public release




