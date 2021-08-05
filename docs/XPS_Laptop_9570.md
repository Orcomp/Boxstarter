# Re-install Windows XPS 15 9570

A lot easier than I initially thought.

- Download the Windows media creation tool (https://www.microsoft.com/en-au/software-download/windows10), which will help setup a Windows 10 installation image on a USB stick.
- Plug the USB stick into the laptop. (Do not make any changes to the BIOS or settings)
- Start up the laptop and hold the F12 button down to access the BIOS settings.
- Select the USB stick option and continue. (Yes it is that simple...)
- Go though the installation process. At some stage you will need to repartition the hard drive. Delete all the partitions so that only one line is left and then click "Next". (i.e. do not click on "New").
- Once Windows 10 is installed you will have to install the drivers.
- Run the "UpdateWindows.txt" script, which will also install the "Dell Command | Update" application. Use this to install all the drivers, from the Dell support page. After installing drivers reboot the computer.
- Install Dell Command update


## Color Saturation

- Download "Dell Premiercolor" and go through the wizard.

## Fan issue

- Only use CPU graphics (disable NVIDIA GPU using the "NVIDIA Control panel" application)
- I wonder whether not installing the NVIDIA driver would fix this permanently in the first place...

**Other solutions:**

Here are other solutions I found online while doing this research. I haven't tried them yet. (Haven't had to...)

- Install "Dell Power Manager" from the windows store: Set to quiet
- https://www.dell.com/community/XPS/XPS-9370-Fan-Noise/td-p/5803616/page/17
- https://communities.intel.com/thread/115794
- https://www.reddit.com/r/Dell/comments/5y3rii/xps_9560_battery_life_optimization_and_fan/

## DPI issues on external monitor

Visual Studio and other apps not rendering properly.

Short answer: Make the external monitor the primary monitor.

- https://developercommunity.visualstudio.com/content/problem/25097/font-is-blurry-due-to-not-supporting-mixed-mode-dp.html
- https://www.danantonielli.com/adobe-app-scaling-on-high-dpi-displays-fix/

## BIOS changes

- System Configuration / SATA Operation = AHCI
- System Configuration / Keyboard illumination = Dim
- System Configuration / Touchscreen = off
- Power Management / Primary battery charge configuration = Primary AC use

## Black screen flicker issue

- Disable "refresh" in Intel Graphics, under the performance tab
- https://www.reddit.com/r/Dell/comments/8wy79o/black_screen_flicker_on_dell_xps_15_9570/

## Other

- Undervolting: https://www.notebookcheck.net/Intel-Extreme-Tuning-Utility-XTU-Undervolting-Guide.272120.0.html

  - Install intel XTU
  - Cache voltage offset: -160mV
  - Graphics offset: -35mV

- RAM upgrade: https://www.windowscentral.com/best-dell-xps-15-9570-compatible-ram
- RAM upgrade "how to" guide: https://www.windowscentral.com/how-add-more-ram-dell-xps-15-9570

https://www.dell.com/community/XPS/LAPTOP-FAN-CONTROL/m-p/6055828#M9486
https://www.dell.com/community/XPS/Extreme-fan-noise-on-XPS-9570/td-p/6095873

- Find out if we can disable the NVIDIA graphics completely from the BIOS

# Troubleshooting

## Flickering black screen issue

- Use the latest driver version from INTEL.
- How to uninstall the Dell version?

https://www.dell.com/support/article/au/en/aubsd1/sln305754/xps-9560-precision-5520-black-screen-or-flickering-issue?lang=en
https://www.dell.com/community/Laptops-General-Read-Only/XPS-9560-Screen-flicker/td-p/5126096/page/32
https://www.reddit.com/r/Dell/comments/8wy79o/black_screen_flicker_on_dell_xps_15_9570/

## Replacing SSD

- Samsung 970 PRO
- https://www.windowscentral.com/upgrade-ssd-dell-xps-15-9570

Enable AHCI? (See the link above)

## Replacing Wifi card

- Intel 9260
- https://www.youtube.com/watch?v=gQTKBGoz35k
- https://www.reddit.com/r/Dell/comments/8n1orj/replacing_the_killer_1535_wifi_in_xps_9570_with/

## Temperature issues

- https://www.ultrabookreview.com/14875-fix-throttling-xps-15/