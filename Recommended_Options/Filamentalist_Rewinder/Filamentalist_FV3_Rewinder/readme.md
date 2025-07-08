<p align="center"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="150" height="150">
<h1 align="center">The Filamentalist V3 ("FV3") Passive Filament Driven Rewinder</h1>
<p align="center">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/FV3/FV3_with_Spool.PNG" width="300" height="400">
</p>

## [FV3 Assembly Guide Document](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3_Rewinder/Documentation/Filamentalist_V3_Manual_V1.1.1.pdf)  [<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/FV3/FV3%20Manual.png" width="150" height="100">](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3_Rewinder/Documentation/Filamentalist_V3_Manual_V1.1.1.pdf)
## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/FV3/FV3%20Manual.png" width="50" height="60"> **BOM:**

**ATTENTION!! PLEASE READ COMMENTS IN FAR RIGHT COLUMN** (you may need to scroll over in your view)

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm dia. x ##mm Stainless Steel Rod, Tube, or Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8T7ZQB?th=1, Aliexpress https://www.aliexpress.us/item/2255800287548941.html (select M8x70mm) | Undersized shaft (7.93-7.97mm or 5/16" dia) works the best.  50mm axles will work in the standard width design but longer axles cut to length (up to ~75mm) will provide greater stability for the Rim Rollers.  The Classic Filamentalist 80mm axles will work but hang over ~1mm per side.  Custom rewinder widths are possible using the Fusion 360 parametric model and you can cut shaft to whatever length is desired.  8mm (or 5/16") diameter straight stainless tube is also an excellent alternative to solid rods as they are much easier to cut to length like https://www.amazon.com/uxcell-Stainless-Thickness-Seamless-Straight/dp/B081GBTQGC or https://www.aliexpress.us/item/3256805495613016.html. |
|   1   | 688 bearing | For Tensioner Arm|
|   4   | 608 bearings | For Drive and Idler axles.  Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | Inexpensive MR608-2RS rubber dust seal style is recommended as they are slightly higher resistance than the open or ZZ metal seal style. You actually want a little of resistance in the axle bearings to help the 1-way bearing unlock. |
   OR:
|   4   | 688 bearings | As an alternative to the 608 bearings for Drive and Idler axles, so would be a total of 5 688 bearings including the Tensioner Arm bearing.  This allows for only needing to buy one bearing size but the 688's might be a tighter fit on the axle shafts.  Inexpensive MR688-2RS rubber dust seal style is recommended as they are slightly higher resistance than the open or ZZ metal seal style. You actually want a little of resistance in the axle bearings to help the 1-way bearing unlock. |
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
|   4   | #84 Rubber Band | See [FAQ](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FAQ.md#rubber-band-sourcing-options) | 2" bike tire inner tube cut to width or rubber bands |

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
- Material: ABS or ASA (2020 Center Mount version: ~154gm per unit, Filamentalist Enclsoure Mount Version: ~175gm per unit)
- Print Time: 2020 Center Mount version: ~7hr 34min, Filamentalist Enclsoure Mount Version: ~9hr 10min (based on the Ellis PIF profile speeds, accelerations, and volumes)
- 0.2mm layer height
- 40% infill recommended.  Linear style infills are fastest (rectilinear, monotonic, grid, triangles, stars, etc.)
- Wall Count: 4
- Solid Top/Bottom Layers: 5

- Recommended orientation is set in the stl files and should load correctly into slicer programs.  Print orientation is shown below in the slicer plate pictures for base and accent color parts.
- Where applicable, stl's are provided for two different axle bearing types, 688 (16mm OD) and 608 (22mm OD) bearings.  Bearing size is denoted in the file naming.
- **!! IMPORTANT !!  This design relies on multiple press-fits for bearings and ECAS fittings.  As a result, printer calibration is important.  The Print_Calibration_Tool_###_Bearing.stl file is included.  It is highly recommended that you print this part first, check fits, and make adjustments to extrusion multipliers and/or slicer scaling if needed before printing the Filamentalist parts.**
   - Other materials such as PETG or PLA may work fine but parts were not designed or validated for these materials.  If you want to use a different material start with the Print Calibration Tool and adjust extrusion rates and slicer scaling to achieve the correct dimensions for the press fit parts.

  
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/abbbd81a78ae753106748c35d51503875ee82a7b/Recommended_Options/Filamentalist_Rewinder/Assets/FV3/Slicer_Plate_Base_Color.png" width="375" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/abbbd81a78ae753106748c35d51503875ee82a7b/Recommended_Options/Filamentalist_Rewinder/Assets/FV3/Slicer_Plate_Accent_Color.png" width="375" height="300">

