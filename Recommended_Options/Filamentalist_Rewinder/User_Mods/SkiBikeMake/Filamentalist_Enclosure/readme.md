# The "Filamentalist" Enclosure # 

The Filamentalist Enclosure is a passive dry box designed to house the Filamentalist passive rewinder.  It  consists of (4) printed endcaps, (6) pieces of 2020 extrusion cut/ordered to the desired length, and 0.060" (1/16') polycarbonate sheet(s) cut to size. 

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240619_221414.jpg" width="475" height="425">
</p>

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240615_221926.jpg" width="475" height="600">
</p>

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240615_221938.jpg" width="475" height="600">
</p>

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240615_222004.jpg" width="475" height="475">
</p>

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240615_222014.jpg" width="475" height="475">
</p>

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/da3dacf4f50ca5de08879cdd9d0642990da49a36/Filamentalist_Enclosure/Assets/20240615_222119.jpg" width="475" height="475">
</p>

BOM:

- 2020 Extrusion - Qty 6 - Select/cut length to be greater than or equal to [Rewinder Qty] X [Rewinder Width] + 10mm
    - for example: 6 X 81.5 (std. Filamentalist Width) + 10 = 499mm.  Round up to a standard 500mm long 2020 extrusion
    - get extrusions with holes that can be tapped to a 5mm thread (like the Misumi with a 4.2mm D hole)
    - examples: https://www.amazon.com/dp/B09DYMCBYF, https://www.aliexpress.us/item/3256801651139612.html

- Polycarbonate Sheet (Lexan) - 1/16" (or 0.060") thick.  Width of pieces = Extrusion Length -2mm (i.e. cut sheet to 498mm wide if using 500mm extrusions)
    - Lid Length = 451.5mm
    - Base Rear Panel Height = 120mm
    - Base Front Panel Height = 45mm
    - Bottom Panel Length (if used) = 230mm
    - For enclosures up to 607.6mm wide a single 24" x 36" sheet is enough material.  (2) 24" x 24" or (1) 24" x 24" + (2) 12" x 24" sheets will work as well if it is easier for you to source smaller sheets.

- Seal Material - ~10m or 32ft of 3/8" wide x 1/4" high (9mm x 6mm) self-adhesive weather seal.  Something like this:  https://www.homedepot.com/p/M-D-Building-Products-17-ft-Black-Small-Rubber-Auto-Marine-Weatherseal-for-All-Climates-01025/202066509, or https://www.amazon.com/Insulation-Weatherproof-Soundproofing-Self-Adhesive-Weatherstrip/dp/B082HDZ1P1?th=1, or https://www.aliexpress.us/item/3256806396445681.html.  Most of the glue needs to be peeled off so you want the style that has the "strings" embedded in the glue to aid in removal.

- M5x10/12mm length BHCS or SHCS - Qty 6 - For securing end caps to extrusions.  BHCS (Button Head) looks the best.

- M5 10mm length BHCS - Qty 4 - for mounting hinges to base and lid frames

- M5 x 16/18/20mm length BHCS - Qty 2 - Hinge Pin Screws.

- M3 x 4/5mm length BHCS or SHCS - Qty 2 - for tying lid panel to lid endcaps.

- 5mm Heatset Insert - Qty 2 - Optional, for setting how far the lid hinges back.

- M5 x 8/10mm length SHCS - Qty 2 - Optional, for setting how far the lid hinges back.

There is room, and some special "far left" and "far right" extended supports that allow you to build one ~94mm wide Filamentalist unit using the parametric model to support a wider spool like KVP or NinjaFlex.

**Assembly Tips:**

**Lid Panel Installation:** The 0.060" Lexan bends easily but it is not easy to bend it and get it captured in the lid endcaps and extrusions.  Its a two person job. If doing it alone and use 2 or 3 loops of string set at the right length to hold the correct bend and spacing at the edges of the Lexan.  Secure the non-captured end of the extrusions with a loop of strip or tape so that you don't overflex and crack the endcap that is screwed on while wrestling this thing together.

**Seal Installation:**

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f93ed33f1c8511d502d34e729206b746fa133d2f/Filamentalist_Enclosure/Assets/Seal_Install_1.jpg" width="475" height="475">
</p>
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f93ed33f1c8511d502d34e729206b746fa133d2f/Filamentalist_Enclosure/Assets/Seal_Install_2.jpg" width="475" height="475">
</p>
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f93ed33f1c8511d502d34e729206b746fa133d2f/Filamentalist_Enclosure/Assets/Seal_Install_3.jpg" width="475" height="475">
</p>
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f93ed33f1c8511d502d34e729206b746fa133d2f/Filamentalist_Enclosure/Assets/Seal_Install_4.jpg" width="475" height="475">
</p>
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f93ed33f1c8511d502d34e729206b746fa133d2f/Filamentalist_Enclosure/Assets/Seal_Install_5.jpg" width="475" height="475">
</p>

**Securing/Sealing on Printer:**

For a Voron enclosure you can "straddle" the top panel like the pic below.  Drill 2 countersunk holes in the top panel and screw them into t-nuts in the bottom enclosure extrusion.  The screw heads sit just below the panel surface so that the bowden tube doesnt catch on them while the print head is zooming around.   Run seal material in the rear bottom extrusion channel of the enclosure. Cut out sections of the weather stripping base to make space for the t-nuts to sit under but leave a continuous piece of weatherstripping seal running over the top of the t-nuts.  You can stick toothpicks into the t-nut holes (or 3mm screws with the heads cut off) to serve as locating pegs when you drop the enclosure onto the printer to make sure the top panel holes align with the t-nut locations.  This will pull  the top panel against the seal and is enough to secure the enclosure in place on the printer.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/bb7fdd7f198937ab097e0a71e6ffcc328b678437/Filamentalist_Enclosure/Assets/Base_Attachment.jpg" width="950" height="475">
