# Amiga Utilities instructions

When the Imager finishes writing the image on your SD card you can insert it into the SD card slot of your RaspberryPi.<br>
After turning your Amiga onm you should see the Emu68 Logo on your HDMI output.<br>

## First Time Run

Ideally, (but it is not essential), the  Amiga should have both a HDMI monitor and standard Amiga monitor connected since both are used on the First run!<br>
The first time the SD card is run there will be several additional things done :

## Buptest

Buptest is a test performed by Emu68 to check that the PiStorm is functioning properly. On your HDMI output you will see several lines of output. If all is well the test should be successful and your Amiga will continue booting the Emu68. From now on the output will be on your normal Amiga monitor output. Therefore if you do not have a HDMI monitor connected you will not see this message. <br>

After the Amiga succesfully boots into Workbench the first time it will disable Buptest since it is not needed anymore and it only slows the boot process down.

## Workbench finalization

There are several scripts run to finalize the installation of Workbench including:
- Setting PAL/NTSC monitors
- Setting HDToolBox and Fat32 partition driver according to your RaspberryPi (rPi3/4)
- Deletion of unecessary libraries
- Setting up iBrowse, PFS3
- Tidying up Icon positions

## Locale preferences

You will also be asked to setup your Locale preferences. This is important for the clock to be set correctly when you go online (which is a requirement for accessing https sites).

## Additional settings after Workbench first boots

## RTG Screenmodes

We have provided a Picasso96 settings file with a lot of useful resolutions pre-set for you. Just run the ScreenMode preferences and set any resolution you like. It will display on your HDMI display. Workbench will be much snappier and you will be able to enjoy millions of colours. We have also installed PeterK's icon library that takes advantage of all these colours so you can install PNG icons in all their glory.

## Formatting of extra Work partitions

If your SD Card is bigger than 100GB and you set up Work partition to be bigger than 101GB (the maximum PFS supports) then it will be split into additional partitions. The first partition named Work: is already formatted, but you will need to format the rest yourself. Just select the **Non Initialized** partition icon and on the right click Icons menu select Format disk, then follow the instructions and format the partition.

---

# Pistorm utilities and features included

Besides the usual Workbench Tools, Utilities and System Programs we also included all necessary and usefull **Pistorm** utilities and also a selection of **Programs** that will help you with the Pistorm and Emu68 startup.<br>
Both are placed in the same named folders on Workbench: partition.

# Pistorm tools

The included tools will make sure you can monitor the status of Emu68, adjust all possible settings, start,stop and configure WiFi and more.

## EmuControl

An essential utility to control everything Emu68 related. You can adjust how JIT performs, setup Debug options and see some of the properties like temperature.

## VC4Tweak

Lets you tweak the RTG graphics output with filtering options. If you want the settings to be used next time you reboot then you have to edit the Devs/Monitors/Videocore tooltypes accordingly.

## Online / Offline / WiFi Config

If you setup WiFi SSID and Password before you can click on Online icon and your Amiga should get online.<br>
The installation is using a demo version of Roadshow TCP/IP stack which will let you be online for up to 15 minutes after which you have to reset your Amiga. <br>
Clicking the Offline icon will stop the TCP/IP stack and you will get offline again. However, due to limitations in the demo version of Roadshow you may need to reboot your Amiga to go back online. We encourage you to consider buying the full version of Roadshow which does not have these limitations. <br>

If you didn't setup the WiFi SSID and Password before (or you want to change it) then you can use the **WiFi Config** icon which will let you edit the wifipi.device configuration file.

## Emu68Meter and Emu68Info.r

These two utilities will display the status of the Emu68 and give you information on raspberryPi used.

## SMB Config

**SMB Config** icon will bring up the configuration file for the included Samba driver. You can enter the connection string to your Samba share on the bottom file. If you want to mount the Samba share then you need to go into Storage/DOSDrivers folder and double click the SMB0 icon or you can use the MountSMB button in Directory Opus (right clicking on the same button will unmount the Samba share volume).

## TransferKick

If you want to use WHDLoad Games and/or Demos then you will need to have kickstart ROM files present in the Devs/Kickstarts drawers. We have provided a script that will make it easier for you to copy proper kickstart files automatically to the folder from the FAT32 partition.<br>
You can copy all your kickstart rom files into folder named Kickstarts on the FAT32 partition. After you boot your amiga click on the **TransferKick** icon and a script will check for all suitable kickstart rom files and copy them to Devs/Kickstarts for you.

## InstallPackages

This script can install custom packages that you have in the Fat32 partition **Install** folder. In the future we will have packages available that you can install for free. Just copy the Package (it is an .lha file) into the Install folder, boot your Amiga and double click **InstallPackages** icon.  Please refer to the [Additional Packages](packages.md) section of the documentation for further information.

---

# Programs

In addition of Pistorm tools we also installed a few essential and useful programs for you.

## Directory Opus 4

This is one of the more commonly used  file commander tools on the Amiga. It is the daddy of all double-panel browsers and Amiga installation cannot be without one. We have also provided additional functionality like archive extraction for you so you are all set up and good to go.

## IBrowse (demo)

Demo version if the web browser for amiga. It is essential that you have it, if you use it a lot you are encouraged to buy the full version. Documentation included with the installation uses IBrowse for display. You should be able to navigate Aminet without any problems now.

## SnoopDOS

Utility that lets you see what amiga is doing. Essential to debug problems and find out what your system is missing.

## HippoPlayer

An essential module (and much more) player that is still being developed. Latest version will be installed for your convenience.

## SysInfo

The most commonly used program to display how fast your Amiga is and what is inside.

## AmiSpeedTest

When you get Online you will want to see how fast your transfer rate is gonna be. Use this and you will find out.

## Jano Editor

A free and feature-rich Editor. Especially on OS 3.1 you will need it!

## AmiSSL, Picasso96, MUI

We have installed these so you don't have to set them Up.

Please refer to [What's Included section](included.md) to see where the tool downloads these programs and their documentation.
