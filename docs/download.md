The latest version of Emu68 Imager can be found at the following link:

[https://mja65.github.io/Emu68-Imager/Software/Emu68Imager.zip](https://mja65.github.io/Emu68-Imager/Software/Emu68Imager.zip)

The latest version is currently 1.0.2. Changes since 1.0 are:

1.0.2

- A check for and a message will be displayed if the .HDF file created is then locked for access by another process. 
- The sequencing of the ADF files searched for has been changed to reflect some omissions noted in some of the Escom disks for 3.1.
- Accessing files FROM the network should work for mapped network drives. It will not work for UNC links (those starting with double backslash - servername) due to limitations in HST-Imager.
- There is also a check to prevent a user from  select a network path for the working folder as this will not work 

1.0.1

- Added check for whether the .hdf file is locked after creation to try to address if antivirus/anti-malware programs have locked the file for access
- Added messagebox at the conclusion of the tool running to alert the user the tool has successfully completed
- Removed the 7 Cities of Gold RTB file from the Install Packages

