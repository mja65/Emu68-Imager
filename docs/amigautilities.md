# Amiga Utilities instructions

When Imager finishes writing the image on your SD card you can insert it into the SD card slot of your RaspberryPi.<br>
After turning your amiga on you should see the Emu68 Logo on your HDMI output.<br>

## First Time Run

The Amiga should have both HDMI monitor and standard Amiga monitor connected, since both are used on the First run!<br>
First time the SD card is run there will be several additional things done :

## Buptest

Buptest is a test performed by Emu68 to check that the pistorm is functioning properly. On your HDMI output you will see several lines of output. If all is well the test should be succesfull and your Amiga will continue booting the Emu68. From now on the output will be on your normal Amiga monitor output.<br>

After the amiga succesfully boots into Workbench it will disable Buptest since it is not needed anymore and it only slows the boot process down.

## Workbench finalization

There are several scripts run to finalize the installation of Workbench including:
- Setting PAL/NTSC monitors
- Setting HDToolBox and Fat32 partition driver according to your RaspberryPi (rPi3/4)
- Deletion of unecessary libraries
- Setting up iBrowse, PFS3
- Tidying up Icon positions

## Locale preferences

You will also be asked to setup your Locale preferences. This is important for Clock to be set correctly when you go online.

---

# Pistorm utilities and features included

Besides the usual Workbench Tools, Utilities and System Programs we also included all necessary and usefull **Pistorm** utilities and also a selection of **Programs** that will help you with the Pistorm and Emu68 startup.<br>
Both are placed in the same named folders on Workbench: partition.

# Pistorm tools

The included tools will make sure you can monitor the status of Emu68, adjust all possible settings, start,stop and configure WiFi and more.

## EmuControl

Essential utility to control everything Emu68 related. You can adjust how JIT performs, setup Debug options and see some of the properties like temperature.

## VC4Tweak

Lets you tweak the RTG graphics output with filtering options. If you want the settings to be used next time you reboot then you have to edit the Devs/Monitors/Videocore tooltypes accordingly.

## Online / Offline / WiFi Config

If you setup WiFi SSID and Password before you can click on Online icon and your Amiga should get online.<br>
The installation is using a demo version of Roadshow TCP/IP stack which will let you be online for 15 minutes after which you have to reset. <br>
Clicking the Offline icon will stop the TCP/IP stack and you will get offline again.<br>

If you didn't setup the WiFi SSID and Password before or you want to change it then you can use the **WiFi Config** icon which will let you edit the wifipi.device configuration file.

## Emu68Meter and Emu68Info.r

These two utilities will display the status of the Emu68 and give you information on raspberryPi used.

## SMB Config

**SMB Config** icon will bring up the configuration file for the included Samba driver. You can enter the connection string to your Samba share on the bottom file. If you want to mount the Samba share then you need to go into Storage/DOSDrivers folder and double click the SMB0 icon.

## TransferKick

If you want to use WHDLoad Games and/or Demos then you will need to have kickstart ROM files present in the Devs/Kickstarts drawers. We have provided a script that will make it easier for you to copy proper kickstart files automatically.<br>
You can copy all your kickstart rom files into folder named Kickstarts on the FAT32 partition. After you boot your amiga click on the **TransferKick** icon and a script will check for all suitable kickstart rom files and copy them to Devs/Kickstarts for you.

## InstallPackages

This script can install custom packages that you have in the Fat32 partition Packages folder. In the future we will have packages available here that you can install for free. Just copy the Package (it is an .lha file) into the Packages folder, boot your amiga and double click **InstallPackages** icon. 

# Programs

In addition of Pistorm tools we also installed a few essential and usefull programs for you.

## Directory Opus 4

This is the most used file commander used on amiga. It is the daddy of all double-panel browsers and Amiga installation cannot be without one. We have also provided additional functionality like archive extraction for you so you are all set up and good to go.

## IBrowse (demo)

Demo version if the web browser for amiga. It is essential that you have it, if you use it a lot you are encouraged to buy the full version. Documentation included with the installation uses IBrowse for display. You should be able to navigate Aminet without any problems now.

## SnoopDOS

Utility that lets you see what amiga is doing. Essential to debug problems and find out what your system is missing.

## HippoPlayer

Essential module (and much more) player that is still being developed. Latest version will be installed for your convenience.

## SysInfo

The most commonly used program to display how fast your Amiga is and what is inside.

## AmiSpeedTest

When you get Online you will want to see how fast your transfer rate is gonna be. Use this and you will find out.

## Jano Editor

A free and feature-rich Editor. Especially on OS 3.1 you will need it!

## AmiSSL, Picasso96, MUI

We have installed these so you don't have to set them Up.

Please refer to [What's Included section](included.rb) to see where the tool downloads these programs and their documentation.
