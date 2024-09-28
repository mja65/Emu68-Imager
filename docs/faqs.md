# FAQs

### Q: Why aren't there any FAQs in here?
A: Because everything is perfectly clear after reading the documentation
### Q: Where is the Linux/Mac version?
A: Short answer. There is none.

A: Longer answer. The GUI is built using WPF (Windows Presentation Foundation), which as the name suggests, is Windows specific. More importantly, while Powershell is supported on Mac and Linux, some of the tools used are not. As an example, 7zip is used to extract LHA archives and this is not available on either Mac or Linux. Unfortunately the Unlha tools themselves have certain limitations.