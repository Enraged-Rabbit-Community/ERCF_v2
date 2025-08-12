<p align="center"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="150" height="150">
<h1 align="center">The Filamentalist "Classic" Passive Filament Driven Rewinder</h1>


<p align="center"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_render2.png" width="250" height="375">]
</p>
   
## [Filamentalist Classic Assembly Guide Document](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/a68bc6678bab41d7bded5e42a17276a9430a0f45/Recommended_Options/Filamentalist_Rewinder/Filamentalist_Classic/Documentation/Filamentalist_Rewinder_Manual_V3.1.2.pdf)  [<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist RC2 Manual_Cover.jpg" width="150" height="100">](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/a68bc6678bab41d7bded5e42a17276a9430a0f45/Recommended_Options/Filamentalist_Rewinder/Filamentalist_Classic/Documentation/Filamentalist_Rewinder_Manual_V3.1.2.pdf)

## [Filamentalist Classic Assembly Guide Video](https://youtu.be/-1cHOcnosxE?si=RZV318OI9f3f_CkE)  [<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist Assembly Video Thumbnail.jpg" width="150" height="100">](https://youtu.be/-1cHOcnosxE?si=RZV318OI9f3f_CkE)

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> **BOM:**

**ATTENTION!! PLEASE READ COMMENTS IN FAR RIGHT COLUMN** (you may need to scroll over in your view)

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm dia. x 80mm Stainless Steel Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8VFSWD, Amazon Alternate https://www.amazon.com/Unifizz-Stainless-Steel-Round-Silver/dp/B09P9MC953?th=1 (sheared ends may need to be cleaned up), Aliexpress https://www.aliexpress.us/item/3256801518620991.html | Undersized shaft (7.93-7.97mm or 5/16" dia) works the best.  100mm length is more available and can extend out of rewinder, you can cut polished 8mm or 5/16" diameter stainless rod to length, or there are stls to make a wider rewinder based on a 100mm axle.  Custom rewinder widths are also possible using the Fusion 360 parametric model and you can cut shaft to whatever length is desired. 8mm (or 5/16") diameter straight stainless tube is also an excellent alternative to solid rods as the are much easier to cut to length. |
|   5   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | MR608-2RS style recommended, but open or  MR608-ZZ style will work |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS, Aliexpress | 8mm Bore, 12mm length, 14.2mm Diameter. Get the "octogonal" style. |
|   1   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | A locking clip is required and can be bought or printed (stl included).  The rubber seal is not needed and should not be installed upon assembly. |
|   2   | O-rings | Metric 3.5x20 (ID) or AS568 Standard size 211, Home Depot #110, Amazon example: https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/, Aliexpress example: https://www.aliexpress.us/item/2255799953260685.html (select correct size) | In the range of 13/16" ID, 1-1/16" OD or ~20mm ID, ~27mm OD, ~3.5mm cross section/cs, Nitrile Butadiene Rubber (NBR or Buna-N)|
|   1   | Spring  | https://www.amazon.com/dp/B076LNJF5Q, Aliexpress | Like in extruders - 304 Stainless Steel,6mm OD,0.6mm Wire Size,7.5mm Compressed Length,15mm Free Length (the stiffer 1mm wire size extruder spring used on CW2 and G2E will also work if you have those on-hand) |                                 |
|   1 | 3mm Heatset Insert | M3x4x5 like these:  https://www.amazon.com/gp/product/B09MCW7ZN5 | Voron standard size | set into the Tensioner Mnt |
|   1   | 3x35mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw anything in the range of 35mm +/- 10mm should work.  If building the alernate reverse access version then a 30mm length is recommended. |
|  2-6  | M3x8 SHCS  |  Stainless Steel Socket Head Screw | for locking rim rollers to 8mm steel axle shaft.  1 to 3 screws per roller Depending on tightness/looseness of Rim Roller center bore |
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation 8/10/12mm lengths will work|
|   3   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation 16mm length will work |
|   1   | M3 Washer  |  Stainless Steel | between Spring Tensioner screw head and spring |
|   4   | Rubber Band | See [FAQ](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FAQ.md#rubber-band-sourcing-options)) | bike tire inner tube or rubber bands |

**Optional Parts**
| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | D2F-L3 Microswitch  | Omron brand - Mouser, Digikey, etc., Aliexpress example: https://www.aliexpress.us/item/3256805036222979.html  | for pre-gate sensor option versions |
|   2   | M2x10 Self Tapping Screw | Philips or socket head.  Amazon example: https://www.amazon.com/DTGN-M2x10mm-Phillips-Self-tapping-Screw/dp/B0CSRTYBLR, Aliexpress example: https://www.aliexpress.us/item/3256802486141312.html (select size) | for pre-gate sensor option versions |
|   1   | JST-XH 2-pin Socket/Plug | Amazon example:  https://www.amazon.com/CQRobot-Connector-Terminals-Housing-Adapter/dp/B0B2R966ZY, Aliexpress Example: https://www.aliexpress.us/item/3256804799083128.html (need housing, plug, and terminal) | for pre-gate sensor option versions |
|   var.   | 24 awg wire  |   | for pre-gate sensor option versions |
| var.  | 2.5mm ID PTFE tubing | Amazon, Aliexpress, 3D printing vendors | 2.5mm ID recommended but you can try whatever you have.  Length depends on the distance from your rewinder location to your ERCF inputs |


## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Printing Guidelines:

## **General:**
- Material: ABS or ASA (~170 gm per site)
- Print Time: ~8hr 17min (based on the Ellis PIF profile speeds, accelerations, and volumes)
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

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Tuning

Tune by setting the Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs rewinder drag and set a slip range in-between the two "imaginary" lines.  Adjust the spring tensioner screw accordingly and err on the light side.  Run the rewinder (see test code below). If loose filament is forming around the filament spool during unload, tighten the spring tensioning screw.  If no loose filament is forming around the filament roll, gradually reduce the spring tension until loose filament starts to accumulate and then increase tension in ~1/2 screw turn increments until you feel you have the lightest tension that results in a tightly packed unload. 

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> O-Ring Replacement

You may never need to replace o-rings.  Testing and extrapolation estimates that the wear-out point is ~5K cycles.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders in your line-up.  Also, o-rings with grooves worn in them can be swapped with their opposing partners to present the unworn side/face to the filament to extend the life of a set.  For o-ring replacement, remove the Drive Roller Assembly from the rewinder (unscrew the (6) screws of the Right and Left Supports).  Then unscrew the set screw on one Rim Roller.  You can now slide the CDR Spacer and Center Drive Roller from the axle, remove the old o-rings (a dental pic works great), and install a pair of new ones.  Reinstall the Center Drive Roller and CDR Spacer back on the axle and install the Rim Roller back onto the axle per 3.3 above, and re-install the supports.  


## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Troubleshooting

Please see [troubleshooting guide](troubleshoot.md), reference the [FAQ](Filamentalist_FAQ.md), or join our discord server (https://discord.gg/uDcGxukRKd) for more help.



# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Version History

Versioning convention.  V"X"."Y"."Z"
- "X" represents a major change in form, fit, or function.  An increment in "X" may not require that existing built units undergo rework but the new parts will generally not be compatible with past version rewinders.
- "Y" represents a "step rev" or minor revision.  These are generally small "tweaks" for improved functionality, useability, and/or assembly and typically would not require reprint/rework for existing rewinders.  
- "Z" represents a backwards compatible "bug fix".  This will generally be addressing nuisance CAD or printability issues.

V1 - 5/17/24 - Public release into ERCF V2 RC2 repository

V1.1 - 5/19/24 - Update to CAD and stls for Tensioner Arms to remove potential filament catching point during endless spool ejection

V1.2 - 5/20/24 - Reverted Center_Drive_Roller to cylindrical press fit hole (vs hex of V1 and V1.1).  Revised 608 press fit pockets of Idler_Roller_(male&female) parts for both 80mm and 100mm width versions for improved press fit.

V1.3 - 5/20/24 - Added bevel to internal step on  Idler_Roller_(male) part for 80mm and 100mm versions to improve printability.  Updated the .f3dparametric file, step files, and stls for 80mm and 100mm versions.

V1.4 - 5/21/24 - Shortened threads on Idler_Roller_male parts by 1.5mm to remove slight interference.  Updated CAD, 80mm, and 100mm stls.

V1.5 - 6/4/24 - Slightly deepened 608 bearing pockets in Idler Roller parts to prevent potential side loading binding due to print/assembly tolerances.  Reprint not required for existing functioning units.

V1.6 - 6/12/24 - No mandatory reprints/rebuilds required:  Updated CAD parametric model and 80/100mm step files because two  Tensioner Mount-to-Support holes were getting "buried" in the 100mm version.  Updated the Tensioner_Mount_100mm stl file as well.

V1.7 - 6/13/24 - Opened up c-sunk hole on Tensioner_Arm_Left part pivot screw hole to allow for full seating of a FHCS head and use of a 16mm long screw.  A new stl for Tensioner_Arm_Left ans new f3d and step files are included.

V1.8 - 7/2/24 - Removed notch/gap in axle pressing tool that shouldn't have been there.  80/100mm stl's updated as well as f3d and stp CAD files.

V2 - 7/22/24
  1. Added Rear Load option Tensioner_Mount (works as bottom load too)
  2. Removed threaded Rim Roller option and converted Rim Rollers from press-fit to set screw style.
  3. Add 608 bearing inner race clearance back into Supports.
  4. Added ~2mm of additional bowden capture in Tensioner_Mounts

V3 - 8/5/24
  1.  Add options for Tensioner Mounts with pre-Gate sensors
  2.  Included option for the Filamentalist Enclosure style Base Supports
  3.  Updated all supports to include a spool guide rail to help keep spools from wandering off of the rollers.

V3.0.1 - 8/8/24 - No reprint/rebuild required:
1. Improved clearances for indexing tab feature in Tensioner Arm parts
2. Improved breakaway feature for small print-in support in Tensioner_Arm_Right part 
3. Provided additional edge chamfering to Idler Roller Axles
4. Reinstated design history in Filamentalist_(parametric)_V3.f3d CAD model so that the parametric functionality would work correctly.
5. Added accent color to file naming convention in stl file names.
6. Updated pdf manual to reflect/describe accent color for file naming convention in stl file names.

V3.0.2 - 8/15/24 - No reprint/rebuild required:
1. Added more reference dimensions to the User Parameters section for the Filamentalist_(parametric).f3d parametric CAD model.
