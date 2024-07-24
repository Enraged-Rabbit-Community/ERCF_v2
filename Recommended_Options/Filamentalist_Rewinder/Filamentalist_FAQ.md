# Filamentalist Frequently Asked Questions

[1. Troubleshooting](#troubleshooting)

[2. Dimensions/Footprint](#dimensions-footprint)

[3. Pregate Sensor Solutions](#pregate-sensor-solutions)

[4. Enclosure Solutions](#enclosure-solutions)

[5. Stronger gear motor and 40 tooth mod](#gear-motor-options)

## Troubleshooting
- If you have built the Filamentalist(s) and are having issues with its functioning such as loose loops or gear motor stalling please refer to this [Trouble Shooting Guide](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/troubleshoot.md).  If this doesn't help to resolve your questions you can get help from the many great users at the Filamentalist Discord server here (https://discord.gg/uDcGxukRKd)

## Dimensions Footprint
- Length:  186mm
  - Length with 200mm Diameter Spool:  202mm
- Height:  76mm without optional Base Plate, 79mm with Base Plate
  - Height with 200mm Diameter Spool:  252mm without optional Base Plate, 255 with Base Plate (varies slightly with Rim Roller rubber band thickness)
- Width:  80mm Axle Version = 81.5mm, 100 mm Axle Version = 100mm
  
[return to index](#filamentalist-frequently-asked-questions)

## Pregate Sensor Solutions

  Research the options below and decide what will work best for you.
  
  ### CottonTail Lite:
  - Coupler Blocks: https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/ERCT_Buffer/Coupler_Block/Coupler_Block_Lite.stl
  - End Cap Mount:  https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/ERCT_Buffer/Support_Arm/End_Cap_Mount.stl
  - End Arm Cap Mount:  https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/ERCT_Buffer/Support_Arm/End_Arm_Cap_Mount.stl
  - End Arm Cap Mount Extension:  https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/ERCT_Buffer/Support_Arm/End_Arm_Cap_Mount_Extention.stl
  - Electronics Box will Mount to This:  https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/rc2/Stls/Electronics/Universal_Box
  
  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/6c7f8dd72794a8ecd0c1e0981dfac9007970ab2d/Recommended_Options/Filamentalist_Rewinder/Assets/CottonTail%20Lite%20Pre-Gate%20Sensors.jpg" width="500" height="350">

  ### CheeseFrog's
  https://github.com/juliusjj25/ERCF-Pregate-Sensors

  This is what SkiBikePrint uses (SkiBikeMake on Discord).  It is simple and works great.  It requires the "bumped" lever style Omron D2F microswitches.  Great for a new build.  Retrofitting this onto an existing ERCF requires a tear down of the unit to replace the filament path portion of the blocks as well as the latches.  I did it the brute force way and trimmed my existing latches back with clippers and "muscled" the filament path parts out and back in to the blocks.  The brute force approach may not be for everyone!
  
  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/d43d10075f9a9581f6db1cd0bece84393a75faaf/Recommended_Options/Filamentalist_Rewinder/Assets/CheeseFrog%20Sensors.jpg" width="500" height="350">

  ### Gneu's Filament Block 
  https://github.com/gneu42/Triple-Decky/tree/main/STL/ERCF-V2/Rev_C/Rev_C9/Optional%20Pre-gate%20Sensor%20(Experimental)

  Similar to the CheeseFrog solution but more complex.  Also requires a teardown/rebuild if added to an existing ERCF.
  
[return to index](#filamentalist-frequently-asked-questions)

## Enclosure Solutions

  ### Filamentalist Enclosure

  An elegant passive enclosure/dry box (no heaters or fans) designed to house the Filamentalist passive rewinder.  It is great for a 4-6 channel ERCF (can go to higher channels if desired).  It consists of (4) printed endcaps, (6) pieces of 2020 extrusion cut/ordered to the desired length, and 0.060" (1/16') polycarbonate sheet(s) cut to size.  Details and files here:  https://github.com/SkiBikePrint/ERCF_Mods/tree/main/Filamentalist_Enclosure

  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240619_221414.jpg" width="500" height="350">

  ### (Un)original Prusa Drybox

  Box is available here:  https://www.printables.com/model/551828-unoriginal-prusa-drybox .  Delete the rollers and add your own Filamentalist mounting solution.  You may need the rear load option for the Filamentalist

  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/26b48491a1fce7cc9411857c30e11546146ed1a2/Recommended_Options/Filamentalist_Rewinder/Assets/UnOriginal%20Prusa%20DryBox.jpg" width="300" height="350">
  (solution/picture courtesy of barsam on Discord)

  
[return to index](#filamentalist-frequently-asked-questions)

## Gear Motor Options

  It is frequently asked if a NEMA 14 gear motor is strong enough to drive an MMU plus Filamentalist.  The 0.7A Moons NEMA 14 motor that came with my ERCF V1 Blurolls kit worked fine with the ERCF V1 and Filamentalist.  When I upgraded to ERCF V2 the additional resistance that came with the "Springy" version of the selector made the system slightly underpowered with a NEMA 14.  So if a NEMA 14 is what you currently have for your ERCF, TradRack, or other MMU, I suggest you try it before buying a higher torque motor.  If you are building a new MMU then a NEMA 17 recommended.  

  For the ERCF Grafton's 40 tooth gear mod is also recommended ( https://www.printables.com/model/692720-ercf-40-tooth-gear-modifiction ). It allows you to use the same belt as is used with the baseline 80 tooth gear by providing a higher motor mount to take up the slack. Some ERCF kits come with a 42Ncm NEMA 17.  This combined with the 40T mod should give you sufficient torque to overcome MMU and long bowden tube resistance as well as allowing to run the Filamentalist at 300+mm/s speeds.  

  If you are buying a new NEMA 17 below are verified high torque motors (55-59Ncm) that perform well in the needed RPM range for 200-500mm/s load/unload speeds.  There is really no need to go higher than the 55-59Ncm torque range as you will just start grinding grooves in your filament with the MMU gear.

1. 17HE19-2004S from stepperonline.com - 55Ncm (they have a new 17HS19-2004S1 50Ncm version that should be similar to the 17HE19-2004S but a little more powerful)
2. LDO-42STH48-2504AC - 55Ncm

[return to index](#filamentalist-frequently-asked-questions)
