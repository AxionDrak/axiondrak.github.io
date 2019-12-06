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

* ![useful image]({{ site.url }}/assets/images/exe-icon.png) [Requires .NET Framework 4.5](https://www.microsoft.com/en-US/download/details.aspx?id=30653) (Web installer)

## Hash
* * *
Use the table below to ensure that downloaded files have not changed. These values are for the latest stable version in its compiled (final) version.

Version: 1.3.1

| Filename                 | MD5                              | SHA256                                                         
|:-------------------------|:---------------------------------|:-----------------------------------------------------------------|
| LICENSE                  | e62637ea8a114355b985fd86c9ffbd6e | 230184f60bae2feaf244f10a8bac053c8ff33a183bcc365b4d8b876d2b7f4809
| PSX2CNFCreator.exe       | dd0c35d018b24e87ec0f718252642e95 | ad125417a59c54f0e37b16e5a154cdf992b975ab9246d904f942fdd9844f49e9
| README.md                | 845a543111e6fbef46a58bf4b077e5ad | d8edd37c2b09a8fb0d35e895aa5b334fbdb792dedea47c6ec7f1d3f72932127d
| psxhelp.chm              | a2bff35e32c93ddcf35d5bd8b910b297 | 32395274a35ba473940cee39864ee1d202e724f1a5df313796f19e8899642d5d
| PSX2CNFCreator_1.3.1.zip | 5231ef77bffce2a693de508f5cab4b54 | 3b1a4243d3bc1c73bef78d4d9e76ab0903269b8be1bf4493dbe647ff80f12b8c

## Features
* * *
* Supports create SYSTEM.CNF files _(PSOne and PSTwo)_
* Supports any ELF file _(PSOne and PSTwo)_
* Supports file and program versioning _(PSTwo)_
* Supports PAL and NTSC video modes _(PSTwo)_
* Supports HDDUNITPOWER in NONE, HDD, NIC and NICHDD modes _(PSTwo)_
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

Below are two examples of this file:

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
