# Amiga Utilities instructions

When Imager finishes writing the image on your SD card you can insert it into the SD card slot of your RaspberryPi.<br>
After turning your amiga on you should see the Emu68 Logo on your HDMI output.<br>

## First Time Run

The Amiga should have both HDMI monitor and standard Amiga monitor connected, since both are used on the First run!<br>
First time the SD card is run there will be several additional things done :

## Buptest

Buptest is a test performed by Emu68 to check that the pistorm is functioning properly. On your HDMI output you will see several lines of output. If all is well the test should be succesfull and your Amiga will continue booting the Emu68. From now on the output will be on your normal Amiga monitor output.

## Workbench finalization

There are several scripts run to finalize the installation of Workbench including:
- Setting PAL/NTSC monitors
- Setting HDToolBox and Fat32 partition driver according to your RaspberryPi (rPi3/4)
- Deletion of unecessary libraries
- Seting up iBrowse, PFS3
- Tidying up Icon positions

## Locale preferences

You will also be asked to setup your Locale preferences. This is important for Clock to be set correctly when you go online.

---

# Pistorm utilities and features included



