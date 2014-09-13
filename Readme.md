Boxstarter scripts to setup a dev environment on a new windows box.

## Goal:

- Keep it lean
- Keep it simple

There is a two step process, some large installs like VS, SQL server etc.. are done manually.


## Introduction

- The boxstarter list only containts software I use regularly. Nothing more.
- The boxstarter links to use in IE are found at the top of each file.
- The order in which the files should be run are:
    1. UpdateWindows.txt (Run this just after installing windows.)
    1. InstallSotware.txt
    1. PostInstall.txt
    
**NOTE:** Whenever you need a program check [Chocolatey](http://chocolatey.org/) first. It is the best place to discover the most used programs by developers for any category.
Most of the programs are available for free.
    
## Steps

After running the scripts mentiond above run the following programs

1. [Simple System Tweaker](http://www.tweaking.com/content/page/simple_system_tweaker.html) or download and install [Ultimate Windows Tweaker](http://www.thewindowsclub.com/ultimate-windows-tweaker-3-windows-8)

    
## Observations

I started this Boxstarter project to run windows in VirtualBox with a linux host ([Manjaro](http://manjaro.org/)).
Unfortunately the VM is not fast enough on my laptop so I went the other way. Installed windows 8.1 as the host and Manjaro as guest.

This actually makes sense since Windows requires a lot more resources than Linux. Manjaro with VBox actually runs very fast and does not use a lot of resources.


### Antivirus

The default anti virus that comes with Windows 8.1 is good enough if you surf the web sensibly.


### Partitions

Since the OS will be going on a SSD drive no need to partition.

Instead I create some folders on C:\ to save my data.

[Folder Organisation](http://www.howtogeek.com/howto/15677/zen-and-the-art-of-file-and-folder-organization/)
[Application Launcher](http://www.howtogeek.com/howto/11166/use-quick-launch-as-a-super-powered-application-launcher/)

## Todo

- Find an easy way of remapping AppData and Documents folder to somewhere else.

## Notes

- ConEmu can be set to replace cmd.exe, which I highly recommend. http://superuser.com/questions/509642/how-to-change-the-default-terminal-emulator-on-windows-cmd/509710#509710
  (If you are not sure about ConEmu then read this: http://stackoverflow.com/questions/60950/is-there-a-better-windows-console-window/10904494#10904494)
- Notepad2-mod can be set to replace notepad. http://www.flos-freeware.ch/doc/notepad2-Replacement.html
  Notpead2-mod is a very capable editor, and opens up files realy fast.
- Conky for Windows is called "Desktop Info" http://www.glenn.delahoy.com/software/


## Software List

  - I keep this list up to date: http://orcomp.github.io/Blog/useful/2014/04/20/Useful-Tools.html