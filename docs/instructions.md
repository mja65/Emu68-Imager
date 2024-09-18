# Instructions

[Quick Start](#quick-start)

[Emu68 Imager tool instructions](#emu68-imager-tool-instructions)

[Amiga Utilities instructions](#amiga-utilities-instructions)

When you start the Emu68 Imager you will be presented with the options screen:

![Emu68 Imager Screenshot](images/screenshot1.png)

The **Run Tool** button will be red until you select the required options. When you select those it will turn green and you can press it.

# Quick Start

If you want to quickly create an image for your Pistormed amiga then you can leave most things on their default setting and do the following:
- Insert your SD card in your SD card reader
- If you inserted the SD card after the tool was run then press the **Refresh Available Media** button
- Select the desired SD card from the drop down control
- Select the desired OS version
- Copy the Kickstart ROM and all installation ADF floppy images to a folder on your disk (refer to [ADF Images](#adf-images) section)
- Select the Kickstart folder by clicking on **Click to set Kickstart Path** button
- Select the ADF Images folder by clicking on **Click to set ADF Path** button
- Select the Screen Mode of your HDMI monitor in the drop down box
- The button **Run Tool** should turn green if there was enough space on your disk
- Press the **Run Tool** button and follow the popup windows to start the tool
- It will take some time for all utilities to be downloaded and image written

# Emu68 Imager tool instructions

The tool has several sections. You will need to select options in each section for the tool to be able to run. When everything that is mandatory is selected the **Run Tool** button will turn green and you can continue with the image creation.

At any time you can click on **Click for Documentation** button which will show this instructions in your default browser.

## Selecting SD card

You can insert the SD crd before you start the tool. If you insert the SD card or change it while the tool is running you have to press the  **Refresh Available Media** button so the drop down box is refreshed.
Select the desired SD card from the **Select Media to use** drop down box. When you do so the partition bar will change according to the capacity of the SD card. 

If you change the default sizes of the partitions then the **Reset Partitions to default** button will reset the partitions to their default values as if you selected the SD card for the first time.

## Selecting Parititon sizes

The tool will set the partition sizes to some reasonable default values. You can change any partition size to your liking. To resize a partiton you can click on the desired bar and drag it left/right to resize or you can enter the desired values in the text boxes below the bar. If you enter invalid values the text box background will turn red.
If you want to resize Fat32 or Workbench partitions then you will have to first *shrink* the Work partition (the Work partition gets most space by default). This will give you some **Not Used** space and you can resize other partitions to your liking.
There are 5 parts on the partition bar:

### Fat32

This is the boot partition for the raspberry Pi. It contains the Emu68 image and all necessary files for it to function. Additionally it contains the following:
- Kickstart image for your Amiga
- config.txt file with configuration of your pistorm and raspberry Pi
- cmdline.txt file with configuration of the Emu68
- Kickstarts folder to which you can copy the Kickstarts you want to use with WHDLoad games and demos
- Packages folder to which you can copy Install Packages for the Emu68 Imager tool package installer

The Fat32 partition can be upto 4GB big. The tool selects the default size according to the capacity of the SD card. 

### Workbench

This is the boot partition for your Amiga. It will contain the Workbench installation and all tools and utilities that are necessary.
In addition to the installation folders that are installed with the OS you chose there are the following two folders created:
- Pistorm - contains all tools associated with Pistorm and Emu68
- Programs - contains essential utilities that we thought will benefit the user on clean install

Please refer to [Amiga Utilities instructions](#amiga-utilities-instructions) about the content of these two folders.

The Workbench partition can be upto 100Gb big. The tool selects the default size according to the capacity of the SD card. 

### Work

The Work partition is the one that will use up most of the capicity of your SD card. It should be used to install any programs for your Amiga.
You can populate some (or all) of it using the Imager tool from the start. Please refer to the [Transfer Files to Work Partition](#transfer-files-to-work-partition) section on how to do that. If you don't populate it using this functionality then it will be empty.

The Work partition will by default take up all the remaining capacity of your SD card. Since the PFS3 partitions on the amiga can only be upto 100GB in size the tool will create multiple Work partitions if your SD card has more capacity. Only the first Work: partition will be formatted, you will need to format the rest yourself on the amiga. Please refer to [First Time Run](#first-time-run) section on how to do that.

### Free Space

The Free Space is the space that will be avaialble as "Free" on your amiga - HD Tool Box will be able to repartion and use it as you wish.
It is recommended to resize your Work partition so that there is no Free Space since the *free space* WILL be written to your SD card (it will take time to write it).

### Not Used

The Not Used is the part of the SD card that will not be touched and it will NOT be available on your amiga. If you would like to have smaller image on the amiga and have some free space which you can Repartion on your windows (to have another Fat32 or NTFS volume for PC use for example) then please use this *not used* space for it.


# Amiga Utilities instructions

test text 2
