#### Page Sections:
  - [Installation](#---installation)
  - [Caveats & Possible problems / workarounds](#---caveats--possible-problems--workarounds)
  - [Font Problems](#---font-problems)
  - [Blank Screen After Update](#---blank-screen-after-system-update)
  - [Happy Hare Version Incompatibility](#---happy-hare-version-incompatibility)
  
*\[This guide is copied from the [KlipperScreen Happy Hare repo](https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition) and reformatted for ERCF. Thanks Moggie!\]*

## ![#f03c15](assets/f03c15.png) ![#c5f015](assets/c5f015.png) ![#1589F0](assets/1589F0.png) Installation
**Firstly, make sure Happy Hare software is completely up-to-date. Features were added to support this KlipperScreen add on.**

Install and setup a base KlipperScreen from the original source. Get it working. Don't skip this step because we cannot help with basic KlipperScreen and system setup.  Once you have that installed and working, log into you Rasberry Pi and execute the following commands. You can cut'n'paste...

    cd ~
    mv KlipperScreen KlipperScreen.orig
    git clone https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition.git KlipperScreen
   
    cd ~/KlipperScreen/happy_hare
    ./install_ks.sh -g <num_gates>
   
(where <num_gates> is the number of selectors you built with, e.g. 8 for a typical ERCF v2)
   
KlipperScreen will be restarted and hopefully you should now be running the enhanced version!

> [!NOTE]  
> Expert Tip: The last step of running './install_ks -g <num_gates>' can be run many times.. and sometimes is needed after an update to install new images or update menu structure. If you customize the MMU part of the KlipperScreen menu and want to make use of the "replicator" function that will automatically replicate menu options for the configured number of gates, you can edit menus.conf and reference the templating there.

Note that the base KlipperScreen is up-to-date (and Moggieuk will continue to merge with master every 2 weeks) with changes in the original but also includes extra menu functionality that can be used in the creation of your custom menus.  See the generated ercf_klipperscreen.conf for clues!

## ![#f03c15](assets/f03c15.png) ![#c5f015](assets/c5f015.png) ![#1589F0](assets/1589F0.png) Caveats & Possible problems / workarounds
I have only tested on a single screen.  A 640x480 resolution BTT TFT5.0.   It is possible that you might find layout problems on other (likely smaller) displays.  Also, I have only tested in and optimized for horizonal orientation.  I doubt it will be effective in vertical but I don't know of any Voron owners with vertically mounted panels.

JFYI the installer will alter or add the KlipperScreen entry in `moonraker.conf`:

    [update_manager KlipperScreen]
    type: git_repo
    path: ~/KlipperScreen
    origin: https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition.git
    env: ~/.KlipperScreen-env/bin/python
    requirements: scripts/KlipperScreen-requirements.txt
    install_script: scripts/KlipperScreen-install.sh
    managed_services: KlipperScreen

## ![#f03c15](assets/f03c15.png) ![#c5f015](assets/c5f015.png) ![#1589F0](assets/1589F0.png) Font problems:
The CSS style only specifies a "Free Mono" font to be used (the same as original KlipperScreen) for all textual displays.  I use the Unicode Box character set in that font to render the selector status, filament positions and TTG map. A couple of users have reported issues with this part of the display, either not appearing or not spaced correctly.  E.g.

![mmu_panel_printing](https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition/blob/master/docs/img/mmu/font_problem.jpg)

If this occurs the first thing to try is to run the following, then restart KlipperScreen:

    sudo apt install fontconfig
    fc-cache -f -v
    sudo systemctl restart KlipperScreen

If this doesn't fix the problem I suggest installing a new font set.

> [!NOTE]  
> A very useful way of listing the fonts you have installed on your system by family is with:
> > fc-list : family | sort | uniq

<details>
<summary>🔹 How to install JetBrains fonts...</summary>

Download the JetBrains fonts from (www.jetbrains.com).  Extract the zip.  Copy all the `*.ttf` fonts (you will find them under fonts/ttf in the extracted zip) into `/usr/share/fonts/truetype` directory (you will have to sudo cp else you will likely get permission denied), then cache these fonts:

    cd <path where you extracted the font files>/fonts/ttf
    sudo cp *.ttf /usr/share/fonts/truetype
    fc-cache -f -v
     
Then finally update the font reference in the KlipperScreen css file:

    cd ~/KlipperScreen/styles

Edit the `base.css` file.  Find the css entry for `.mmu_status`, then change the font-family to:

    font-family:      JetBrains Mono;

(by default it is `font-family:     Free Mono;`)

Then restart KlipperScreen

    sudo systemctl restart KlipperScreen

If you have to do this, please let Moggieuk know the details about the operating system you are running on and how you installed KlipperScreen in the first place... if I can locate the source of the issue I might be able to workaround in the future.

</details>

## ![#f03c15](assets/f03c15.png) ![#c5f015](assets/c5f015.png) ![#1589F0](assets/1589F0.png) Blank Screen after system update
It has come to my attention that sometimes a system (OS) update can break KlipperScreen.  This is nothing to do with KlipperScreen but rather the installation of a slightly broken video driver `fbturbo`.  Luckily the fix is simple.  After OS upgrade run:

    sudo apt purge xserver-xorg-video-fbturbo

## ![#f03c15](assets/f03c15.png) ![#c5f015](assets/c5f015.png) ![#1589F0](assets/1589F0.png) Happy Hare version incompatibility
If you are upgrading and see a message like this when accessing the main MMU panel it is probably because of a version mismatch with Happy Hare on your printer.  Follow the instructions in the popup!

<img src="https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition/blob/master/docs/img/mmu/mmu_version_error.png" width=50%>

*All screen shots are taken with the "Colorize" theme (my preference because the buttons are more defined).  The default is z-bolt and looks slightly different.*



### ERCF Setup Steps:
- [Flashing Your Local MCU](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Flashing-Local-MCU.md)
- [Installing Happy Hare](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Installing-Happy-Hare.md)
- [Happy Hare Configuration](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Happy-Hare-Configuration.md)
- [Hardware Configuration Checks](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Hardware-configuration-checks.md)
- [Hardware Calibration](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Hardware-Calibration.md)
- [Toolhead Distances](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Toolhead-Distances.md)
- Installing KlipperScreen Happy Hare
- [Slicer Setup](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Slicer-Setup.md)
- [Further Mods to Consider](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/Further-Mods.md)

#### Even more Happy Hare info can be found at:
- [Happy Hare Wiki](https://github.com/moggieuk/Happy-Hare/wiki)