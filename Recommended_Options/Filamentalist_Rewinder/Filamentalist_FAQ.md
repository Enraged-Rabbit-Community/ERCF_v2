# Filamentalist Frequently Asked Questions

[1. Troubleshooting](#troubleshooting)

[2. Dimensions/Footprint](#dimensions-footprint)

[3. Enclosure Solutions](#enclosure-solutions)

[4. Gear motor recommendations and 40 tooth mod](#gear-motor-options)

[5. Pregate Sensor Solutions](#pregate-sensor-solutions)

[6. Rubber Band Sourcing Options](#rubber-band-sourcing-options)

[7. TPU - Can the Filamentalist handle soft/flexible materials?](#flexible-filament)

## Troubleshooting
- If you have built the Filamentalist(s) and are having issues with its functioning such as loose loops or gear motor stalling please refer to this [Trouble Shooting Guide](https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/troubleshoot.md).  If this doesn't help to resolve your questions you can get help from the many great users at the Filamentalist Discord server here (https://discord.gg/uDcGxukRKd)

## Dimensions Footprint
- Length:  186mm
  - Length with 200mm Diameter Spool:  202mm
- Height:  76mm without optional Base Plate, 79mm with Base Plate
  - Height with 200mm Diameter Spool:  252mm without optional Base Plate, 255 with Base Plate (varies slightly with Rim Roller rubber band thickness)
- Width:  80mm Axle Version = 81.5mm **(max spool width of 68mm)**, 100 mm Axle Version = 100mm **(max spool width of 86.5mm)** <br />
  <br />
    
[return to index](#filamentalist-frequently-asked-questions)

## Enclosure Solutions

  ### Filamentalist Enclosure

  An elegant passive enclosure/dry box (no heaters or fans) designed to house the Filamentalist passive rewinder.  It is great for a 4-6 channel ERCF (can go to higher channels if desired).  It consists of (4) printed endcaps, (6) pieces of 2020 extrusion cut/ordered to the desired length, and 0.060" (1/16') polycarbonate sheet(s) cut to size.  Details and files here:  https://github.com/SkiBikePrint/ERCF_Mods/tree/main/Filamentalist_Enclosure

  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240619_221414.jpg" width="500" height="350">

  ### (Un)original Prusa Drybox

  Box is available here:  https://www.printables.com/model/551828-unoriginal-prusa-drybox .  Delete the rollers and add your own Filamentalist mounting solution.  You may need the rear load option for the Filamentalist

  <img src="https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/Assets/UnOriginal%20Prusa%20DryBox.jpg" width="300" height="350">
  (solution/picture courtesy of barsam on Discord)<br />
  <br />
    
  [return to index](#filamentalist-frequently-asked-questions)


## Gear Motor Options

  It is frequently asked if a NEMA 14 gear motor is strong enough to drive an MMU plus Filamentalist.  The 0.8A Moons NEMA 14 motor that came with my ERCF V1 Blurolls kit worked fine with the ERCF V1 and Filamentalist.  When I upgraded to ERCF V2 the additional resistance that came with the "Springy" version of the selector made the system slightly underpowered with a NEMA 14.  So if a NEMA 14 is what you currently have for your ERCF, TradRack, or other MMU, I suggest you try it before buying a higher torque motor.  If you are building a new MMU, then a NEMA 17 with torque greater than 40N-cm is recommended.  

  For the ERCF, Grafton's 40 tooth gear mod is also recommended ( https://www.printables.com/model/692720-ercf-40-tooth-gear-modifiction ). It allows you to use the same belt as is used with the baseline 80 tooth gear by providing a higher motor mount to take up the slack. Some ERCF kits come with a 42Ncm NEMA 17.  This combined with the 40T mod should give you sufficient torque to overcome MMU and long bowden tube resistance as well as allowing to run the Filamentalist at 300+mm/s speeds.  

  If you are buying a new NEMA 17, below are verified high torque motors (55-59Ncm) that perform well in the needed RPM range for 200-500mm/s load/unload speeds.  There is really no need to go higher than the 55-59Ncm torque range as you will just start grinding grooves in your filament with the MMU gear.  There is likely several other stepper motor options that have similar specifications.

1. 17HE19-2004S from stepperonline.com - 55Ncm (they have a new 17HS19-2004S1 50Ncm version that should be similar to the 17HE19-2004S but a little more powerful)
2. LDO-42STH48-2504AC - 55Ncm<br />
  <br />
    
  [return to index](#filamentalist-frequently-asked-questions)


## Pregate Sensor Solutions

  Research the options below and decide what will work best for you.
  
  ### CottonTail Lite:  
  - https://github.com/Tyler8299/CottonTail-Lite
  - Includes:
    - Coupler Blocks
    - End Cap Mount 
    - End Arm Cap Mount
    - End Arm Cap Mount Extension
    - Universal Electronics Box, Lid, and Mount
    - LED Carrier/Apron
  
  <img src="https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/Assets/CottonTail%20Lite%20Pre-Gate%20Sensors.jpg" width="500" height="350">

  ### CheeseFrog's
  https://github.com/juliusjj25/ERCF-Pregate-Sensors

  This is what SkiBikePrint uses (SkiBikeMake (Filamentalist) on Discord).  It is simple and works great.  It requires the "bumped" simulated roller lever style Omron D2F-L3 microswitches.  These are great for a new build.  Retrofitting this onto an existing ERCF requires a tear down of the unit to replace the filament path portion of the blocks as well as the latches.  I did it the brute force way and trimmed my existing latches back with clippers and "muscled" the filament path parts out and back in to the blocks.  The brute force approach may not be for everyone!
  
  <img src="https://github.com/SkiBikePrint/Filamentalist/blob/9d7a90dc3dec40c67051558c80c616155eb8eba8/Assets/CheeseFrog%20Sensors.jpg" width="500" height="350">

  ### Gneu42's Filament Block 
  https://github.com/gneu42/Triple-Decky/tree/main/STL/ERCF-V2/Rev_C/Rev_C9/Optional%20Pre-gate%20Sensor%20(Experimental)

  Similar to the CheeseFrog solution but more complex.  Also requires a teardown/rebuild if added to an existing ERCF.<br />
  <br />

  ### Filamentalist Tensioner Mount based Pre-Gate Sensors

  This option is provided for users who are using an MMU other than ERCF and don't have another option for pre-gate sensors.  Although these work well, I have found that having the sensor "bump" at the beginning of the Tensioner Mount filament path makes filament loading a little more difficult.  If you are building a new ERCF I recommend the Cheesefrog sensors above.  If you have an existing ERCF and have the space for them, the CottontailLite sensors above are a good option.  For more information on the Tesnioner Mount based pre-gate sensor option refer to the assembly manual, CAD, and stl files.

  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/354a8adedb6695756e69be10073012356cb178e7/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_pre-gate_sensor_cad.jpg" width="250" height="250"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/354a8adedb6695756e69be10073012356cb178e7/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_pre-gate_sensor_pic.jpg" width="250" height="250">

    
  [return to index](#filamentalist-frequently-asked-questions)


## Rubber Band Sourcing Options

### Bike Tire Inner Tube
- You can cut to get a perfect fit across the face of the Rim Roller for 80mm, 100mm, or custom width rewinders with this solution.  Mountain bike or "balloon" tire sized tubes for tires in the 1.75"-2.5" width work well.  Select a wheel diameter of at least 16" to have enough material for up to 12 100mm wide rewinders.  Cut at ~30-35% wider than face of Rim Roller to account for width reduction when stretched onto roller.
  - easy to source locally (your garage, bike shop, hardware store,...)
  - Amazon example: https://www.amazon.com/BELL-Standard-Bicycle-Inner-Tube/dp/B003CUBPUY
  - Aliexpress example: https://www.aliexpress.us/item/3256804654544066.html
 
<img src="https://github.com/SkiBikePrint/Filamentalist/blob/71cee20fe18fa942feb86cab2a580b9eeac974d1/Assets/inner_tube.jpg" width="500" height="350">

### Rubber Bands
  - For the standard size Classic Rewinder (20mm Rim Roller face width):
    - Size #82 (2 1/2" length x 1/2" wide) or ~50mm diameter (~80mm length) x 10mm width
      - qty 2 per roller for 80mm width version, qty 3 per roller for 100mm width version
    - Amazon example: https://www.amazon.com/AIWOQI-Industrial-supplies-Survival-Tactical/dp/B0CZQ57TF6
    - Aliexpress example: https://www.aliexpress.us/item/3256803949130763.html
  - For the standard size FV3 Rewinder (23mm Rim Roller face width):
    - Size #84 (3 1/2" length x 1/2" wide) or ~57mm diameter (~90mm length) x 12-13mm width
      - qty 2 per roller for 80mm width version, qty 3 per roller for 100mm width version
    - Amazon example: https://www.amazon.com/dp/B0CBJQLXLB
    
<img src="https://github.com/SkiBikePrint/Filamentalist/blob/71cee20fe18fa942feb86cab2a580b9eeac974d1/Assets/rubber_band_82.jpg" width="300" height="350"><br />
  <br />
    
  [return to index](#filamentalist-frequently-asked-questions)


## Flexible Filament
  - The Filamentalist has been successfully tested with 95A hardness TPU
  - 85A hardness TPU (for example NinjaFlex) - NOT RECOMMENDED! - Soft TPU tends to kink and jam during unload.
  - The smaller/lighter the spool, the better.  The resistance created by the rotational inertia of a heavy spool can cause the Flexibile filament to kink at the o-rings or just expand and jam in the tubing.
    - the little 200/250 gram spools work great.
    - Lower unload acceleration reduces the above problem by reducing the rotational inertia.<br />
  <br />
    
  [return to index](#filamentalist-frequently-asked-questions)
