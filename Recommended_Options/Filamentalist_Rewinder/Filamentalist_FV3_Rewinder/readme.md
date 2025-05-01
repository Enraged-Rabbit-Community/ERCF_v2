## WORK IN PROGRESS! ##

<h1 align="center">The "Filamentalist V3"   <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="150" height="150">   Passive Filament Driven Rewinder</h1>
<p align="center">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/3c9f6ff0488cfe39d422b2b4c9527ab92d81b29c/Recommended_Options/Filamentalist_Rewinder/Filamentalist_V3_beta/Assets/Filamentalist_V3_Render_Large.png" width="700" height="600">
</p>

## [Filamentalist FV3 Assembly Guide Document](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/4648ff0c2f5a9ee3f4b7aded86e414564832cd24/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3/Documentation/Filamentalist_V3_Manual_V1.0.pdf)  [<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/d2b144ee8d95d24b84439ef060b2681a3b5932ac/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3/Assets/FV3%20Manual.png" width="150" height="100">](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/d2b144ee8d95d24b84439ef060b2681a3b5932ac/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3/Assets/FV3%20Manual.png)
## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> **BOM:**

**ATTENTION!! PLEASE READ COMMENTS IN FAR RIGHT COLUMN** (you may need to scroll over in your view)

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm dia. x ##mm Stainless Steel Rod, Tube, or Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8T7ZQB?th=1, Aliexpress https://www.aliexpress.us/item/2255800287548941.html (select M8x70mm) | Undersized shaft (7.93-7.97mm or 5/16" dia) works the best.  50mm axles will work in the standard width design but longer axles cut to length (up to ~75mm) will provide greater stability for the Rim Rollers.  The Classic Filamentalist 80mm axles will work but hang over ~1mm per side.  Custom rewinder widths are possible using the Fusion 360 parametric model and you can cut shaft to whatever length is desired.  8mm (or 5/16") diameter straight stainless tube is also an excellent alternative to solid rods as they are much easier to cut to length like https://www.amazon.com/uxcell-Stainless-Thickness-Seamless-Straight/dp/B081GBTQGC or https://www.aliexpress.us/item/3256805495613016.html. |
|   1   | 688 bearing | For Tensioner Arm|
|   4   | 608 bearings | For Drive and Idler axles.  Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | MR608-2RS style recommended, but open or  MR608-ZZ style will work |
   OR:
|   4   | 688 bearings | As an alternative to the 608 bearings for Drive and Idler axles, so would be a total of 5 688 bearings including the Tensioner Arm bearing.  This allows for only needing to buy one bearing size but the 688's might be a tighter fit on the axle shafts.|
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS, Aliexpress | 8mm Bore, 12mm length, 14.2mm Diameter. Get the "octogonal" style. |
|   1   | ECAS04   |  | Press-in pneumatic fitting for the bowden tubes (like used in ERCF).  A locking clip is required and can be bought or printed (stl included).  The rubber seal is not needed and should not be installed upon assembly. |
|   2   | O-ring | Metric 3.5x20 (ID) or AS568 Standard size 211, Home Depot #110, Amazon example: https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/, Aliexpress example: https://www.aliexpress.us/item/2255799953260685.html (select correct size) | In the range of 13/16" ID, 1-1/16" OD or ~20mm ID, ~27mm OD, ~3.5mm cross section/cs, Nitrile Butadiene Rubber (NBR or Buna-N)|
|   1   | Spring  |  https:https://www.amazon.com/dp/B076LNJF5Q, Aliexpress https://www.aliexpress.us/item/3256805126192641.html (select size per comments) | 304 Stainless Steel,6mm OD,0.6mm Wire Size,7.5mm Compressed Length,15mm Free Length |                                 |
|   1 | 3mm Heatset Insert | M3x4x5 like these:  https://www.amazon.com/gp/product/B09MCW7ZN5 | Voron standard size | set into the Tensioner Mnt |
|   1   | M3x30mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw |
|  6-10  | M3x12-16mm SHCS  |  12-16mm length will work | for locking rim rollers to 8mm steel axle shaft.  1 to 3 screws per roller Depending on tightness/looseness of Rim Roller center bore.  4 additional screws if using the Filamentalist Enclosure Mounts |
|  4  | M3x12 FHCS  |  Flat Head Cap Screw | for Idler Roller wheels, Tensioner Bearing axle, and Tensioner Pivot |
|   12-14   | M3x8mm FHCS  |  Stainless Steel Flat Head Cap Screw | Qty 12 for 2020 center mount, 14 for Enclosure mount |
|   1   | M3 Washer  |  Stainless Steel | for Spring Tensioner screw |
|   4   | #84 Rubber Band | See [FAQ](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/f4b36f50e9c2cce9561285ea40eadc532c116dd9/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FAQ.md) | 2" bike tire inner tube cut to width or rubber bands |

**Parts for Microswitch Option**
| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | Omron D2F-01FL-D3 Lever Microswitch | https://www.mouser.com/ProductDetail/Omron-Electronics/D2F-01FL-D3?qs=i1w9Bv2NFd2YXdp4zNwbgA%3D%3D  | For pre-gate sensor levered switch option. |
   OR:
|   1   | Omron D2F-01F-D3 Button Microswitch | https://www.mouser.com/ProductDetail/Omron-Electronics/D2F-01F-D3?qs=i1w9Bv2NFd2sPdBLm34BPQ%3D%3D  | For pre-gate sensor printed lever switch option. |
|   1   | MR85 Bearing | Amazon: https://www.amazon.com/dp/B07CKL54RS, Aliexpress: https://www.aliexpress.us/item/3256807026256776.html   | ZZ, RS, or open style will work.  For pre-gate sensor switch option. |
   OR:
|   1   | 8x3 Disc Magnet | Amazon: https://www.amazon.com/FINDMAG-Magnetic-Whiteboard-Refrigerator-Magnets-8x3mm/dp/B0863BGG6H, Aliexpress: https://www.aliexpress.us/item/3256806495856656.html   | For pre-gate sensor switch option. |
   OR:
|   1   | 6x3 Disc Magnet | Amazon: https://www.amazon.com/TRYMAG-Magnets-Refrigerator-Whiteboard-Neodymium/dp/B09QHSB2XM, Aliexpress: https://www.aliexpress.us/item/3256807048616464.html   | For pre-gate sensor switch option. |  
|   var.   | 24 awg wire  |   | for pre-gate sensor option versions |
|   2   | M2x8mm SHCS |  Amazon:  https://www.amazon.com/Alloy-Steel-Socket-Screws-Black/dp/B015A37DVU, Aliexpress:  https://www.aliexpress.us/item/3256806889548681.html | Self tapping screws can be used as an alternative |
| 2  | Male/Female connectors |  | Connectors of your choice, JST-XH 2-pin works well |

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Printing Guidelines:

## **General:**
- Material: ABS or ASA (2020 Center Mount version: ~154gm per site, Filamentalist Enclsoure Mount Version: ~175gm per site)
- Print Time: 2020 Center Mount version: ~7hr 34min, Filamentalist Enclsoure Mount Version: ~9hr 10min (based on the Ellis PIF profile speeds, accelerations, and volumes)
- 0.2mm layer height
- 40% infill recommended.  Linear style infills are fastest (rectilinear, monotonic, grid, triangles, stars, etc.)
- Wall Count: 4
- Solid Top/Bottom Layers: 5

## **Part Specific:**
- Orientation suggestions are relative to the installed assembly orientation and are shown in the slicer images below.
- There are stls for both 80mm and 100mm wide version and a Fusion 360 parametric CAD model for additional custom widths.  See "Additional Notes/Considerations" point 3 above for more details.
- If rotating the Filamentalist is not feasible for your required filament loading direction or you need a bottom feed capability (for example enclosure limitations or feeding through the bottom of a shelf) there is an option for a rear loading version which only requires printing the Tensioner_Mount_Rear_Load_80mm/100mm_[option] in the place of Tensioner_Mount_80mm/100mm part.
  
  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/rear_load_option.jpg" width="350" height="175">

- Stl's are provided for optional clip-in style supports where no Base_Plate is needed and the rewinders are easily clipped in and out of (2) 2020 extrusions mounted 170mm center-to-center apart.  This option is highly recommeded if your setup can accomodate this style type of mount.
  
  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Clip-In_Supports.jpg" width="250" height="175">
- **!! IMPORTANT !!  This design relies on multiple press-fits for bearings and ECAS fittings.  As a result, printer calibration is important.  A Test_Block stl is included.  It is highly recommended that you print this block first, check fits, and make adjustments to extrusion multipliers and/or slicer scaling if needed before printing the Filamentalist parts.**
  
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Logo.png" width="200" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Sliced_(Black)_1.jpg" width="375" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Sliced_(Orange)_1.jpg" width="375" height="300">


| **Qty per Site** | **Part**  | **Pic** |  **Orientation**            | **Printed Supports Needed** | **Comments** |
|------|-----------------------------------------|------------|--------------------|-----|---------------------------------|
| 1       | Right_Support | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Right_Support.jpg" width="40" height="40"> |  Horizontal                   | N     |                                  |
| 1       | Left_Support | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Left_Support.jpg" width="40" height="40">                                                            | Horizontal                   | N     |                                  |
| 1       | Option: Right_Support_[2020_Clip-In_option] | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Right_Support(2020-Clip-In).jpg" width="50" height="30"> |  Horizontal                   | N     |                                  |
| 1       | Option: Left_Support_[2020_Clip-In_option] | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Left_Support(2020_Clip-in).jpg" width="50" height="30">                                                            | Horizontal                   | N     |                                  |
| 1       | Base_Plate_80mm/100mm_[option] | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Base.jpg" width="40" height="40">                                                            | Horizontal                   | N     | Optional part for a standalone unit not mounted to another surface  |
| 1       | Idler_Roller_Axle_80mm/100mm  | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Rear_Roller_Axle.jpg" width="40" height="40"> | Horizontal | N | align flat of "D" to build plate |
| 2       | [a]_Rim_Roller_80mm/100mm | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Rim_Roller.jpg" width="40" height="40">                                                   | Horizontal                | N       | Dished side up.   |
| 1       | [a]_Center_Drive_Roller  | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Center_Drive_Roller.jpg" width="40" height="40">                                                        | Horizontal                 | N        | Recommend scattered seams for press fit-bore concentricity |
| 2       | CDR_Spacer_80mm/100mm |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Center_Drive_Roller_Spacer.jpg" width="40" height="40">    | Horizontal                 | N        |                             |
| 1       | Tensioner_Arm_Left |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Arm_Left_1.jpg" width="40" height="40"> | Horizontal                          |  N    |  |
| 1       | Tensioner_Arm_Right |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Arm_Right_1.jpg" width="40" height="40"> | Horizontal                          |  Built-in     | Remove built-in support from the locking tab |
| 1       | [a]_Tensioner_Mount_80mm/100mm | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Mnt_printed.jpg" width="40" height="40">                           | Vertical (as installed)                | N  | There is a pre-gate sensor option version available as well (split to parts in slicer for print-in-place breakaway connector retaining key).  |
| 1       | [a]_Tensioner_Mount_Rear_Load_80mm/100mm _[option] | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/f2f9d9bb04fad333333788b4d2238f26b38bbf62/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Mount_Rear_Load.jpg" width="60" height="30">                           | Vertical (as installed).  Optional for rear loading if needed.               | N  | There is a pre-gate sensor option version available as well.  |
| 1       | [a]_Idler_Roller _(male) _80mm/100mm   | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Idler_Roller_(male).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1       | [a]_Idler_Roller _(female)_80mm/100mm   | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Idler_Roller_(female).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1    | Axle_Depth_Tool_80mm/100mm | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Axle_Pressing_Tool.jpg" width="40" height="40"> | Vertical | N | Pocket opening up.  Print with 100% infill for reuse strength and durability when building multiple rewinders. |
| 2 | [a]_ECAS_Clip | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/ECAS_Locking_Clip.jpg" width="40" height="40"> |  Horizontal | N | Tab up |
| 1 | Test_Block | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/test_block.jpg" width="40" height="40"> |  608 Pocket facing up | N | printer calibration tool |



## Assembly Tips: ##

