
### Re-install Windows XPS Tower 8930

Follow exactly the same steps as the XPS 9570.
No need to change anything in the BIOS. Leave Boot security and UEFI on. Insert the USB and reboot. Click F12 and choose to boot from USB.

Install:

- Drivers: https://www.dell.com/support/home/au/en/aubsd1/product-support/product/xps-8930-desktop/drivers
- SupportAssist
- Intel Toolbox (includes drivers for Optane 900P) (Installed by Chocolatey)
- Intel Rapid Storage
- Samsung Magician (Installed by Chocolatey)

### Other Settings

#### NVME M.2 slot

In order to get the NVME M.2 slot to work we need to use AHCI instead of RAID.

This is easy to do when following these steps:

- Run msconfig
- Enable Safe Boot (minimal)
- Reboot into BIOS and change to AHCI
- Boot into safe mode
- Run msconfig and disable safe boot
- Reboot

Then we need to format the new partition in order for Windows to see it in Explorer.