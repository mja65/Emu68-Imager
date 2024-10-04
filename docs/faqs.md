# FAQs

### What are some important things I should know?
- ROM files MUST be from the A1200 and NOT the A4000
- There must be enough space on the work partition if you want to transfer your own files. 
- FILENAMES do not MATTER, the tool inspects file contents to identify the needed resources.

### I have a KickStart ROM for AmigaOS **3.1** but the tool cannot find or check it
As stated in the documentation you need a 3.1 Kickstart ROM for the **A1200** - not the A4000 model. 
Please check again exactly which Kickstart roms are supported [here](instructions.md#kickstart-rom-files). 
Make sure you use **single file** and **unencrypted** ROM variants as those are the ones currently supported.

### The tool cannot find or check my Kickstart ROM image for **3.2 or 3.2.2.1**
- For **3.2** select the **ROM/** directory on your **OS 3.2 CD** and click the **Check** button.
- For **3.2.2.1** extract the file **A1200.47.111.rom** from the **Hotfix3.2.2.1.lha** (inside the **Update3.2.2/ROMs/** directory) to a directory of your choice and select that. Then click **Check** button.
- Make sure you use **single file** and **unencrypted** ROM variants, as they are the only ones currently supported.

### The tool cannot find or check my AmigaOS 3.1 ADFs
These ADF files **must** be **UNMODIFIED and Original** copies of the Workbench 3.1 install floppies. The imager tool only supports unmodified versions since changes may introduce incompatibilities which break the automatic install system. 
There are several different versions of the AmigaOS 3.1 Workbench out there (originally from Commodore, later on sold with Escom Amigas and now sold by Cloanto and their Amiga Forever package) - All of these official versions are supported.

### The tool cannot find or check my AmigaOS 3.2.2.1 ADFs.
- There is a directory **UserFiles** created (with **ADFs/** directory inside it) when you first run the Tool.
- Copy all files from your **OS 3.2 CD** (from the **ADF/** directory) to **UserFiles/ADFs/**.
- Copy all files from **Hotfix3.2.2.1.lha** (from the **Update3.2.2/ADFs/Update/** directory) to **UserFiles/ADFs/**.
- Copy the **Update3.2.2.1.adf file** from **Hotfix3.2.2.1.lha** (in the **Update3.2.2/ADFs/Hotfix/** directory) to **UserFiles/ADFs/**.

> <font color="red">When copying files, you should overwrite older versions with newer update and hotfix files when prompted.</font>

- Press **Check** button, it should turn Green if all steps were completed correctly.

### It's nice there is a GUI to start, but the running of the tool is in the Terminal. Why?

The tool is written in Powershell. Limitations in Powershell (and frankly the knowledge of the coder) make a graphical output difficult. Two examples:

1. Downloads of the various packages uses standard Powershell functionality. Showing progress for downloads either requires using the standard Powershell output or there is no output whatsoever

2. Updating progress to a Window is possible, but introduces significant delay in order for Powershell to update the window. "Significant" delay means in some circumstances the tool would take twice as long to run versus what it does now. 

In summary, functionality over aesthetics.

### The tool is looking for ADFs I do not have! 

This tool is provided for users who have legally acquired versions of the ROMs and ADFs. If you do, you should have no issue accessing the required files (e.g. using the Hyperion website to download any updates).

If you've chosen to "sail the high seas" that's your choice but you will need to work out how to acquire the complete set. It is not something we can point you towards

### I've written the image but [wifipi.device / videcore (RTG) / Buptest / (any other Emu68 software)] is not working!

The tool is using the currently available version of Emu68 and Emu68 tools. By all means, reach out for support but please consider if your issue relates to the imager or Emu68. If the later, then it is not something the tool can resolve.  However, please raise the issue in the appropriate forum if you encounter it (e.g. the emu68-support channel on Discord)

### How do I upgrade from the demo version of Roadshow to the full version?

If you have the full version of Roadshow, copy the bsdsocket.library from the install package to the Libs folder on the Workbench drive. You can either use the option to transfer files when you run the tool (please refer to the [Supplying your own additional files](#supplying-your-own-additional-files) section) or copy the files to the FAT32 partition.

### Why is [Insert your favourite Amiga package name] not installed?

The tool is intended to provide a basic image to help you get started, to avoid common pitfalls such as RTG and internet issues and using 100% legally acquired software. Once you have a basic set up you have access to the internet as well as a suitably sized SD card where you can transfer whatever you need to add additional software. 

It can be a rewarding experience learning about how to install software on your Amiga. However, if you are after a fully set up and customised distribution with all games and applications pre-installed and where you can write an image to a SD card and just use it then you should download and use one of those.

### Where is the Linux/Mac version?
Short answer: There is none.

Longer answer: The GUI is built using WPF (Windows Presentation Foundation), which as the name suggests, is Windows specific. More importantly, while Powershell (the main language the tool is written in) is supported on Mac and Linux, some of the tools used are not. As an example, 7zip is used to extract LHA archives and this is not available on either Mac or Linux. Unfortunately the Unlha tools themselves have certain limitations. It also makes direct changes to the physical device meaning WINE or similar will not work. 
