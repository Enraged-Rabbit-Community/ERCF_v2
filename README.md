## TEMPORARY Manual Quick Link
[https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g](https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g/edit?usp=sharing)

This is the Google Slides document containing the ERCFv2 manual for community development. Currently, we are adding the content from the ERCF v1 manual with placeholder images. Once that is complete, we will move on to updating the manual and loading in update images.

Please be careful sharing the link, as it grants edit permission.

---

# ERCF v2 Community Project

<p align="center">
  <img src="need_ogo.jpg" alt='ERCFv2' width='30%'>
  <h1 align="center">Voron ERCF v2</h1>
</p>

<p align="center">
MMU for Klipper based 3D-Printers
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

This is a community born project and major update to the Voron ERCF MMU that was started a couple of years ago by Ette.  It is endorsed by Ette and the guiding philosophy wasn't to start again with a new MMU design but to refine what has already proven to be a very capable machine and push it to be the best it can be by simplifying construction, improving reliability and aligning as close as possible to v1.1 BOM. The project includes an all new optional integrated filament buffer system (ERCT) and a bit of bling!  It fully leverages the Happy Hare firmware MMU control software and Klipper Screen entensions.

## Table of Content
- [New Components](#changelog)
- [BOM](#bom)
- [Acknowledgements](#acknowledgements)
- [Build Photos](#build-photos)
- [Showroom](#showroom)
- [Chagelog](#changelog)
<!--
- [FAQ](https://github.com/EtteGit/EnragedRabbitProject/tree/main/Documentation/FAQ)
  - [Carrot Patch](https://github.com/EtteGit/EnragedRabbitProject/blob/main/Documentation/FAQ/FAQ_ERCP.md)
  - [Carrot Feeder](https://github.com/EtteGit/EnragedRabbitProject/blob/main/Documentation/FAQ/FAQ_ERCF.md)
-->
 
## New Components
If you are familar with ERCF v1.1 this will serve as an overview of changes:
1. Sturdy backbone (based on Sturdy Bunny by @sneakytreesnake V2.3804)
2. Reliable encoder (based on Binky by @mneuhaus VT.483)
3. Remove need for top hats with sprung servo (based on Springy by @moggieuk V0.1503 | V2.4088)
4. Remove snag points on reverse filament flow (for EndlessSpool support)
5. Improved gate mechanism to prevent filament slip back and removing magnetic gate (Triple Decky by @gneu V2.5345 and refined by Thumper Blocks by @kierantheman)
6. Remove high wear parts / those prone to breakage (the servo arm improvements / bearing)
7. Formal filament bypass (including position in selector array)
8. Standardized layout so things like calibrating the selector is mostly automatic (the geometry is sufficiently fixed)
9. Rationalize command line set in Happy Hare firmware for consistency
10. Magnetically closed connector cover on encoder
11. Reinforced gearbox assembly, preventing twisting with overtightened fasteners (@sneakytreesnake V2.3804)
12. Filament passthrough integrated into filament block end as standard (@moggieuk V0.1503)
13. Updated manual (@Miriax, @ningpj, @kinematicdigit
14. High Quality Step-by-step CAD (@fizzy)
15. New integrated passive buffer system (Cotton Tail by @kinematicdigit)
16. Testing, Ideas and Quality (the whole team)

### Other (Possibly) Planned Companion Projects:
* Pellet purge system to remove the need for the wipe tower and to unify tip creation to one place. Based on @bombela V2.4393 Assisted Purge System work
* Filament cutter to avoid need to form tips

## BOM
You can find a Bill of Material for the project here: [BOM](https://docs.google.com/spreadsheets/d/1HtVIu4yqzS6xJQr63-JKtMAh4Xq7wbtWPFeuiCnrnnE)
Note that the BOM also contains an upgrade list for those of you wanting to use your existing ERCF v1.1 kits.

## Acknowledgements
Firstly and most importantly let me introduce the development and test team.  A project like this doesn't happen without hundreds of hours of volunteer effort and all of these are awesome.  Please give some :clap: :clap:

* @moggieuk V0.1503 | V2.4088 (Mr Happy Hare)
* @gneu V2.5345 (Filament block innovator)
* @sneakytreesnake V2.3804 (The backbone!)
* @mneuhaus VT.483 (Mr Binky)
* @Miriax (Doc Demon)
* @kinematicdigit (Mr Cotton Tail)
* @ningpj (Tester and Breaker)
* @fizzy (Master of CAD)
* @kierantheman (Mr Thumper)
* gsx8299 (Builder Extraordinaire)
* @bombella (Purge system fame)

CAD Design Guidelines Used (in case you were interested) can be found: [here](/Assets/Dev_Notes.md)

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
<img src="Showroom/Spidermans.png" alt="Spidermans" width="950"/><img src="Showroom/NoS_Prints.png" alt="NoS_prints" width="950"/><img src="Showroom/BnE_Prints.png" alt="BnE_Prints" width="950"/><img src=Showroom/Bimaterial_logo.png alt="Voron Logo TPU" width="650"/><img src=Showroom/9_colors_test.png alt="9_colors_test" width="400"/>

## Changelog
TODO

