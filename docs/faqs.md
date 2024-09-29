# FAQs

### Q: I cannot get KickStart ROM for **3.1** to check correctly
A: As stated in the documentation you need a 3.1 Kickstart ROM for A1200 model. Please check again exactly which Kickstart roms are supported [here](instructions.md#kickstart-rom-files)

### Q: I cannot get KickStart ROM for **3.2 or 3.2.2.1** to check correctly
A:
- For **3.2** select the **ROM/** directory on your **OS 3.2 CD** and click **Check** button
- For **3.2.2.1** extract the file **A1200.47.111.rom** from the **Hotfix3.2.2.1.lha** and its **Update3.2.2/ROMs/** directory to a directory of your choice and select it. Click **Check** button

### Q: I cannot get OS 3.1 ADFs to check correctly
A: You need to have **UNMODIFIED and Original** ADF copies of the Workbench 3.1 install floppies available. We can only support unmodified versions since we don't know what was changed on floppies that were modified. There are several different versions of 3.1 Workbench out there and we support all that we found. 

### Q: I cannot get OS 3.2.2.1 ADFs to check correctly
A:
- There is a directory **UserFiles** created (with **ADFs/** directory inside it) when you first run the Tool
- Copy all files from your **OS 3.2 CD** and its **ADF/** directory to **UserFiles/ADFs/**
- Copy all files from **Hotfix3.2.2.1.lha** and its **Update3.2.2/ADFs/Update/** directory to **UserFiles/ADFs/**  (IMPORTANT: **Overwite** any existing files !)
- Copy the **Update3.2.2.1.adf file** from **Hotfix3.2.2.1.lha** and its **Update3.2.2/ADFs/Hotfix/** directory to **UserFiles/ADFs/**
- Press **Check** button, it should turn Green if you did all steps correctly

### Q: Where is the Linux/Mac version?
A: Short answer. There is none.

A: Longer answer. The GUI is built using WPF (Windows Presentation Foundation), which as the name suggests, is Windows specific. More importantly, while Powershell is supported on Mac and Linux, some of the tools used are not. As an example, 7zip is used to extract LHA archives and this is not available on either Mac or Linux. Unfortunately the Unlha tools themselves have certain limitations.
