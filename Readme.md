# Boxstarter scripts

This repository contains boxstarter scripts to help setup a dev environment on a new windows box.

There is a two step process, some large installs like VS, SQL server etc.. are done manually.

You can run the scripts multiple times. If a program is already installed it will just be skipped.

## Introduction

- The boxstarter list only contains software I use regularly.
- The boxstarter links to use in IE are found at the top of each file.
- The order in which the files should be run are:
    1. Update BIOS (for new installs)
    1. **UpdateWindows.txt** (Run this just after installing windows.)
    1. Install drivers (for new installs)
    1. **InstallSoftware.txt**
    1. Install large programs (VS, Office etc...) separately
    1. **PostInstall.txt**
    1. **UpdateWindows.txt** (Run windows update again.)
    1. Run CCleaner and KCleaner to get rid of all the junk. (These are installed in the scripts above)
    1. Run [Simple System Tweaker](http://www.tweaking.com/content/page/simple_system_tweaker.html)

**NOTE:** Whenever you need a program check [Chocolatey](http://chocolatey.org/) first. It is the best place to discover the most used programs by developers for any category.
Most of the programs are available for free.

## Configuration

- Make Notepad2-mod the default text editor: http://www.flos-freeware.ch/doc/notepad2-Replacement.html
- Install Chrome Extensions and Chrome Apps: Check the "Chrome Extensions"  and "Chrome Apps" sections [here](http://orcomp.github.io/Blog/#docs/list_of_useful_software).
- Files and Folder:

  - [Folder Organisation](http://www.howtogeek.com/howto/15677/zen-and-the-art-of-file-and-folder-organization/)
  - [Application Launcher](http://www.howtogeek.com/howto/11166/use-quick-launch-as-a-super-powered-application-launcher/)

### Antivirus

The default anti virus that comes with Windows is good enough if you surf the web sensibly.

### Partitions

Since the OS will be going on a SSD drive no need to partition.

## Paid software

I generally try and use free or open source software as much as possible. So when I pay for something it is generally really worth it.

- [Directory Opus](https://www.gpsoft.com.au/)
- [bvckup2](https://bvckup2.com/)

## Official Software List

- I keep this list up to date: http://orcomp.github.io/Blog/#docs/list_of_useful_software