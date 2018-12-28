
## Backup Applications

All these programs will be installed by chocolatey.

- [UltraSearch](https://www.jam-software.com/ultrasearch/)
- [FreeFileSync](https://freefilesync.org/)
- [AllDup](http://www.alldup.de/alldup_help/alldup.php)
- TreeSize free
- DirectoryOpus

## Strategy

When trying to consolidate backed up files and folders from multiple hard drives, always start with the latest version.

Then delete duplicate files and structure things on all older devices (one at a time).

## Notes

- Turn off Windows Defender when moving large amounts of files (Turn off internet access first)
- Zip, archive database files (DATA folder)

## Folders that can safely be deleted (on inactive drives)

### General

- Program Files/ Visual Studio
- Temp
- Windows
- AppData\Local\NuGet
- Program Files\Visual Studio (All versions)
- obj, Bin, Lib (in development machines, C# solutions)
- MSOCache
- $WINDOWS.~BT and $WINDOWS.~WS
- ProgramData/PackageCache: https://superuser.com/questions/455853/can-i-delete-the-folder-c-programdata-package-cache?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa

### Specific to my setup

- C:\Source\_packages
- C:\Source\_symbols
- AppData\Local\NuGet
- Syncfusion
- JetBrains program files
- Delete exe that have been downloaded in Downloads folder

## Transfer Files

bvckup v2 is probably the fastest way of copying files from one directory to another, or one hard drive to another. (But disable virus checking before doing this! otherwise it will slow everything down.)


### bvckup v2 settings for "one time straight copy"

Straight one time copy of files from one folder to another: https://bvckup2.com/support/forum/topic/917

- Manually run job
- Copy files in full
- Disable move/rename detection

Make sure anti-virus software is disabled

## Links

- https://www.howtogeek.com/howto/30173/what-files-should-you-backup-on-your-windows-pc/

Files to backup: https://www.makeuseof.com/tag/backup-windows-files-folders/