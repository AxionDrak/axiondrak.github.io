---
layout: default
---

# PSX/2 CNF Creator
* * *
**PSX/2 CNF Creator** is a small tool for creating _SYSTEM.CNF_ files compatible with PSOne (PS1) and PSTwo (PS2) consoles, being mainly used for disk homebrews.

## Images
* * *
![useful image]({{ site.url }}/assets/images/psxcnf/psx-cnf-01.png)![useful image]({{ site.url }}/assets/images/psxcnf/psx-cnf-02.png)![useful image]({{ site.url }}/assets/images/psxcnf/psx-cnf-03.jpg)

## Official Page on GitHub:
* * *
* [PSX/2 CNF Creator - GitHub](https://github.com/AxionDrak/PSX2CNFCreator)

## Downloads:
* * *
* ![useful image]({{ site.url }}/assets/images/zip-icon.png) [PSX/2 CNF Creator 1.3.1 - Stable](https://github.com/AxionDrak/PSX2CNFCreator/releases/tag/v1.3.1)

* ![useful image]({{ site.url }}/assets/images/zip-icon.png) [PSX/2 CNF Creator - Old Versions](https://github.com/AxionDrak/PSX2CNFCreator/releases)

* ![useful image]({{ site.url }}/assets/images/exe-icon.png) [Requires .NET Framework 4.5](https://www.microsoft.com/en-US/download/details.aspx?id=30653) (Web installer)

## Hash
* * *
Use the table below to ensure that downloaded files have not changed. These values are for the latest stable version in its compiled (final) version.

Version: 1.4.0

| Filename                 | MD5                              | SHA256                                                         
|:-------------------------|:---------------------------------|:---------------------------------------------------------------|
| LICENSE                  | e62637ea8a114355b985fd86c9ffbd6e | 230184f60bae2feaf244f10a8bac053c8ff33a183bcc365b4d8b876d2b7f4809
| PSX2CNFCreator.exe       | c08a278b477dd8d52da3c77759de0e40 | 912c5c37ccacbd220321944ad629f31cc257a27f106dac0c85d272ab4b0eef14
| README.md                | f68faaed59732675bd932ccf3d3dfa72 | 7ba72e34bf463ed30f47bbc88d7d3a7130fec61d4d6d3aaf78978219b9774700
| psxhelp.chm              | 1cc1f0ccbb29168d288863019a10f7f5 | 32980b3a6fc0f1baf16c37e2da9aebfe3e0880d3e19e5e93c09403263866fe1e
| PSX2CNFCreator_1.4.0.zip | 83a43b325ca267f68a691423de762f35 | aeae499657beead34f4f16bdb43b48df4a9b195496dae35ea3968ecfd4cf1181

## Features
* * *
* Supports create SYSTEM.CNF files _(PSOne and PSTwo)_
* Supports create SYSTEM.CNF files for OPL Mini *(PSTwo)*
* Supports any ELF file _(PSOne and PSTwo)_
* Supports any KELF file *(OPL Mini for PSTwo)*
* Supports file and program versioning _(PSTwo)_
* Supports PAL and NTSC video modes _(PSTwo)_
* Supports HDDUNITPOWER in NONE, HDD, NIC and NICHDD modes _(PSTwo)_
  - OPL mini support only HDD, NIC and NICHDD modes
* Supports TCB _(PSOne)_
* Supports EVENT _(PSOne)_
* Supports STACK _(PSOne)_
* Supports Dummy file creation _(gargabe)_
* Automatically corrects the file format SYSTEM.CNF
* CLEAR option added as facilitator
- Compatible _(tested)_ with the following operating systems:
  - Windows 7
  - Windows 8
  - Windows 8.1
  - Windows 10

## Languages
* * *
* At the moment, only Brazilian Portuguese is supported (sorry :/)

## SYSTEM.CNF
* * *
The structure of the SYSTEM.CNF file is different for PSOne and PSTwo consoles.

Below are examples of this file:

- SYSTEM.CNF _(PSOne)_
```
BOOT = cdrom:\MY_ELF.ELF;1
TCB = 4
EVENT = 16
STACK = 801FFFFC
```

- SYSTEM.CNF _(PSTwo)_
```
BOOT2 = cdrom0:\MY_ELF.ELF;1
VER = 1.0
VMODE = NTSC
HDDUNITPOWER = NICHDD (Optional)
```

- SYSTEM.CNF *OPL Mini Mode (PSTwo)*
```
BOOT2 = pfs:/EXECUTE.KELF
VER = B.99
VMODE = NTSC
HDDUNITPOWER = NICHDD
```

## Report Bugs
* * *
Verify that the bug is reproducible and still occurs in the latest version of SVN/Daily build.

Also check the list of known issues (below) to ensure the issue is not yet known:

Include the following information:
* PSX/2 CNF Creator version _(try the latest version of SVN/Daily build)_
* Bug details, including playback instructions
* Operating System _(Windows 7/8/8.1/10)_
* Attach an image if possible

## Known Issues
* * *
* No problem reported :)

## Changelog
* * *

`v1.4.0`
December 08, 2019
* Added support for OPL Mini (OPL Mini Mode).
  - Available in PSTwo mode by selecting the OPL Mini Mode option.  
* Validation system now uses REGEX.
* Improved source code.

`v1.3.1`
December 06, 2019
* Fixed SYSTEM.CNF file creation system for PSOne.
  - You can now choose the directory where the file will be saved.
* Rearranged the appearance of the graphical interface.
* Removed instruction screen previously located in graphical interface.
* Added "Display Help" option in the Help menu.
  - You can now read the program manual through this menu. _(psxhelp.chm)_
* Rewrite source code for improvement and cleanup.

`v1.3.0`
November 18, 2019
* Added support for creating Dummy _(gargabe)_ files to fill CD/DVD discs.

`v1.2.0`
November 17, 2019
* Added support for choosing directory to save SYSTEM.CNF file
* Added program information screen
* Added donation option via PayPal ;)

`v1.1.0`
November 16, 2019
* Added full support of SYSTEM.CNF for PSOne
* Stability corrections

`v1.0.0 - Release To Manufacturing (RTM)`
November 15, 2019
* Added HDDUNITPOWER support _(PSTwo)_
* Added reset option all settings

`v0.50.0 - RC Version (Release Candidate)`
November 14, 2019
* Added full support of SYSTEM.CNF for PSTwo
* Stability corrections

`v0.10.0 - Beta Version`
November 10, 2019
* Initial release BETA

## Compile
* * *
See _COMPILE_ file for how to compile and install PSX/2 CNF Creator.

## Documentation
* * *
See _README_ for PSX/2 CNF Creator information.

## License
* * *
This project is released under the GNU license. If you redistribute the binary or source code of PSX/2 CNF Creator, please attach file _LICENSE_ with your products.
Review _LICENSE_ file for further details.

* * *
Copyright 2019, Laete Meireles (Axion Drak)

<<[back](./)
