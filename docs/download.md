There are currently two version of the Emu68 Imager available. The latest version of Emu68 Imager can be found at the following Github repository page where you can download the latest release:

[Link to Github Repository Releases](https://github.com/mja65/Emu68-Imager-Software/releases)

The legacy version of the imager can be found at the following [link](https://mja65.github.io/Emu68-Imager/Software/Emu68Imager.zip):

The latest version of Emu68 Imager is 2.1.1.4.

The latest legacy version of Emu68 Imager is 1.0.6.5. Note, this version of the tool is not receiving updates.

Changes since 1.0 are:
2.1.1.4

-Update to fix issue where non-English Windows reported 64bit rather than 64-bit resulting in false detection of non 64 bit Windows

2.1.1.3

- Changed prerequisite check so ARM64 WIndows users were not excluded
- Changed DL for Whdloadwrapper to reflect changes on Turran FTP server

2.1.1.2

- Updates for Emu68 Updater to update Videocore.card file

2.1.1.1

- Updated WHDLoadWrapper function to include -UseBasicParsing parameter to suppress warning on newer versions of Powershell

2.1.1

- Updated Emu68 Updater to update Videocore.card as well as tooltype
- Fixed issue where incorrect version of Emu68info was being used from Emu68-tools repository
- Corrected typo in CheckScreenModeandChipset.rexx

2.1.0.1

- Fixed issue with missing text qualifiers
- Fixed issue with environment variable names for Pi3
- Fixed UI issue with loading settings

2.1

- Introduced selection of Screenmodes so user can select either Native or RTG screenmode to boot. All user interaction has been moved to after Workbench has loaded so users who have not connected native output should not be stuck at a black screen
- Introduced check so that if a user selects an unsupported screenmode the screenmode will revert to PAL Highres non interlaced
- Revised system detection in Startup-Sequence
- Removed unnecessary Onetimerun scripts
- Added Unicam parameters to cmdline to support Framethrower
- Updated Emu68 Imager to use the new Emu68-tools repository including the new Videocore.card file 
- Added latest version of HST Amiga (0.5.208)
- Added latest version of HST Imager (1.4.526)
- Changed icon positioning to use HST Amiga so no longer performed on first boot
- Changed Onetimestartup to allow for execution of scripts after workbench has loaded
- Added additional screenmode (1600*900) to Picasso96settings

2.0.4.2

- Fixed issue where user had Imager residing in a file path with spaces
- Restored buptest on first boot

2.0.4.1

- Fixed cosmetic issue with UI typo
- Fixed display issue with Disclaimer
- Bugfix for where conversion to integer was not always set
- Bugfix for where incorrect files might be copied in rare circumstances
- Bugfix for issue where creating .img files resulted in an error

2.0.4

- added Framethrower parameters to cmdline.txt
- added warning if running Windows in scaled mode since GUI will have issues 
- fixed issue where some input boxes in GUI were ignored
- updated to use latest version of HST imager
- fixed some issues where icon positioning wasn't always working (mainly 3.9)
- various other bug fixes

2.0.3

- Changed extraction process for ISOs to use HST-Imager rather than 7z to resolve issue where non-English characters were corrupted (affected install of OS3.9)
- Removed unrequired code relating to generation of the onetime run script to set PFS maximium filename size (HST Imager already does this)
- Revised handling of variables in Amiga scripts to ensure compatibility with OS3.9
- Changed check for out-of-date versions of Emu68 Imager to make message more prominent and to include link to Download page
- Revised code for checking whether image can be generated
- Changed Reset to default so that users who have chosen to remove the Workbench partition do not need to restart Emu68 Imager should they wish to reset the disk and start again
- Added additional handling to ensure that Amiga partitions were actually deleted
- Removed unrequired function "Confirm-HSTNoErrors"
- Updated function to remove extraneous message to terminal
- Updated "Copy-ArchiveinArchiveFiles" function so that log file is written to the correct temporary folder
- Added additional tooltips to the GUI (i.e. hovering over fields provides explanation to the user)
- Amended name of onetimescript for determining model of Raspberry Pi so loading image in WinUAE on first boot did not attempt to run 

2.0.2

- Added check for documentation site as part of start up checks
- Added parameters user selected when running Emu68 Imager to the log
- Changed the reporting of issues for connection to warnings from error messages
- Removed the onetime run script to set PFS maximium filename size (HST Imager already does this)
- Added error reporting if terminal window state cannot be changed
- Added checks so that the Imager does not write to a non existent variable when entering volume name in rare circumstances
- Fixed issue where Emu68 Imager occasionally exited when user changed selectable packages
- Corrected total number of tasks

2.0.1.1

- Fixed issue where FAT32 files were not beign copied when writing an .Img file


2.0.1

- Fixed issue where code was not always returning the Amiga partitions

2.0.0.2

- Fixed issue where user ran with no Workbench partition

2.0.0.1

- Fixed issue where backup server for WHDLoadWrapper was not always being used

2.0

- Complete rewrite of the code

New features include:
- Option to run in either Simple Mode or Advanced Mode so users can generate an SD card without needing to go through most of the configuration options
- Progress bar reporting when running tasks
- New User Interface with more modular design
- Ability for backup server location to be set for downloaded software
- Minor tweaks on Amiga environment
- Changes to config.txt so Pistorm16 support will work when Pistorm16 included as part of Emu68 Github Releases

Disk Set up
- Disk partitioning now works as proper disk partitioning so you can add/create/delete/move partitions rather than just resizing them
- Multiple 0x76 partitions can be created if you wish to use them
- Rather than a single Work partition you can have more than 1 (or none). All partitions will now be formatted rather than just the first one. You can use whichever device name and volume name you choose. Note, the Workbench partition currently remains with a fixed volume name and device name
- Ability to define settings on Amiga partitions as you can within HDToolbox (e.g. boot priority, buffers, device name, volume name, etc.)
- When writing to an image, in addition to .img files you can write to .vhd image files which only use as much space as the data contained within the image

Configuration of Image
- Option to select which icon set you wish to install (e.g. glowicons vs standard icons)
- Option to add/remove packages from install (e.g. language files)

Writing of Image
- Use of the latest version of HST Imager so no longer a need to write to an image before the image is then written to a disk (i.e. significant saving in temporary space needed particularly when writing large images)
- Significant performance improvements in speed of execution - this is impacted by the speed of your SD card as individual files are now written directly to the SD card which can be slower than writing a large image so your mileage will vary depending on the speed of your SD card, the number of files you are writing and the SD Card adapter used 

Also many "under the hood" changes too numerous to mention.

1.0.6.5

- Uopdated Github link for Emu68Tools

1.0.6.4
- Forced download of GeNet 1.3 (since 2.0 requires custom version of Emu68)
- Updated documentation links for download

1.0.6.3

- Changes to the Onlinescript to allow for use in menutools. Roadshow send and receive parameters are now stored in their own file.

1.0.6.2

- Bugfix for the Emu68-Updater script introduced in 1.0.6.1

1.0.6.1

- Bugfix for the Emu68-Updater script which would cause it not to work in rare circumstances

1.0.6

- Added genet.device for Ethernet connections for Pi4/CM4 users where Kickstart version >= 3.2
- Added Online script for genet.device
- Added Emu68-Updater by Shaytan so a user can check and automatically install updates to Emu68 when they are released 
- Added GUI Version of SMB Config by Shaytan
- Added GUI version of Wifi Config by Shaytan
- Added AreWeOnline by TomCat
- Added additional software from Aminet to support the above (CLICon, aget)

1.0.5.2

- Improved the Online script to better handle where connections do not work. Where connections have failed but WirelessManager remains connected, WirelessManager is closed so the log can be accessed on the Amiga (previously the log was inaccessible as WirelessManager locks the file). The logs for WirelessManager, AddInterface from Roadshow and sntp are all concatenated and written to RAM:WirelessLogs.Txt so the user can see all the information in one place for troubleshooting

1.0.5.1

- Added check for encrypted Cloanto Kickstart ROMs so the user is alerted if they have chosen this ROM since it will not work on PiStorm without being decrypted

1.0.5

- Added support for installing AmigaOS 3.9
- Fixed TransferKick to account for where there are no Kickstart files in the Kickstart folder
- Minor bug fixes

1.0.4.3

- Added functionality to support AmigaOS 3.2.3. 
- Revised Imager code to better allow for future versions of AmigaOS to be added without impacting previous versions of Emu68Imager

1.0.4.2

- Fixed some typos in the log created during execution and as reported in the terminal
- Added filter so versions of Emu68 >= 1.1 will not be downloaded. This is a temporary measure until this version is released and is supported
- Changed downloading of documentation to the Amiga so that if the download fails that the image will still be created

1.0.4.1

- Fixed issue with the Quicklink on the disclaimer window not working (thanks to Makedonk for identifying)
- Added check for 64bit OS so Imager will not start if 32bit version of Windows is used
- Corrected typo in FindFreeSpace command used in Powershell
- Added additional flag for the "Invoke-Webrequest" commands to improve compatibility (thanks to Czig for identifying issue and solution)

1.0.4

- Fixed issue with DOpus and Kickstart 3.1 where DOpus would search for drawer .info file in default 3.2 location that did not exist
- Updated install packages to include XPK (included in live updates)
- Added Picasso96 ENV "DisableAmigaBlitter" setting to prevent graphical corruption arising with the most recent PeterK icon.library version under Kickstart 3.1 and using a RGB Workbench screen where clicking on icons could result in graphical corruption  

1.0.3

- Fixed prioritisation of ADFs so that 3.1 ADFs are correctly prioritised (Commodore, then Cloanto, then Escom)
- Introduced check for latest version of input CSV files at start up to allow for updates without a new version of the tool being required
- Minor bug fixes (e.g. typos in terminal output, missing screenshot from documentation copied to image) 

1.0.2

- A check for and a message will be displayed if the .HDF file created is then locked for access by another process. 
- The sequencing of the ADF files searched for has been changed to reflect some omissions noted in some of the Escom disks for 3.1.
- Accessing files FROM the network should work for mapped network drives. It will not work for UNC links (those starting with double backslash - servername) due to limitations in HST-Imager.
- There is also a check to prevent a user from  select a network path for the working folder as this will not work 

1.0.1

- Added check for whether the .hdf file is locked after creation to try to address if antivirus/anti-malware programs have locked the file for access
- Added messagebox at the conclusion of the tool running to alert the user the tool has successfully completed
- Removed the 7 Cities of Gold RTB file from the Install Packages

