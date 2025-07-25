The latest version of Emu68 Imager can be found at the following link:

[https://mja65.github.io/Emu68-Imager/Software/Emu68Imager.zip](https://mja65.github.io/Emu68-Imager/Software/Emu68Imager.zip)

The latest version is currently 1.0.6.1 Changes since 1.0 are:

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

