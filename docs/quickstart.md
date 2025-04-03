# Quick Start

When you start the Emu68 Imager you will be presented with the options screen:

![Emu68 Imager Screenshot](images/screenshot1.png)

The `Run Tool` button will remain red until you select the required options.
Options that are mandatory are the SD Drive to write to, The OS version you intend to install, your desired screen mode for the RTG driver, and the paths to both the system ADF images and your Kickstart ROM image.
Bear in mind that if you are installing AmigaOS 3.2.2.1 or 3.2.3, you will need both the base 3.2 ADFs as well as the hotfix/update ADFs in the same folder.

---

If you want to quickly create an image for your Pistormed amiga then you can leave most things on their default setting and do the following:
- Insert your SD card into an SD card writer. If you do this after you have first launched the tool, then press the `Refresh Available Media` button.
- Select the desired SD card from the drop down control.
- Select the desired OS version - currently 3.1, 3.2, 3.2.2.1 and 3.2.3 are available.
- Ensure the Kickstart ROM and all installation ADF floppy images are in folders on your disk or have been copied to the default folder (refer to [Supplying Kickstart ROM and Workbench installation floppy images (.ADF files)](instructions.md#supplying-kickstart-rom-and-workbench-installation-floppy-images-adf-files) section).
- If you have not used the default folder, select the Kickstart folder (can be the same as the ADF folder) by clicking on `Click to set Kickstart Path` button. Click the `Check` button to validate you have the correct files.
- If you have not used the default folder, select the ADF Images folder (can be the same as the Kickstart folder) by clicking on `Click to set ADF Path` button. Click the `Check` button to validate you have the correct files.
- Select the Screen Mode of your HDMI monitor in the drop down box (assuming you do not want the default option of Automatic).
- If the `Run Tool` button remains red then you have not set the required options. Pressing this button when red will inform you of which options you have missed.
- The `Run Tool` button should turn green if there was enough space on the disk you launched from. If you have insufficient space, the button will turn yellow and give you the opportunity to select a different drive. Bear in mind that you will need enough space available for the entire image - which can get quite large for bigger SD cards.
- Press the green `Run Tool` button and follow the popup windows to start the tool. A console window will open showing you the current progress.
- It will take some time for all utilities to be downloaded and image written. The console window will show progress. 
