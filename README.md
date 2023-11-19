# ERCF v2 Community Project

This README is under construction.... (and represents internal developer notes at the momement)

## BOM Quick Link
[https://docs.google.com/spreadsheets/d/1HtVIu4yqzS6xJQr63-JKtMAh4Xq7wbtWPFeuiCnrnnE](https://docs.google.com/spreadsheets/d/1HtVIu4yqzS6xJQr63-JKtMAh4Xq7wbtWPFeuiCnrnnE)


This is the, perhaps temporary, repository for community development of the next generation v2 Enraged Rabbit Carrot Feeder (ERCF). This project is endorsed by ERCF's creator Ette.  Thank you for an awesome project Ette!!

## Manual Quick Link
[https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g](https://docs.google.com/presentation/d/1GNcei5_qR5PPlFaxJqjTnTScKnyJQXV2OCJxBeb3A3g/edit?usp=sharing)


This is the Google Slides document containing the ERCFv2 manual for community development. Currently, we are adding the content from the ERCF v1 manual with placeholder images. Once that is complete, we will move on to updating the manual and loading in update images.

Please be careful sharing the link, as it grants edit permission.

## Initial Development / Test Team:
* @moggieuk V0.1503 | V2.4088
* @gneu V2.5345
* @sneakytreesnake V2.3804
* @mneuhaus VT.483
* @Miriax
* @kinematicdigit
* @ningpj


## Goals:
- Simplify construction (without any significant additional costs)
- Aim for out of the gate reliability (i.e. wider tolerance for certain parts)
- Quicker set up time / less config
- Align with current BOM and design as closely as possible.


## Components:
1. Sturdy backbone (based on Sturdy Bunny from @sneakytreesnake V2.3804)
2. Reliable encoder (based on Binky from @mneuhaus VT.483)
3. Remove need for top hats with sprung servo (based on Springy from @moggieuk V0.1503 | V2.4088)
4. Remove snag points on reverse filament flow (for EndlessSpool support)
5. Improve gate mechanism so filament does not slip back through accidentally (perhaps removing the need for the magnetic gate?) (based on Triple Decky from @gneu V2.5345)
6. Remove high wear parts / those prone to breakage (the servo arm improvements / bearing)
7. Formal filament bypass (including position in selector array)
8. Standardized layout so things like calibrating the selector is mostly automatic (the geometry is sufficiently fixed)
9. Rationalize command line set in Happy Hare for consistency
10. Magnetically closed connector cover on encoder (the current one is prone to breaking)
11. Reinforced gearbox assembly, preventing twisting with overtightened fasteners (@sneakytreesnake V2.3804)
12. Filament passthrough integrated into filament block end as standard (@moggieuk V0.1503 | V2.4088, @sneakytreesnake V2.3804) 
13. Updated manual


## Other Planned Companion Projects:
* ERCP v2 (new buffer system) which could be based on the auto rewind idea from @mneuhaus VT.483
* Pellet purge system to remove the need for the wipe tower and to unify tip creation to one place. Based on @bombela V2.4393 Assisted Purge System work
* Idea: Integrated dIsplay / control panel.  Integrated low spec rpi running a further customized version of KlipperScreen that is solely for managing ERCF.  The pi could also drive ERCF motors and servo

## CAD Design Guidelines

### Features

* no overhangs over 45 degrees
* no supports (unless they are absolutely needed, and if that's the case they must be built in to the part)
* 0.4mm chamfer on surfaces that touch the print bed (and no fillets on the build surface--breaks the 45 degree overhang rule)
* general "nice" aesthetic
* Take note of part orientation to make sure the part is strong in the directions it needs to be.
* Countersunk holes "overhanging" the print surface should have a chamfer on them or other method like that to prevent issues
* Think about minimum perimeters/shells--try to avoid really thin features
* Design with common screws/hardware in mind. Ie, stick with M3x6,8,12,16,20,25,30,35,40, M5x10,16,30,40 when possible (for V1/V2)
* Counterbore bridging for holes [[1]](#counterbore)
* always orient STLs such that no reorientation is necessary (stricter that just thinking about it in design)
* consider fillets for all edges that are sharp and might be touched by people, 0.5-1.0 tends to be good
* loose joints generally oversized by 0.3-0.4mm diameter for loose fit or 0.1mm for press fit. 3.4mm for M3 hardware, 5.4mm for M5 hardware

### Screw Holes
* Loose fit screw holes - Make the hole 0.4mm bigger
* Thread into the plastic - Make the hole 0.1mm smaller

### Press Fits/Bearings
* Make the feature .2mm bigger. A 10mm diameter bearing would be 10.2mm [[3]](#press-fit)

### Heatsets
* Heatset holes should be 4.7mm in diameter
* blind heatset holes should be 5mm deep
* add a 0.4 chamfer to all heatsets entrance edges on build surface (helps with insertion)

### References
* [1] <a href="https://github.com/Finn2708/CounterboreBridging" id="counterbore">Fusion360 Counterbore Addon</a>

### Photos
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
