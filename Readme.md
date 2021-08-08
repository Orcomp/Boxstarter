# Boxstarter scripts

This repository contains [boxstarter](https://boxstarter.org/) scripts to help setup a dev environment on a new windows box.

There is a two step process, some large installs like VS, SQL server etc.. are done manually.

You can run the scripts multiple times. If a program is already installed it will just be skipped.
 
The Windows configs for Boxstarter can be found [here](https://boxstarter.org/WinConfig)

## Introduction

Every time I do a clean Windows install I update the scripts and notes on this page, in order to make the next clean install easier and faster.
The goal is to setup a productive .NET dev environment as quickly as possible by only installing the bare minimum. 

These notes and scripts were first started around 2014, and have gone through numerous revisions. (I typically re-install Windows every 6 months.)

- Settings and licenses are stored in "C:\Source\Licenses and Settings" 

## Pre-Install

Read docs\Checklist_NewInstall.md

## Install

- The Boxstarter list only contains software I use regularly.
- The Boxstarter links to use in IE (or Edge) are found at the top of each file.
- The order in which the files should be run are:

    1. Manual: Update BIOS (for new Windows installs)
    1. Boxstarter: **UpdateWindows.txt** (Run this just after installing windows.)
      - Double check the file and uncomment line for Dell installs
    1. Manual: Install drivers (for new Windows installs) 
    1. Manual: Run PowerShell Scripts to set correct settings for Win10 (See section below)
    1. Boxstarter: **InstallSoftware.txt** (Run 2 or 3 times until no more errors occur)
    1. Manual Installs:
      - [Directory Opus](https://www.gpsoft.com.au/)
      - [Rider](https://www.jetbrains.com/rider/) (Seriously good C# dev IDE. Install from Toolbox)
        - [DotTrace](https://www.jetbrains.com/profiler/) (Install from Toolbox as well)
      - [VisualStudio - Preview](https://visualstudio.microsoft.com/vs/preview/) 
        - NOTE: See VisualStudio_Rider_Setup.md file, to setup Rider and VS
      - MS Office (Through office365)  
      - [OneDrive](https://onedrive.live.com/about/en-au/download/)
      - [bvckup2](https://bvckup2.com/)
      - [WordWeb](https://wordweb.info) (Pro version)
      - [Greenshot](https://github.com/greenshot/greenshot/releases) (Latest release from Github)
      - [AsciiDoctor](https://asciidoctor.org/)
      - [splashtop](https://www.splashtop.com/) (Server and client)
    1. Boxstarter: **PostInstall.txt**
    1. Manual: Run "Disk Cleaner" from the command line

**NOTE:** Whenever you need a program check [Chocolatey](https://chocolatey.org/packages) first. It is the best place to discover the most used programs by developers for any category.

Read the "docs\SoftwareToKeepAnEyeOn.md" document.

Product keys are available from: https://my.visualstudio.com/productkeys

Licenses and settings are available here: https://github.com/Orcomp/Licenses-and-settings (which is private ;-). Check the FolderStructure.md file to re-establish the right folder structure for various programs.
### Paid Software

I generally try and use free or open source software as much as possible. So when I pay for something it has to be worth it.

- [Directory Opus](https://www.gpsoft.com.au/)
- [bvckup2](https://bvckup2.com/)
- [Fences](https://www.stardock.com/products/fences/)
- [WordWeb](https://wordweb.info)
- [Fork - git](https://git-fork.com/)
- [Duplicate Cleaner Pro](https://www.duplicatecleaner.com/)
- [Obsidian](https://obsidian.md/)
- [GitKraken](https://www.gitkraken.com/git-client) (git client)
- [dendron](https://www.dendron.so/)
- [Scapple](https://www.literatureandlatte.com/scapple/overview)

## Post Install - Configurations

- Files and Folder:
  - [Folder Organisation](http://www.howtogeek.com/howto/15677/zen-and-the-art-of-file-and-folder-organization/)
- Set another text editor as default (instead of notepad): https://www.winhelponline.com/blog/replace-notepad-text-editor-notepad-plus-association
- Run Sysinternals Autoruns to manage programs that are allowed to startup on their own.
- Make sure Drives have the right name. (Run "Disk Management" from the command line. See this [link](https://www.diskpart.com/articles/drive-letter-not-available-8523.html) for help)
- Install Dropbox and point it to "I:\Dropbox"
- Install OneDrive and point it to "I:\Files\..."

### Windows

- Enable "Night Light" settings
- Make sure "Hardware-accelerated GPU scheduling" is turned on in "Display settings > Graphics Settings (bottom of the page) > Hardware-accelerated GPU scheduling = true"
- Make sure HDD is not indexed and is not allowed to sleep (otherwise it causes windows to freeze every so often). Control Panel > Power Options, choose your preferred plan > Change Advanced power settings > Hard Disk > Turn off hard disk after .... and set it to "never".

#### Setup Scripts

This looks like the best, active, up to date script to be use: https://github.com/hellzerg/optimizer (Also assess: https://github.com/farag2/Sophia-Script-for-Windows)

Other scripts:

- https://github.com/farag2/Windows-10-Sophia-Script
- https://github.com/ChrisTitusTech/win10script
  - https://christitus.com/debloat-windows-10-2020/ (Chris continually keeps this up to date.)
- https://github.com/Sycnex/Windows10Debloater
- https://github.com/gordonbay/Windows-On-Reins
- https://github.com/Disassembler0/Win10-Initial-Setup-Script No longer active. Cloned the repo and have my own My.preset options.

Notes:

Other simple GUI tools to consider ([Beware](https://www.mirinsoft.com/blog/19-apps/34-stable-release-of-new-spydish-app-is-out) see comment section):
  - [SpyDish](https://github.com/builtbybel/spydish)
  - [BloatBox](https://github.com/builtbybel/bloatbox)

#### Task Scheduler

- Setup script to create new workspace on login. (See I:\Scripts)

#### Settings

- Settings > Search > Searching Windows > disable
- Might need to disable this on all HDDs directly as well. (Right click on the HDD drive, Properties, disable indexing)
- Notifications and actions > disable all notifications

#### Teams

- Settings > Disable hardware acceleration. (Causes images to jitter) 

#### Setup Date Time, Region, Language properly

- https://support.gitkraken.com/known-issues/date-format/

#### Icons

- Right click on desktop and change the icons to small (Should be set by PowerShell script).

#### Power Plan

- Make sure power plan is on ultimate or performance
- Never sleep or hibernate

#### Disable auto restart on scheduled updates

- https://www.makeuseof.com/tag/disable-forced-restarts-windows-update/
- Disable reboot after updates: https://www.minitool.com/news/prevent-windows-update-from-automatically-restarting-your-pc.html

#### Disable Encryption

- Device Encryption : Turn Off (Turn off bitlocker on Windows 10 Pro or above)

#### Extensions

Chrome (Should be synced to Google account):
  - Toby
  - Session Buddy
  - Octotree
  - Todoist
  - Todoist for Gmail
  - EasyReader
  - Polar (PDF reader) (https://getpolarized.io/)
  - Paperpile
  - DuckDuckGo Privacy Essentials
  - Github Writer (https://github.com/ckeditor/github-writer)

Vivaldi
  - Same as Chrome
  - Vivaldi email

**Keep an eye on:**

- [Tabli](https://github.com/antonycourtney/tabli)
- Tidy Bookmark Tree

### Antivirus

The default anti virus that comes with Windows is good enough.

Configure Defender from PowerShell. See the [docs](https://docs.microsoft.com/en-us/powershell/module/defender/?view=win10-ps).

Some more useful [docs](https://www.reddit.com/r/Windows10/comments/5gf38v/when_excluding_a_process_in_windows_defender_do_i/) and [here](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/configure-extension-file-exclusions-windows-defender-antivirus)

Run as admin (Copy and paste into PowerShell)
```
Add-MpPreference -ExclusionPath 'C:\Source', 'C:\Users\Ben\.nuget', 'C:\Users\Ben\AppData\Roaming\WildGums', 'I:\', 'K:\'

Add-MpPreference -ExclusionProcess 'C:\Program Files\Bvckup 2\*', 'C:\Program Files (x86)\Microsoft Visual Studio\*', 'C:\Program Files (x86)\Splashtop\*', 'C:\Program Files\FreeFileSync\Bin\*', 'C:\Program Files\GPSoftware\Directory Opus\*', 'C:\Program Files (x86)\Duplicate Cleaner Pro\*', 'C:\Program Files\Microsoft VS Code\*', 'C:\Users\Ben\AppData\Local\Fork\*'
```

### Partitions

Since the OS will be going on a SSD drive no need to partition.

## Notes

- Markdown: Use VSCode with some markdown extensions
- VSCode extensions: https://stackoverflow.com/questions/35773299/how-can-you-export-vs-code-extension-list
- Visual Studio extensions: Sync to account
- Chrome Extensions: type in "chrome://system" then click on the expand extensions button (Google should remember the extensions as they are saved to my Google account.)
  - Session Buddy
  - Toby
  - Todoist
  - Octotree
  - EasyReader
  - Paperpile
- DirectoryOpus settings (Opus has a great wizard to save and restore settings)

### C# Scripting

Looks like dotnet-script is the best current solution with full support in VS Code.
The file extension is ".csx".

- [Guide](https://galdin.dev/blog/csharp-scripts-using-dotnet-script/)
- [dotnet-script](https://github.com/filipw/dotnet-script)

## Guides
### bvckup v2

Probably the fastest way of copying files from one directory to another

Straight one time copy of files from one folder to another: https://bvckup2.com/support/forum/topic/917

- Manually run job
- Copy files in full
- Disable move/rename detection

Make sure anti-virus software is disabled

### NAS Setup (LACIE-2Big)

Make sure to create a user account on the NAS that has exactly the same username and password as the windows (workstation) login.

Login to the NAS using http:\\lacie-2big-nas

### Printer Scanner

Install drivers and toolbox for MF 4350d.

This can be very tricky. After a lot of research follow these steps:

- Do NOT plug the USB cable from the printer to the computer.
- First install the drivers and patch from the Canon USA site.
- Search for MF 4350d here https://www.usa.canon.com/internet/portal/us/home
- Install the drivers and patch then reboot.
- Then install the Toolbox software. Make changes to the software to always run as admin. Follow the instructions here: https://community.usa.canon.com/t5/Office-Printers/MF-toolbox-can-t-find-scanner/td-p/223042

#### Kyocera: 
- Install [Kyocera](https://www.kyoceradocumentsolutions.com.au/support-centre/downloads) drivers

