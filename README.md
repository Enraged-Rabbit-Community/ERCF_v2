## TEMPORARY Manual Quick Link
[https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g](https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g/edit?usp=sharing)

This is the (temporary) Google Slides document containing the ERCFv2 manual for community development. Currently, we are adding the content from the ERCF v1 manual with placeholder images. Once that is complete, we will move on to updating the manual and loading in update images.

Please be careful sharing the link, as it grants edit permission.

---

# Enranged Rabbit v2 Community Project

<p align="center">
  <img src="/Assets/ERCFv2.png" alt='ERCFv2' width='70%'>
  <h1 align="center">Voron ERCF v2</h1>
</p>

<p align="center">
An expandable MMU for Klipper based 3D-Printers
</p>

<p align="center">
  <a aria-label="Downloads" href="https://github.com/Enraged-Rabbit-Community/ERCF_v2/releases">
    <img src="https://img.shields.io/github/release/Enraged-Rabbit-Community/ERCF_v2?display_name=tag&style=flat-square">
  </a>
  <a aria-label="Stars" href="https://github.com/Enraged-Rabbit-Community/ERCF_v2/stargazers">
    <img src="https://img.shields.io/github/stars/Enraged-Rabbit-Community/ERCF_v2?style=flat-square">
  </a>
  <a aria-label="Forks" href="https://github.com/Enraged-Rabbit-Community/ERCF_v2/network/members">
    <img src="https://img.shields.io/github/forks/Enraged-Rabbit-Community/ERCF_v2?style=flat-square">
  </a>
  <a aria-label="License" href="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/Enraged-Rabbit-Community/ERCF_v2?style=flat-square">
  </a>
</p>

<br>

<table>
<tr>
<td width=30%> <img src="/Assets/Enraged_Rabbit_v2.png" alt='RabbitV2'></td>
<td>
This is a community born project and major update to the Voron ERCF MMU that was started a couple of years ago by Ette.  It is endorsed by Ette and the guiding philosophy wasn't to start again with a new MMU design but to refine what has already proven to be a very capable machine and push it to be the best it can be by simplifying problematic construction, improving reliability and aligning as close as possible to v1.1 BOM. However the project includes an all new optional integrated filament buffer system (ERCT), filament cutter option (ERF), a collection of recommended toolhead sensor modifications and a bit of Bling! It fully leverages the Happy Hare firmware MMU control software with Klipper Screen entensions.
<p>
  
There are a rapidly growing list of MMUs in the market place from the mass produced "Fords" who pioneered the market to the "Toyotas" that are more recent efficient engineering feats but somehow lack soul. We consider ERCFv2 the "BMW" - a little over engineered perhaps but destinctively cool and you feel good drving it.  We hope you enjoy!
</td>
</tr>
</table>

## Table of Content
- [ERCF Changes since V1.1](#enraged_rabbit_carrot_feeder_ercf)
- [Optional Components](#optional_components)
- [Firmware](#firmware)
- [BOM](#bom)
- [Acknowledgements](#acknowledgements)
- [Changelog](#changelog)
- [Build Photos](#build-photos)
- [Showroom](#showroom)
<!--
- [FAQ](https://github.com/EtteGit/EnragedRabbitProject/tree/main/Documentation/FAQ)
  - [Carrot Patch](https://github.com/EtteGit/EnragedRabbitProject/blob/main/Documentation/FAQ/FAQ_ERCP.md)
  - [Carrot Feeder](https://github.com/EtteGit/EnragedRabbitProject/blob/main/Documentation/FAQ/FAQ_ERCF.md)
-->

<br>

## Enraged Rabbit Carrot Feeder (ERCF)
If you are familar with ERCF v1.1 this will serve as an overview of updates:
<ol>
  <li>Sturdy backbone - no more flex
  <li>Reliable (and custom) encoder design
  <li>Sprung servo instead of adjustable top hats
  <li>Innovative 3-position servo design & Filament trap in blocks instread of magnetic gates
  <li>Formal filament bypass
  <li>Reinforced gearbox assembly
  <li>Beautifully illustrated Manual
  <li>High Quality Step-by-step CAD
  <li>New integrated passive buffer system (Cotton Tail)
  <li>Reliable tips with companion Filament cutter
  <li>Both functional and asthetic LED status indication option. Aka Bling!
</ol>

<br>

## Optional Components
<i>(although you might see variations of these projects elsewhere, consider this the new integrated and guaranteed ERCF compatable source)</i>

### Enraged Rabbit Cotton Tail (ERCT)
<table>
<tr>
<td width=30%><img src="Options/ERCT_Buffer/Assets/heroimage_ERCT.png" alt='ERCT'></td>
<td>
When an MMU changes tool the unloaded filament needs to be thoughtfully managed so that is doesn't tangle. The Enraged Rabbit Cotton Tail (ERCT) buffer system is designed to attach directly to ERCF V2. It is a passive system that optimizes space and is also designed to reduce resistance in the filament path, creating a consistent system for calibration.
<p>

ERCT also incorporates a neopixel on each gate that, when driven by the Happy Hare firmware, provides both functional feedback as well as the necessary "bling".  Enjoy!
<p>

[Read more](Options/ERCT_Buffer/ERCT.md)
</td>
</tr>
</table>

### Enraged Rabbit Filametrix (ERF)
<table>
<tr>
<td>
Before the MMU can unload a filament it must prepare the tip so that it can be cleanly loaded next time.  This tip forming process is very difficult to tune and varies based on material type, temperature, hotend type and even weather!  Introducing Enraged Rabbit Filametrix (ERF) filament cutting system.  This lightweight addition to your Stealthburner toolhead adds a cutting blade.  When retracting the problematic tip of the filament is simply cut off for perfect tips and no jams.
<p>

ERF also supports an optional servo operated ganrtry activation pin so no print area is lost with this addition. ERF designs also include the recommended integrated toolhead sensor
<p>

[Read more](Options/ERF_Filament_Cutter/ERF.md)
</td>
<td width=30%><img src="Options/ERF_Filament_Cutter/Assets/ERF.png" alt='ERF'></td>
</tr>
</table>


### Toolhead Sensors
ERCF can be operated without a toolhead sensor (filament detection) in the toolhead but it is not recommended. A toolhead sensor provides an accurate homing point very close to the nozzle but also adds reliability to the tool change process. ERCF includes a set of toolhead sensor modifications for popular extruders. These work reliably through coupling a microswitch to the filament path.

### Other (Possibly) Planned Optional Companion Projects:
<ul>
  <li>Pellet purge system to remove the need for the wipe tower. Stay tuned
</ul>

<br>

## Firmware
<table>
<tr>
<td width=30%><img src="https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition/blob/master/docs/img/mmu/mmu_main.png" alt='KlipperScreen'></td>
<td>
ERCF is designed to be used with the Happy Hare MMU firmware for Klipper which adds a set of klipper extensions for configuration setup, testing and operation of ERCF. These commands are available through the command line or macros but are perhaps best operated with an interactive UI with the optional KlipperScreen extension.
<p>

Happy Hare provides an easy installation script which has knowledge of recommended settings and will greatly accelarate the setup process.
<p>

[Happy Hare](https://github.com/moggieuk/Happy-Hare) &nbsp;&nbsp; [KlipperScreen](https://github.com/moggieuk/KlipperScreen-Happy-Hare-Edition)
</td>
</tr>
</table>

<br>

## BOM
You can find a Bill of Material for the project and options here: [BOM](https://docs.google.com/spreadsheets/d/1HtVIu4yqzS6xJQr63-JKtMAh4Xq7wbtWPFeuiCnrnnE)
Note that the BOM also contains an upgrade list for those of you wanting to use your existing ERCF v1.1 kits.

## Acknowledgements
Most importantly let me introduce the development, test and doc team.  A project like this doesn't happen without hundreds of hours of volunteer effort and all of these folks are truely awesome.  Please give some :clap: :clap: :clap:
<ul>
  <li>@moggieuk V0.1503 | V2.4088 (Mr Happy Hare & Chief whip)
  <li>@gneu V2.5345 (Filament block innovator)
  <li>@sneakytreesnake V2.3804 (The project backbone!)
  <li>@mneuhaus VT.483 (Mr Binky)
  <li>@Miriax (Designer & Doc Demon)
  <li>@kinematicdigit (Mr Cotton Tail & Doc Illustrator)
  <li>@ningpj (Tester, Breaker & Doc's)
  <li>@fizzy (King of CAD)
  <li>@gsx8299 (Test Builder Extraordinaire)
  <li>@sorted (Filametix "don't get enraged" filament cutting system)
  <li>@kierantheman (Mr Thumper)
</ul>

<br>

## Changelog
<ul>
  <li>v2.0 - Initial Release (Merry Christmas!)
</ul>

CAD Design Guidelines used in this project (in case you were interested) can be found: [here](/Assets/Dev_Notes.md).

<hr>

<br>

## Build Photos
![20231116_230501](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/3d18d3fe-b8f0-4750-8b06-f487ab54ef35)
![20231116_211032](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/971ceefa-8946-438d-9de7-a26cfcdae56b)
![20231116_214903](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/5781d748-67eb-44f2-a793-cf8f4229b99f)
![20231116_211045](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/5df5f56e-9424-42d0-9985-a84c04d67c12)
![20231116_230638](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/ed578c32-6d4d-4698-8aeb-008a0cdf959e)
![IMG_2446](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/fde29ef8-6356-4a68-bd17-26fd160b5c9f)
![IMG_2448](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/bb66a3e3-326e-4866-97da-3e80767f3dc7)
![IMG_2445](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/1b943168-492d-44d6-ad12-038a6f12a8ca)
![IMG_2443](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/147fb32d-f3e4-4365-b579-de3997274053)
![IMG_2444](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/6d84f624-84b9-4a88-ad7c-de2a09619397)
![IMG_2447](https://github.com/Enraged-Rabbit-Community/ERCF_v2/assets/121695166/52122c6a-e28c-4bd7-a8a8-324b2cc9a74f)

## Showroom
<img src="Assets/Showroom/Spidermans.png" alt="Spidermans" width="950"/><img src="Assets/Showroom/NoS_Prints.png" alt="NoS_prints" width="950"/><img src="Assets/Showroom/BnE_Prints.png" alt="BnE_Prints" width="950"/><img src=Assets/Showroom/Bimaterial_logo.png alt="Voron Logo TPU" width="650"/><img src=Assets/Showroom/9_colors_test.png alt="9_colors_test" width="400"/>

