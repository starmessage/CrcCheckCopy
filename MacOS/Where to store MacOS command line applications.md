## Where (in which folder) to store MacOS command-line application programs?

Also asked as:

### Where should shell tools be installed on Mac?
### Where should I save local executables on macOS?

This is part of the user instructions for the users of my MacOS command-line utility, [CrcCheckCopy](https://www.starmessagesoftware.com/crccheckcopy) that lets you compare folders and verify a large number of files using their CRC hashes.  

Like any other command-line utility, users download the Mac utility from the internet and need to store it "somewhere".  

MacOS power users suggest two locations:
- /usr/local/bin/
- ~/bin

ⓘ "bin" comes from "binary" file, which is the historical name for folders that contain executable binaries.

Comparison of the benefits and dissadvanages of each location:
| /usr/local/bin/   | ~/bin     |
| ----------------- | --------- |
| Folder contents available to all users. | Folder contents available only to current user. |
| The folder probably already exists and contains other utilities as well. | The folder probably does not exist. |
| If the folder does not exist, you can create it via the finder or from the Terminal with the command:<br/>```sh sudo mkdir -p /usr/local/bin ``` | If the folder does not exist, you can create it via the finder or from the Terminal with the command:<br/>```sh mkdir ~/bin ``` |
| Is part of the PATH so you can call the program by its name. | Not part of the PATH<sup>*</sup>, but you can call it using the ~/bin/. prefix, e.g. for CrcCheckCopy, call it as ~/bin/CrcCheckCopy |
| Stored together with other command-line utilities that get installed by other apps. |  Dedicated to your downloaded applications. Easy to remember which file is for what purpose.  |
| Fixed folder name. | You can name this folder what ever you want. |

<sup>*</sup>You can add it to the PATH variable by modifying the shell startup scripts (~/.bash_profile for bash which is the standard shell):
```sh  export PATH=$PATH:~/bin ```

After you save the command-line Mac utility to the folder you prefer, you still need to give it permissions to run as executable. This needs to be done just once, using the chmod command. For example, for CrcCheckCopy:  
```sh  chmod a+x ~/bin/CrcCheckCopy ```



[![HitCount](http://hits.dwyl.io/starmessage/badges.svg)](https://www.starmessagesoftware.com/)
[![Analytics](https://ga-beacon.appspot.com/UA-385839-11/github.com/starmessage/CrcCheckCopy/README.md)](https://GitHub.com/starmessage/CrcCheckCopy)
