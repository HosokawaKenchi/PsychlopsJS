﻿About This Project
====================

Psychlops is a frer toolkit/library for drawing various types of visual stimulus used in the vision science. This is the JavaScript version running on web-browsers. Web-site of project including C++ version is at [osdn.jp](http://psychlops.osdn.jp/).


Samples with online editor
----------------------------

Currently, all samples are written in C++ and depends on embeded converter. Pure JavaScript version is being prepared.

- [Contrast Sensitivity (static)](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/ContrastSensitivity_space.cpp)
- [Contrast Sensitivity (dynamic)](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/ContrastSensitivity_temp.cpp)
- [Lilac Chaser](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/visiome/LilacChaser.cpp)
- [Motion Induced Blindness](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/visiome/MotionInducedBlindness.cpp)
- [Random Dot Stereogram](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/visiome/RandomDotStereogram.cpp)
- [Motion induced position shift](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/visiome/MotionInducedPositionShift.cpp)
- [2f3f](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/visiome/2f3f.cpp)
- [CIE Luv viewer](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/CIELuv_demo.cpp) ! Chromaticities of RGB of the display is assumed to be same to sRGB.
- [CIE Lab viewer](https://hosokawakenchi.github.io/PsychlopsJS/psychlops.editor.html#samples/CIELab_demo.cpp) ! Chromaticities of RGB of the display is assumed to be same to sRGB.


Reference Manual
======================

- [Reference Manual](https://hosokawakenchi.github.io/PsychlopsJS/import/doc/ReferenceManual)
- Reference Manual is also embeded in Online Editor. Push [?] icon placed at right-top of the editor's window.


User's Manual
======================

Installation
--------------

### System Requirements

#### Supported browsers
For the client, Chrome and Safari are recommended. Edge and Firefox are also supported. The latest version is strongly recommended for all the browsers.
- Chrome: version 60 or later
- Safari: version 10 or later
- Edge: version 11 or later
- Firefox: version 52 or later

#### Server: online and offline use
Since Psychlops JS operates as a Web application, it basically assumes that it is installed on an HTTP server and accessed via the Internet. At the same time, offline execution is also supported to execute programs in an offline environment with tablet devices.

#### Limitation in offline use
Due to security limitations, JavaScript cannot read and write local files on your computer. Program files should be directly written in <script> tag. Image files are needed to be linked by <img> tags before the loading image files by JavaScript program.


### Using Psychlops on the HTTP server

#### Installation
1.	Unzip all files from the package or git clone from server.
2.	Upload all the unzipped files on your HTTP server. The folder structure should be kept as is.
3.	Delete “index.html” in the top folder.
4.	Rename “index.online.html” to “index.html”.
5.	Access your HTTP server from web-browser. URL depends on your server setting.

### Using Psychlops on the local system

#### Installation
1.	Unzip all files from the package or git clone from server.
2.	Open “index.html” in the top folder of unzipped files in the local system.
3.	Try sample stimuli.
4.	Some functions are restricted in executing on the local system. For example, image files could not be loaded from local file system for security reason.


### Editing

#### Online use
Edit cpp files directly.

##### Editing index
Open “index.menu.html” at top of the Psychlops JS folder. Then, Please edit <li> elements inside the file. To open editor, write “psychlops.editor.html” inside the href attribute in the <a> element. To open experiment directly, write “psychlops.player.html” inside the href attribute.

#### Offline use
After editing cpp files, copy whole C++ programs inside the <textarea id="running_program"> element at the end of “psychlops.offline.template.html” file.


#### Editing index
Open “index.html” at top of the Psychlops JS folder. Then, Please edit <li> elements inside the <section id="menu_list"> element at the last of the file.


### Setup of test environment in local system
It is possible to test the online program in the local environment by running the HTTP server on the local system. Methods for executing the HTTP server in the local environment include the following, for example:
- (macOS and linux) Setup Apache server with package management system such as APT or MacPorts
- (Windows and macOS) Use third-party package to install Apache such as MAMP
- (Windows) Use Microsoft Visual Studio 


#### MAMP (for Windows and macOS)
1.	Download MAMP installer from official website (https://www.mamp.info/en/).
2.	Install MAMP. MAMP Pro is not needed.
3.	Place Psychlops JS files in MAMP’s “htdocs” folder.
4.	Access “localhost” from web-browser.
5.	Edit “index.menu.html” with favorite text editor to edit menu in index.html.
6.	Edit arbitrary cpp files with text editor.
