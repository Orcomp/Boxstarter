Boxstarter scripts to setup a dev environment on a new windows box.

There is a two step process, some large installs like VS, SQL server etc.. are done manually.

You can run the scripts multiple times. If a program is already installed it will just be skipped.

## Introduction

- The boxstarter list only contains software I use regularly.
- The boxstarter links to use in IE are found at the top of each file.
- The order in which the files should be run are:
    1. Update BIOS (for new installs)
    1. **UpdateWindows.txt** (Run this just after installing windows.)
    1. Install drivers (for new installs)
    1. **InstallSotware.txt**
    1. Install seperately:
        - VS (large download)
        - Office (large download)
        - Skype (Chocolatey does not handle Skype well)
        - VS Code (They recommend not to use chocolatey)
        - Fences
    1. **PostInstall.txt**
    1. **UpdateWindows.txt** (Run windows update again.)
    1. Run CCleaneer and KCleaner to get rid of all the junk. (These are installed in the scripts above)
    1. Run [Simple System Tweaker](http://www.tweaking.com/content/page/simple_system_tweaker.html)
    
**NOTE:** Whenever you need a program check [Chocolatey](http://chocolatey.org/) first. It is the best place to discover the most used programs by developers for any category.
Most of the programs are available for free.

## Configuration

- Make Notepad2-mod the default text editor
- Make Conemu the default cmd shell
- Desktop Info (install and configure.) Add to startup
- Add computer to desktop
 
Install Chrome Extensions and Chrome Apps:
 
Check the "Chrome Extensions"  and "Chrome Apps" sections [here](http://orcomp.github.io/Blog/useful/2014/04/20/Useful-Tools.html).
 
Files and Folder:
 
- [Folder Organisation](http://www.howtogeek.com/howto/15677/zen-and-the-art-of-file-and-folder-organization/)
- [Application Launcher](http://www.howtogeek.com/howto/11166/use-quick-launch-as-a-super-powered-application-launcher/)

### Antivirus

The default anti virus that comes with Windows 8.1 is good enough if you surf the web sensibly.

### Partitions

Since the OS will be going on a SSD drive no need to partition.

## Notes

I started this Boxstarter project to run windows in VirtualBox with a linux host ([Manjaro](http://manjaro.org/)).
Unfortunately the VM is not fast enough on my laptop so I went the other way. Installed windows 8.1 as the host and Manjaro as guest.

This actually makes sense since Windows requires a lot more resources than Linux. Manjaro with VBox actually runs very fast and does not use a lot of resources.

- ConEmu can be set to replace cmd.exe, which I highly recommend. http://superuser.com/questions/509642/how-to-change-the-default-terminal-emulator-on-windows-cmd/509710#509710
  (If you are not sure about ConEmu then read this: http://stackoverflow.com/questions/60950/is-there-a-better-windows-console-window/10904494#10904494)
- Notepad2-mod can be set to replace notepad. http://www.flos-freeware.ch/doc/notepad2-Replacement.html
  Notpead2-mod is a very capable editor, and opens up files realy fast.
- Conky for Windows is called "Desktop Info" http://www.glenn.delahoy.com/software/

## Todo

- Find an easy way of remapping AppData and Documents folder to somewhere else.

## Official Software List

- I keep this list up to date: http://orcomp.github.io/Blog/useful/2014/04/20/Useful-Tools.html
 
 
