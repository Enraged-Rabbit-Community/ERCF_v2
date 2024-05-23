<h1 align="center">The "Filamentalist"   <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="150" height="150">   Passive Filament Driven Rewinder</h1>
<p align="center">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_render.png" width="350" height="475">
</p>
<p align="center"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Front.jpg" width="350" height="300">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Top.jpg" width="300" height="300"><img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_6_Color.jpg" width="350" height="300">
</p>

See video of 6 rewinders swapping here (plus Trident Blobifier):  [Filamentalist X6](https://photos.app.goo.gl/hKso7JYPZcdRLKrW8)

# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Theory of operation:
The Filamentalist uses the axial force delivered by the ERCF gear motor along the filament to load and unload to/from the filament spool.  An adjustable spring clamp forces the filament against two o-rings that sit on the drive pulley to create a high traction interface.  A one-way clutch style bearing locks against the drive shaft and rotates the filament spool to take up filament during an unload.  For loading and print extruding, the clutch disengages allowing for effective free-spooling of the filament spool simliar to a roller style spool holder.  For unloading/buffering, some slip will occur between the filament and the o-ring interface and/or the spool rim and the rim roller of the rewinder to account for the varying diameter range of a spool from full to empty (full spool = max slip, empty spool = no/minimal slip).

<p align="center">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist6_1.jpg" width="400" height="465">
</p>

# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Credits:
Discord user Thisiscam first made me aware of Muzi Xiaoyang's video of a filament driven rewinder (https://www.bilibili.com/video/BV1ZM41197fX/?spm_id_from=333.337.search-card.all.click).  Through a long collaboration with Thisiscam, many design iterations/improvements on the Muzi Xiaoyang design, and a great Beta test team the Filamentalist was born. 

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> **Additional Notes/Considerations** 

This rewinder is "almost" perfect, but not completely perfect.  Things that you need to know include:
1. The ERCF gear stepper is doing the heavy lifting.  Configure your gear stepper to run in sync mode with your extruder via Happy Hare settings.
2. A high torque NEMA 17 motor is recommended.  Many in the Beta team ran NEMA 17's spec'd at 55 N-cm max torque and config'd them for 1-1.4A.  Grafton's 40 tooth NEMA 17 mod is recommended (https://www.printables.com/model/692720-ercf-40-tooth-gear-modifiction).  This may not be required so if you already have built your ERCF, try the Filamentalist with the motor you have and decide if you think you need more torque.
3. Several in the Beta team had space constraints that they wanted the rewinder to honor.  As a result, one baseline width of the Filamentalist was set to use a 80mm axle length.  It has a maximum spool width of 68mm and supports most standard 1, 0.5, and 0.25KG spool sizes and still be able to fit 6 rewinders across a 350 size Voron printer. Height was set to be as low as possible to fit some existing dry box designs although there is the possibility to make user modifications to to reduce height further if needed. Some spools such as KVP's are too wide to fit the 80mm design.  If you use spools wider than 68mm there is also stl files posted for a 100mm axle length version. If you are using Autodesk Fusion 360 the provided .f3d file in the CAD directory is a parametric based model allowing you to customize the width of your rewinder to suit your max/min spool widths and/or to design around a standard available steel axle length (see instructions here  [parametric_model](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/CAD/readme.md) ). 
4. Because the standard tuning of this design relies on some filament slip at the o-rings, the o-rings will ultimately wear-out.  Testing and extrapolation estimates that the wear-out point is ~5K cycles.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders in your line-up.  Also, o-rings with grooves worn in them can be swapped with their opposing partners to present the unworn side/face to the filament to extend the life of a set.  See section 3.2 of the Drive Roller Assembly section for o-ring swap/replacement instructions. 
5. Due to pressfits for the 608 bearings, 8mm axle, and ECAS, printer calibration is important.  A "Test Block" stl is included.  It is recommended you print this first and test the press fits and measure the two small holes (2.7mm for cutting 3mm screw threads and 2.3mm for the filament path) to determine if you need to apply any scaling or changes to your extrusion factors in your slicer before printing.  Due to varying ECAS supplier tolerances and varying printer tolerances some experienced cracking at the ECAS hole when pressing in the ECAS.  If all other press fits work well on the Test Block but you experience cracking at the ECAS hole when pressing in an ECAS fitting, you can use an Xacto knife to lightly remove some plastic from the ECAS hole.  If the ECAS is too loose you can use superglue to glue the ECAS into the Tensioner Mount (not the Test Block 😉 ).
6. Questions and input can be directed to the Filamentalist Discord group here:  (https://discord.com/invite/H9yuhrXTEq)

## <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> **BOM:**

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm dia. x 80mm Stainless Steel Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8VFSWD, Amazon Alternate https://www.amazon.com/Unifizz-Stainless-Steel-Round-Silver/dp/B09P9MC953?th=1 (sheared ends may need to be cleaned up), Aliexpress https://www.aliexpress.us/item/3256801518620991.html | Undersized shaft (7.93-7.97mm dia) works the best (5/16" dia).  100mm length is more available and can extend out of rewinder or cut polished 8mm or 5/16" diameter stainless rod to 80mm lengths, or there are stls to make a wider rewinder based on a 100mm axle.  Custom rewinder widths are also possible using the Fusion 360 parametric model and you can cut shaft to whatever length is desired. |
|   5   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | MR608RS, MR608ZZ, etc. |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS, Aliexpress | 8mm Bore, 12mm length, 14.2mm Diameter. Get the "hex" style. |
|   1   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | A locking clip is required and can be bought or printed (stl included) |
|   2   | O-rings | AS568 Standard size 211, Home Depot #110, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/, Aliexpress | In the range of 13/16" ID, 1-1/16" OD or ~20mm ID, ~26mm OD (~3mm cross section/cs), Nitrile Butadiene Rubber (Buna-N)|
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/, Aliexpress | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   1 | 3mm Heatset  | M3x4x5 like these:  https://www.amazon.com/gp/product/B09MCW7ZN5 | Voron standard size | set into the Tensioner Mnt |
|   1   | 3x35mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw anything in the range of 35mm +/- 10mm should work.  If building the alernate reverse access version then a 40-50mm length is recommended. |
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation 8/10/12mm lengths will work|
|   3   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation 16mm length will work |
|   2   | Rubber Band | https://www.amazon.com/dp/B0CPJPN41V , Aliexpress https://www.aliexpress.us/item/3256804772787208.html (120x20mm) | Size #94 (3 1/2" x 3/4"), any wide rubber bands in the 2.5"-3.5" size will work.  Can combine multiples across face of rollers.  Another excellent alternative is to cut bands from a bicycle inner tube.  Mountain bike or "balloon" tire sized tubes for tires in the 1.75"-2.4" width work well.  Cut at ~30-35% wider than face of Rim Roller. |
| var.  | 2.5mm ID PTFE tubing | Amazon, Aliexpress, 3D printing vendors | 2.5mm ID recommended but you can try whatever you have.  Length depends on the distance from your rewinder location to your ERCF inputs |


# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Printing Guidelines:

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
- There is the option to include a threaded Rim Roller to support O-Ring replacement.  This is like not needed for most people.  See "Drive Roller Assembly" section 3.2 below for more detail.
- Stl's are provided for optional clip-in style supports where no Base_Plate is needed and the rewinders are easily clipped in and out of (2) 2020 extrusions mounted 170mm center-to-center apart.  This option is highly recommeded if your setup can accomodate this style type of mount.
  - <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Clip_Mount_Version.jpg" width="280" height="175">
- **!! IMPORTANT !!  This design relies on multiple press-fits for bearings, axles, and ECAS fittings.  As a result, printer calibration is important.  A Test_Block stl is included.  It is highly recommended that you print this block first, check fits, and make adjustments to extrusion multipliers and/or slicer scaling if needed before printing the Filamentalist parts.**
  
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Logo.png" width="200" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Sliced_(Black)_1.jpg" width="375" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Sliced_(Orange)_1.jpg" width="375" height="300">


| **Qty per Site** | **Part**  | **Pic** |  **Orientation**            | **Printed Supports Needed** | **Comments** |
|------|-----------------------------------------|------------|--------------------|-----|---------------------------------|
| 1       | Right_Support | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Right_Support.jpg" width="40" height="40"> |  Horizontal                   | N     |                                  |
| 1       | Left_Support | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Left_Support.jpg" width="40" height="40">                                                            | Horizontal                   | N     |                                  |
| 1       | Base_Plate | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Base.jpg" width="40" height="40">                                                            | Horizontal                   | N     | Optional part for a standalone unit not mounted to another surface  |
| 1       | Idler_Roller_Axle  | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Rear_Roller_Axle.jpg" width="40" height="40"> | Horizontal | N | align flat of "D" to build plate |
| 2 (1)       | Rim_Roller | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Rim_Roller.jpg" width="40" height="40">                                                   | Horizontal                | N       | Dished side up.  Print 1 if you choose to use 1 Rim_Roller_(Threaded) (see next line below) |
| 0 (1)       | Rim Roller (Threaded) | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Rim_Roller_(Threaded).jpg" width="40" height="40">                                                   | Horizontal                | N       | Optional - print if you want the ability to replace o-rings without pressing a roller off of the axle. Dished side up, recommend scattered seams for improved thread perfromance, clean out support web in center splined hole with Xacto knife |
| 0 (1)       | Rim_Roller_Hub (Threaded) | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Rim_Roller_Hub_(Threaded).jpg" width="40" height="40">                                                   | Horizontal                | N       | Optional - print if you want the ability to replace o-rings without pressing a roller off of the axle. Recommend scattered seams for improved thread performance. |
| 1       | Center_Drive_Roller  | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Center_Drive_Roller.jpg" width="40" height="40">                                                        | Horizontal                 | N        | Recommend scattered seams for press fit-bore concentricity |
| 2       | CDR_Spacer |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Center_Drive_Roller_Spacer.jpg" width="40" height="40">    | Horizontal                 | N        |                             |
|         | Tensioner_Arm_Left |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Arm_Left_1.jpg" width="40" height="40"> | Horizontal                          |  N    |  |
|         | Tensioner_Arm_Right |  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Arm_Right_1.jpg" width="40" height="40"> | Horizontal                          |  Built-in     | Remove built-in support from the locking tab |
| 1       | Tensioner_Mount | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Mnt_printed.jpg" width="40" height="40">                           | Vertical (as installed)                | N  |   |
| 1       | Idler_Roller_(male)   | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Idler_Roller_(male).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1       | Idler_Roller_(female)   | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Idler_Roller_(female).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1    | Axle_Pressing_Tool | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Axle_Pressing_Tool.jpg" width="40" height="40"> | Vertical | N | Pocket opening up.  Print with 100% infill for reuse strength and durability when building multiple rewinders. |
| 2 | ECAS_Clip | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/ECAS_Locking_Clip.jpg" width="40" height="40"> |  Horizontal | N | Tab up |
| 1 | Test_Block | <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Test_Block.jpg" width="40" height="40"> |  608 Pocket facing up | N | printer calibration tool |


# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Assembly Instructions:

# 1. Tensioner Mount Assembly

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Mnt.jpg" width="400" height="350">

   - 1.1 Install 3mm heatset insert into Tensioner Mnt.
   - 1.2 Remove the rubber seal from the ECAS fitting.
   - 1.3 Install the ECAS fitting into the Tensioner Mnt.  It should be a moderate press-in.  You may need to push it in firmly using the end of a 8mm steel shaft or printed rear axle shaft to get it to sit flush to the Tensioner Mnt mating surface.  The sidewalls of this hole are relatively thin.  Varying ECAS and print tolerances could result in the sidewall cracking.  If this happens, use superglue around the ECAS and crack.

# 2. Tensioner Arm Installation

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Assy.jpg" width="400" height="350">

   - 2.1 Lay the Tensioner Arm Right part on a flat surface.  Slide the 608 bearing onto the bearing post.  Place the Tensioner Arm Left part into the 608 bearing and rotate against the Tensioner Arm Right part making sure the alignment tab seats correctly at into the pocket at the bottom of the Tensioner Arm Right part.
   - 2.2 Place a 3x18 FHCS (or x16, x12) through the bearing mount hole of the Tensioner Arm Left part and moderately tighten the screw into the Tensioner Arm right piece.  Once installed verify that the bearing turns freely.
   - 2.3 Place a 3x18 FHCS (or x16, x12) through the hole in the Tensioner Arm Left part at the "nose" end and moderately tighten the screw into the Tensioner Arm right piece.  
   - 2.4 Install the Tensioner Arm onto the Tensioner Mnt using a 3x18mm FHCS screw (or x16) .  Tighten until snug and then back off until the arm rotates freely on the mount.
   - 2.5 Place an M3 washer followed by the spring onto an M3x35 SHCS (or x30, x40) and slide through the slotted hole in the bottom of the arm assembly.  Screw the SHCS into the heatset insert of the Tensioner Mnt.  No tension should be on the spring at this point.
       - 2.5.1 ALTERNATE INSTALLATION:
                If the orientation of your Filamentalist makes it difficult to access the tension adjustment screw you can use a 50mm long 3mm SHCS coming from the bowden side of the rewinder with a lock nut, nut with loctite, or a heatset with loctite on the other end as shown in the image below.  
<p align="center">
<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Tensioner_Screw_(alternate).jpg" width="400" height="350">
</p>

# 3. Drive Roller Assembly

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Center_Drive_Roller_with_1-Way_Bearing.jpg" width="300" height="300">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Drive_Roller_Assembly_1.jpg" width="650" height="400">

- 3.1 Press HF081412 One-Way Bearing into Center Drive Roller.  Orientation does not matter at this point.
- 3.2 Install first Rim Roller
    - 3.2.1 For Rim Roller (Threaded) option:

The purpose of this two-piece roller is to allow for future o-ring replacement by removing the Rim Roller from the Hub versus having to press a roller off of the axle and then press it back on.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders in your line-up.  Also, o-rings with grooves worn in them can be swapped with their opposing partners to present the unworn side/face to the filament to extend the life of a set.  To swap o-rings, remove the Drive Roller Assembly from the rewinder (unscrew the (4) screws that attach Right and Left Supports to the Tensioner Mount).  There is no need to diassassemble the Drive Roller assembly.  Use a tool like a dental pick to lift one o-ring and stretch over the top of the other, then push the lower o-ring into the vacated position, and finally push the first o-ring into its new home.

For o-ring replacement, remove the Drive Roller Assembly from the rewinder (unscrew the (6) screws of the Right and Left Supports).  Then unscrew the Rim Roller from the Rim Roller Hub.  If you chose not to use the threaded Rim Roller option youwill need to pull on Rim Roller off of the Axle.  You can now remove the old o-rings and install a pair of new ones, screw the Rim Roller back onto the Hub, and re-install the supports.  This option is recommended if you expect to run a high number of swaps (5K+) over fairly short periods of time as the o-rings will eventually wear out.

  -
    - 3.2.1.1 The optional Rim Roller (Threaded) part has a support web that spans the splined press-fit hole to aid in overhang print quality.  Clean out this web an Xacto knife (or equivalent).
    - 3.2.1.2 Screw the optional Rim Roller Hub (Threaded) part into the Rim Roller (Threaded) part until they are flush with each other.  You may need to use a tool like a flat bladed screwdriver inserted into the hub splines for initial threading.  If threading is excessively tight, thread the hub in and out of the roller multiple times blowing out any debris until there is only light-to-moderate resistance on the threads and then screw the Rim Roller tightly onto the Hub.  You want the resistance of the threads to be less than the resistance of the press-fit of the hub against the shaft so that the roller can be removed from the hub later as needed.  Place the roller onto the Axle Pressing Tool as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Roller assembly until the shaft bottoms-out on the pocket in the Axle Pressing Tool.  If tapping the shaft in, you will hear a change in the pitch of the "thud" when the shaft reaches the floor of the Axle Pressing Tool.

    - 3.2.2 For standard (non-threaded) Rim Roller option:
        - 3.2.2.1 Position the Rim Roller part onto the Axle Pressing Tool with dished side facing down as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Rim Roller part until the shaft bottoms-out in the pocket of the Axle Pressing Tool.
- 3.3 Slide (1) Center Drive Roller spacer followed by the Center Drive Roller (with One-way bearing already installed)
## **!! IF USING THE RIM ROLLER (THREADED) OPTION, THIS IS WHERE THE DRIVE ROLLER ORIENTATION MATTERS !!**   
## **Orient the pressed-on Rim Roller (Threaded) part and shaft so that the shaft is facing upwards from the Roller. Place the Center Drive roller assembly onto the shaft so that the one-way bearing locks in the filament unload/eject direction (locks with clockwise rotation when turning on shaft with Rim Roller (Threaded) below the Drive Roller).  This orientation of Rim Roller (Threaded) and Center Drive Roller ensures that the Rim Roller Hub (Threaded) part will want to tighten against the Rim Roller (Threaded) part when experiencing the highest resistance that occurs during unload/eject.**
- 3.4 Slide the second Center Drive Roller spacer onto the axle shaft.
- 3.5 Position the Rim Roller part (non threaded roller) onto the Axle Pressing Tool with dished side facing down as shown in picture.  Press or gently tap with hammer to drive the 8x80mm axle shaft through the Rim Roller part until the shaft bottoms-out in the pocket of the Axle Pressing Tool.
- 3.4 It is very important that the one-way bearing rotates in the unlocked direction freely with low resistance .  If the resistance of the one-way bearing is greater thatn the combined resistance of the two 608 bearings that the Drive Roller steel axle turns in then the system won't disengage and freespool properly during filament loads resulting in loose coils on the spool.  There has been limited instances of certain one-way bearings having too much resistance.  If your one-way bearings don't spin freely in the unlocked direction then assess your shaft diameter to ensure it is not to much above 8mm and/or you may need to try a different brand of one-way bearing.

# 4. Base Assembly

There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It enables quick add/remove/relocate capabilities and requires no hardware to mount.  You print all of the same parts except for the 2 base Supports that use the clip mount version (see "(2020 Clip-In)_optional" versions in STLs directory).  Assembly is the same.

Also, there is an optional "Base_Plate" part that mounts to the Supports and Tensioner Mount for a standalone application where the unit will not be attached to some other mounting suface.  If installing the Base_Plate part, screw the Tensioner Mount to the Base from the bottom before installing the side Support parts, Drive Roller Assembly, and/or Idler Roller.

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Base.jpg" width="250" height="250">

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Base_MR608_Bearings.jpg" width="300" height="350">  <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Rear_Roller_MR608_Bearings.jpg" width="300" height="250">

   - 4.1 Thread the Idler Roller (male) and Idler Roller (female) parts together tightly.  Press a total of (4) MR608 bearings into the Right Support, Left Support, and Idler Roller parts.  The Axle Pressing Tool can be used to aid with pressing the bearings into the deep bearing pockets of the Idler Roller.  Ensure the inner races of the bearings in the Right/Left Support parts turn freely.

<img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Base_Assy_1.jpg" width="400" height="350">

   - 4.2 Place the Tensioner Assembly around the Drive Roller Assembly and screw the Tensioner Mnt onto one of the Support parts using (2) 3x12 FHCS screws (or x10, x8).
## **Double Check that the one-way bearing of the Center Drive Roller locks when rotated in the direction of a filament unload.**
   - 4.3 Insert the Rear Roller Axle through the same base part aligning the "D" shape end to the flat in the 8mm pocket of the Support.  Ensure it presses all of the way in (you may need to tap it in a bit).  Secure with (1) 3x18 FHCS screw (or x10, x8).  
   - 4.4 Slide the Rear Roller onto the Rear Roller Axle.
   - 4.5 Install the opposite side Support part to assembly pressing in the D shaft end and securing with (3) 3x12 FHCS screws (or x10, x8).  Make sure there is no spring tension on the Tensioner arm for this step.
   - 4.6 Insert a section of bowden tube into the ECAS until it bottoms out/butts against the Tensioner Mnt behind the ECAS.  Place a locking clip in the ECAS (if you don't have these, an stl file is provided to print the locking clips).  2.5mm ID tubing is recommended to ensure good stiffness and minimal "buckling" of filament in the driven filament path.  Cut your section of tubing a little long for the location of the rewinder and the run to the ERCF slot position.  You can fine tune/trim the length after installation of the rewinder.  
## **It is recommended that you chamfer the inner edge of the tubing that is going into the Tensioner Mount with an Xacto knife or drill bit to ensure easy filament loading.  Also, depending on print quality you may want/need to clean up the filament path hole in the Tensioner Mount with a 1.75-2mm drill bit.**


# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Tuning

The standard recommended method for tuning the system is with the Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs rewinder drag and set a slip range in-between the two "imaginary" lines.  Adjust the spring tensioner screw accordingly and err on the light side.  Run the rewinder (see test code below). If loose filament is forming around the filament spool during unload, tighten the spring tensioning screw.  If no loose filament is forming around the filament roll, gradually reduce the spring tension until loose filament starts to accumulate and then increase tension in ~1/2 screw turn increments until you feel you have the lightest tension that results in a tightly packed unload. This method will result in the ultimate wear-out of the o-rings.  Testing and extrapolation estimates that the wear-out point is ~5K cycles.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders.  Ultimately o-rings can be replaced by the process described in section 3.2 of the Drive Roller Assembly section. 

An alternate method is to rely on spool rim slip against the rollers by running a high filament clamping force and selecting a rim surface other than the high friction rubber bands such as a soft PVC tape (electrical or gym floor line tape).  You will have to experiment with what works best for you, particularly on almost empty spools of low weight, and/or reach out to the Filamentalist Discord group for input (https://discord.com/channels/1208529298781372447/1208529299230031883).

# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Troubleshooting

Please see [troubleshooting guide](troubleshoot.md) or join our discord server above for more help.

# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Testing

Below are macros you can cut and paste into the bottom of your mmu_software.cfg or printer.cfg to test and tune your rewinders.

Happy multi-material printing and rewindering!

```
[gcode_macro rewinder_test]
gcode:
    MMU_TEST_LOAD LENGTH=50
    {% for n in range(20) %}

# cycles currently set at 20, i.e. range(20).  You can changes this however you chose.
        MMU_SERVO POS=DOWN
#        MANUAL_STEPPER STEPPER="gear_stepper" SPEED=300 ACCEL=400 MOVE=800
        MMU_TEST_MOVE SPEED=300 ACCEL=400 MOVE=800
# change the SPEED and ACCEL as you see fit
        MMU_SERVO POS=UP
# to stop a macro mid-cycle you must use the e-stop.  This dwell allows you to hit the e-stop while the servo is up so that you can pull the filament out of the ERCF while the printer/macro is stopped
        MMU_SERVO POS=DOWN
        MMU_TEST_MOVE SPEED=300 ACCEL=400 MOVE=-800
        MMU_SERVO POS=UP

    {% endfor %}


[gcode_macro rewinder_test_multitool]
gcode:
    {% set gates = [5] %} # [0,1,2,3,4,5] move between these gates
    {% set test_load_length = params.TEST_LOAD_LENGTH | default(50) | float %}
    {% set repeats = params.REPEATS | default(20) | int %}
    {% set speed = params.SPEED | default(300) | float %}
    {% set accel = params.ACCEL | default(400) | float %}
    {% set length = params.LENGTH | default(800) | float %}

    MMU_HOME

#    MMU_TEST_LOAD LENGTH=50
    {% for n in range(repeats) %}
        {% for gate in gates %}
            MMU_SELECT GATE={gate}
            MMU_TEST_LOAD LENGTH={test_load_length} # preload gate for a bit of length
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE={length}
            MMU_SERVO POS=UP
            MMU_TEST_MOVE SPEED={speed} ACCEL={accel} MOVE=-{length}
            MMU_EJECT
            MMU_RECOVER

        {% endfor %}
  
    {% endfor %}
```

# <img src="https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/rc2/Recommended_Options/Filamentalist_Rewinder/Assets/Filamentalist_Brain_Logo.png" width="50" height="60"> Version History

V1 - 5/17/24 - Public release into ERCF V2 RC2 repository

V1.1 - 5/19/24 - Update to CAD and stls for Tensioner Arms to remove potential filament catching point during endless spool ejection

V1.2 - 5/20/24 - Reverted Center_Drive_Roller to cylindrical press fit hole (vs hex of V1 and V1.1).  Revised 608 press fit pockets of Idler_Roller_(male&female) parts for both 80mm and 100mm width versions for improved press fit.

V1.3 - 5/20/24 - Added bevel to internal step on  Idler_Roller_(male) part for 80mm and 100mm versions to improve printability.  Updated the .f3dparametric file, step files, and stls for 80mm and 100mm versions.

V1.4 - 5/21/24 - Shortened threads on Idler_Roller_male parts by 1.5mm to remove slight interference.  Updated CAD, 80mm, and 100mm stls.

# To DO

1. 
