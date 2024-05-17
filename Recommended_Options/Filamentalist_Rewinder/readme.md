<h1 align="center">The "Filamentalist"</h1>

<h1 align="center">A passive filament driven rewinder/buffer</h1>

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/29681c81d6f0a38790b672aa099865cbd5e38a43/Filamentalist/Images/Filamentalist.png" width="450" height="525">
</p>
<p align="center"><img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f1c8e5d6d365af62a81703c1ab689bb3eaed4eba/Filamentalist/Images/Filamentalist_Front.jpg" width="525" height="450">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f1c8e5d6d365af62a81703c1ab689bb3eaed4eba/Filamentalist/Images/Filamentalist_Top.jpg" width="450" height="450">
</p>

See video of 3 rewinders swapping here (previous "front wheel drive" version, but very similar rewinder):  https://photos.app.goo.gl/iyLBGgytfVCPNLVBA

# Theory of operation:
The Filamentalist uses the axial force delivered by the ERCF gear motor along the filament to load and unload to/from the filament spool.  An adjustable spring clamp forces the filament against two o-rings that sit on the drive pulley to create a high traction interface.  A one-way clutch style bearing locks against the drive shaft and rotates the filament spool to take up filament during an unload.  For loading and print extruding, the clutch disengages allowing for effective free-spooling of the filament spool simliar to a roller style spool holder.  For unloading/buffering, some slip will occur between the filament and the o-ring interface and/or the spool rim and the rim roller of the rewinder to account for the varying diameter range of a spool from full to empty (full spool = max slip, empty spool = no/minimal slip).

<p align="center">
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/95bce4ba5cba58311181e91b689964c466b30c51/Filamentalist/Images/Filamentalist6_1.jpg" width="400" height="465">
</p>

# Credits:
Discord user Thisiscam first made me aware of Muzi Xiaoyang's video of a filament driven rewinder (https://www.bilibili.com/video/BV1ZM41197fX/?spm_id_from=333.337.search-card.all.click).  Through a long collaboration with Thisiscam, many design iterations and improvement on the Muzi Xiaoyang design, and a great Beta test team the Filamentalist was born. 

## **Additional Notes/Considerations** 

This rewinder is "almost" perfect, but not completely perfect.  Things that you need to know include:
1. The ERCF gear stepper is doing the heavy lifting.  Configure your gear stepper to run in sync mode with your extruder via Happy Hare settings.
2. A high torque NEMA 17 motor is recommended.  Many in the Beta team ran NEMA 17's spec'd at 55 N-cm max torque and config'd them for 1-1.4A.  Grafton's 40 tooth NEMA 17 mod is recommended (https://www.printables.com/model/692720-ercf-40-tooth-gear-modifiction).  This may not be required so if you already have built your ERCF, try the Filamentalist with the motor you have and decide if you think you need more torque.
3. Several in the Beta team had space constraints that they wanted the rewinder to honor.  As a result the width of the Filamentalist was set to support most standard 1, 0.5, and 0.25KG spool sizes and still be able to fit 6 rewinders across a 350 size Voron printer.  Some spools such as KVP's are too wide to fit the baseline design.  It's a simple design so feel free to usermod to your heart's content to fit your needs!  Height was set to be as low as possible to fit some existing dry box designs.
4. Because the standard tuning of this design relies on some filament slip at the o-rings, the o-rings will ultimately wear-out.  Testing and extrapolation estimates that the wear-out point is ~4K cycles +/- 1K.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders in your line-up.  Also, o-rings with grooves worn in them can be swapped with their opposing partners to present the unworn side/face to the filament to extend the life of a set.  Ultimately o-rings can be replaced by the process described in section 3.2 of the Drive Roller Assembly section. This o-ring slip/wear also creates a small amount of rubber dust/debris to go along with the typical filament dust /debris that the ERCF gears create.  You may want to add a filament cleaner of your choice (but don't have to).
5. Due to pressfits for the 608 bearings, 8mm axle, and ECAS, printer calibration is important.  A "Test Block" stl is included.  It is recommended you print this first and test the press fits and measure the two small holes (2.7mm for cutting 3mm screw threads and 2.3mm for the filament path) to determine if you need to apply any scaling or changes to your extrusion factors in your slicer before printing.  Due to varying ECAS supplier tolerances and varying printer tolerances some experienced cracking at the ECAS hole when pressing in the ECAS.  If all other press fits work well on the Test Block but you experience cracking at the ECAS hole when pressing in an ECAS fitting, you can use an Xacto knife to lightly remove some plastic.  If the ECAS is too loose you can use superglue to glue the ECAS into the Tensioner Mount (not the Test Block 😉 ).
6. Questions and input can be directed to the Filamentalist Discord group here:  (https://discord.com/invite/H9yuhrXTEq)

## **BOM:**

| Qty per Site | Part | Example Source Reference | Comments |
|-------|---------------------------|-----------------------------|-------------------------------|
|   1   | 8mm dia. x 80mm Stainless Steel Dowell Pin | https://www.amazon.com/uxcell-Stainless-Chamfered-Support-Elements/dp/B0BC8VFSWD, Amazon Alternate https://www.amazon.com/Unifizz-Stainless-Steel-Round-Silver/dp/B09P9MC953?th=1 (sheared ends may need to be cleaned up), Aliexpress https://www.aliexpress.us/item/3256801518620991.html | Undersized shaft (7.93-7.97mm dia) works the best (5/16" dia).  100mm length is more available and can extend out of rewinder or cut polished 8mm or 5/16" diameter stainless rod to 80mm lengths |
|   5   | MR608 bearings | Can be obtained anywhere (Home Depot, Amazon, Aliexpress, etc.)  | MR608RS, MR608ZZ, etc. |
|   1   | HF081412 One-Way Bearing | https://www.amazon.com/dp/B0C7TRFJBS, Aliexpress | 8mm Bore, 12mm length, 14.2mm Diameter. |
|   1   | ECAS press-in pneumatic fittings for the bowden tubes (like used in ERCF)  |  | A locking clip is required and can be bought or printed (stl included) |
|   2   | O-rings | AS568 Standard size 211, Home Depot #110, https://www.amazon.com/211-Buna-N-Ring-Durometer-Black/dp/B000FN0W7I/, Aliexpress | In the range of 13/16" ID, 1-1/16" OD or ~20mm ID, ~26mm OD (~3mm cross section/cs), Nitrile Butadiene Rubber (Buna-N)|
|   1   | Spring  | https://www.amazon.com/gp/product/B08FDYJLYC/, Aliexpress | Like in extruders - 304 Stainless Steel,6mm OD,1mm Wire Size,7.5mm Compressed Length,15mm Free Length,37.2N Load Capacity |                                 |
|   1 | 3mm Heatset  |  | Voron standard size | set into the Tensioner Mnt |
|   1   | 3x35mm SHCS | SS Socket Head Cap Screw | Spring Tensioner Screw anything in the range of 35mm +/- 10mm should work|
|   6   | 3x12 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Mnt and Rear Axle installation 8/10/12mm lengths will work|
|   3   | 3x18 FHCS  |  Stainless Steel Flat Head Screw | for Tensioner Arm clamp bearings and Tensioner Mnt pivot installation 16mm length will work |
|   2   | Rubber Band | https://www.amazon.com/dp/B0CPJPN41V | Size #94 (3 1/2" x 3/4"), any wide rubber bands in the 2.5"-3.5" size will work.  Can combine multiples across face of rollers.  Another excellent alternative is to cut bands from a bicycle inner tube.  Mountain bike or "balloon" tire sized tubes for tires in the 1.75"-2.4" width work well. |
| var.  | 2.5mm ID PTFE tubing | Amazon, Aliexpress, 3D printing vendors | 2.5mm ID recommended but you can try whatever you have.  Length depends on the distance from your rewinder location to your ERCF inputs |


# Printing Guidelines:

## **General:**
- Material: ABS or ASA (~170 gm per site)
- Print Time: ~8hr 17min (based on the Ellis PIF profile speeds, accelerations, and volumes)
- 0.2mm layer height
- 40% infill recommended.  Linear style infills are fastest (rectilinear, monotonic, grid, triangles, stars, etc.)
- Wall Count: 4
- Solid Top/Bottom Layers: 5

## **Part Specific:**
- Orientation suggestions are relative to the installed assembly orientation and are shown in the slicer images below.
  
<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/29681c81d6f0a38790b672aa099865cbd5e38a43/Filamentalist/Images/Filamentalist.png" width="200" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/95bce4ba5cba58311181e91b689964c466b30c51/Filamentalist/Images/Filamentalist%20Sliced%20(Black)_1.jpg" width="375" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/95bce4ba5cba58311181e91b689964c466b30c51/Filamentalist/Images/Filamentalist%20Sliced%20(Orange)_1.jpg" width="375" height="300">


| **Qty per Site** | **Part**  | **Pic** |  **Orientation**            | **Printed Supports Needed** | **Comments** |
|------|-----------------------------------------|------------|--------------------|-----|---------------------------------|
| 1       | Right Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Right%20Support.jpg" width="40" height="40"> |  Horizontal                   | N     |                                  |
| 1       | Left Support | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Left%20Support.jpg" width="40" height="40">                                                            | Horizontal                   | N     |                                  |
| 1       | Base | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/a88c2c8f885684abdce5d5ff6f18d316faf91c62/Filamentalist/Images/Base.jpg" width="40" height="40">                                                            | Horizontal                   | N     | Optional part for a standalone unit not mounted to another surface  |
| 1       | Rear Roller Axle  | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rear%20Roller%20Axle.jpg" width="40" height="40"> | Horizontal | N | align flat of "D" to build plate |
| 2 (1)       | Rim Roller | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Rim%20Roller.jpg" width="40" height="40">                                                   | Horizontal                | N       | Dished side up.  Print 1 if you choose to use 1 Rim Roller (Threaded) (see next line below) |
| 0 (1)       | Rim Roller (Threaded) | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/95bce4ba5cba58311181e91b689964c466b30c51/Filamentalist/Images/Rim%20Roller%20(Threaded).jpg" width="40" height="40">                                                   | Horizontal                | N       | Optional - print if you want the ability to replace o-rings without pressing a roller off of the axle. Dished side up, recommend scattered seams for improved thread perfromance, clean out support web in center splined hole with Xacto knife |
| 0 (1)       | Rim Roller Hub (Threaded) | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/85a541f5e7ae803522ccf610f52861cce66e0702/Filamentalist/Images/Rim%20Roller%20Hub%20(Threaded).jpg" width="40" height="40">                                                   | Horizontal                | N       | Optional - print if you want the ability to replace o-rings without pressing a roller off of the axle. Recommend scattered seams for improved thread performance. |
| 1       | Center Drive Roller  | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Center%20Drive%20Roller.jpg" width="40" height="40">                                                        | Horizontal                 | N        | Recommend scattered seams for press fit-bore concentricity |
| 2       | Center Drive Roller Spacer |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/26900c9dafbd97ff7940f59e07de3eca9dee5aee/Filamentalist/Images/Center%20Drive%20Roller%20Spacer.jpg" width="40" height="40">    | Horizontal                 | N        |                             |
|         | Tensioner Arm Left |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/95bce4ba5cba58311181e91b689964c466b30c51/Filamentalist/Images/Tensioner%20Arm%20Left_1.jpg" width="40" height="40"> | Horizontal                          |  N    |  |
|         | Tensioner Arm Right |  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2173eeed7a371bd58314c6460d6b38eb1fc87574/Filamentalist/Images/Tensioner%20Arm%20Right_1.jpg" width="40" height="40"> | Horizontal                          |  Built-in     | Remove built-in support from the locking tab |
| 1       | Tensioner Mnt | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Tensioner%20Mnt.jpg" width="40" height="40">                           | Vertical (as installed)                | N  |   |
| 1       | Idler Roller (male)   | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2173eeed7a371bd58314c6460d6b38eb1fc87574/Filamentalist/Images/Idler%20Roller%20(male).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1       | Idler Roller (female)   | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2173eeed7a371bd58314c6460d6b38eb1fc87574/Filamentalist/Images/Idler%20Roller%20(female).jpg" width="40" height="40">  | Vertical  | N  |  Scattered seams |
| 1    | Axle Pressing Tool | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/cab2ddf8149339b31714dbadca2cb36611d397f7/Filamentalist/Images/Axle%20Pressing%20Tool.jpg" width="40" height="40"> | Vertical | N | Pocket opening up.  Print with 100% infill for reuse strength and durability when building multiple rewinders. |
| 2 | ECAS Locking Clip | <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/6837e24c214d6256fef5f5dbc52ac9dc8a1a9989/Filamentalist/Images/ECAS%20Locking%20Clip.jpg" width="40" height="40"> |  Horizontal | N | Tab up |
| 1 | Test Block | <img src="https://github.com/SkiBikePrint/Filamentalist/blob/dac1be98bd8ef3632d9162f048f20ea1d720f740/Images/Test%20Block.jpg" width="40" height="40"> |  608 Pocket facing up | N | printer calibration tool |


There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It is highly recommended and enables quick add/remove/relocate capabilities and requires no hardware to mount.  You print all of the same parts except for the 2 Base Supports that use the clip mount version (see "Clip Mount Base Version" folder under STL's directory).  Assembly is the same.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/f96422acb504d4f098fd575ae8534f495f92b699/Filamentalist/Images/Clip%20Mount%20Version.jpg" width="400" height="250">

# Assembly Instructions:

# 1. Tensioner Mount Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/662caf6e50f499b8f42359d868c06f1419f9e44f/Filamentalist/Images/Tensioner_Mnt.jpg" width="400" height="350">

   - 1.1 Install 3mm heatset insert into Tensioner Mnt.
   - 1.2 Remove the rubber seal from the ECAS fitting.
   - 1.3 Install the ECAS fitting into the Tensioner Mnt.  It should be a moderate press-in.  You may need to push it in firmly using the end of a 8mm steel shaft or printed rear axle shaft to get it to sit flush to the Tensioner Mnt mating surface.  The sidewalls of this hole are relatively thin.  Varying ECAS and print tolerances could result in the sidewall cracking.  If this happens, use superglue around the ECAS and crack.

# 2. Tensioner Arm Installation

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/b3865d1dce459810b443cc16736aa5070a433a71/Filamentalist/Images/Tensioner_Assy.jpg" width="400" height="350">

   - 2.1 Lay the Tensioner Arm Right part on a flat surface.  Slide the 608 bearing onto the bearing post.  Place the Tensioner Arm Left part into the 608 bearing and rotate against the Tensioner Arm Right part making sure the alignment tab seats correctly at into the pocket at the bottom of the Tensioner Arm Right part.
   - 2.2 Place a 3x18 FHCS (or x16, x12) through the bearing mount hole of the Tensioner Arm Left part and moderately tighten the screw into the Tensioner Arm right piece.  Once installed verify that the bearing turns freely.
   - 2.3 Place a 3x18 FHCS (or x16, x12) through the hole in the Tensioner Arm Left part at the "nose" end and moderately tighten the screw into the Tensioner Arm right piece.  
   - 2.4 Install the Tensioner Arm onto the Tensioner Mnt using a 3x18mm FHCS screw (or x16) .  Tighten until snug and then back off until the arm rotates freely on the mount.
   - 2.5 Place an M3 washer followed by the spring onto an M3x35 SHCS (or x30, x40) and slide through the slotted hole in the bottom of the arm assembly.  Screw the SHCS into the heatset insert of the Tensioner Mnt.  No tension should be on the spring at this point.
       - 2.5.1 ALTERNATE INSTALLATION:
                If the orientation of your Filamentalist makes it difficult to access the tension adjustment screw you can use a 50mm long 3mm SHCS coming from the bowden side of the rewinder with a lock nut, nut with loctite, or a heatset with loctite on the other end as shown in the image below.  
<p align="center">
<img src="https://github.com/SkiBikePrint/Filamentalist/blob/a2b556a6cd13a9c8438ebea5d4e3340720e51efe/Images/Tensioner%20Screw%20(alternate).jpg" width="400" height="350">
</p>

# 3. Drive Roller Assembly

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2f235409913aefef5219e5df66e258a4124f445c/Filamentalist/Images/Center%20Drive%20Roller%20with%201-Way%20Bearing.jpg" width="300" height="300">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/98160e0638612f0d6ec1bac0d75c2d922c8fa904/Filamentalist/Images/Drive%20Roller%20Assembly_1.jpg" width="650" height="400">

- 3.1 Press HF081412 One-Way Bearing into Center Drive Roller.  Orientation does not matter at this point.
- 3.2 Install first Rim Roller
    - 3.2.1 For Rim Roller (Threaded) option:

The purpose of this two-piece roller is to allow for future o-ring replacement by removing the Rim Roller from the Hub versus having to press a roller off of the axle and then press it back on.  For o-ring replacement, remove the Drive Roller Assembly from the rewinder (unscrew the (6) screws of the Right and Left Supports).  Then unscrew the Rim Roller from the Rim Roller Hub.  You can now remove the old o-rings and install a pair of new ones, screw the Rim Roller back onto the Hub, and re-install the supports.  This option is recommended if you expect to run a high number of swaps (5K+) over fairly short periods of time as the o-rings will eventually wear out.

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

There is an alternate version of the base that clips into two 2020 rails spaced 170mm apart (center-to-center). It enables quick add/remove/relocate capabilities and requires no hardware to mount.  You print all of the same parts except for the 2 Base Supports that use the clip mount version (see "Clip Mount Base Version" folder under STL's directory.  Assembly is the same.

Also, there is an optional "Base" part that mounts to the Supports and Tensioner Mount for a standalone application where the unit will not be attached to some other mounting suface.  If installing the Base part, screw the Tensioner Mount to the Base before installing the side Support parts, Drive Roller Assembly, and/or Idler Roller.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/a88c2c8f885684abdce5d5ff6f18d316faf91c62/Filamentalist/Images/Base.jpg" width="250" height="250">

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Base%20MR608%20Bearings.jpg" width="300" height="350">  <img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/2069f29dd108fc0a90424fd3d8a989f8cd7d30d4/Filamentalist/Images/Rear%20Roller%20MR608%20Bearings.jpg" width="300" height="250">

   - 4.1 Thread the Idler Roller (male) and Idler Roller (female) parts together tightly.  Press a total of (4) MR608 bearings into the Right Support, Left Support, and Idler Roller parts.  The Axle Pressing Tool can be used to aid with pressing the bearings into the deep bearing pockets of the Idler Roller.  Ensure the inner races of the bearings in the Right/Left Support parts turn freely.

<img src="https://github.com/SkiBikePrint/ERCF_Mods/blob/008c49d425768e41388aca29f8c0043d37e5f5bd/Filamentalist/Images/Base%20Assy_1.jpg" width="400" height="350">

   - 4.2 Place the Tensioner Assembly around the Drive Roller Assembly and screw the Tensioner Mnt onto one of the Support parts using (2) 3x12 FHCS screws (or x10, x8).
## **Double Check that the one-way bearing of the Center Drive Roller locks when rotated in the direction of a filament unload.**
   - 4.3 Insert the Rear Roller Axle through the same base part aligning the "D" shape end to the flat in the 8mm pocket of the Support.  Ensure it presses all of the way in (you may need to tap it in a bit).  Secure with (1) 3x18 FHCS screw (or x10, x8).  
   - 4.4 Slide the Rear Roller onto the Rear Roller Axle.
   - 4.5 Install the opposite side Support part to assembly pressing in the D shaft end and securing with (3) 3x12 FHCS screws (or x10, x8).  Make sure there is no spring tension on the Tensioner arm for this step.
   - 4.6 Insert a section of bowden tube into the ECAS until it bottoms out/butts against the Tensioner Mnt behind the ECAS.  Place a locking clip in the ECAS (if you don't have these, an stl file is provided to print the locking clips).  2.5mm ID tubing is recommended to ensure good stiffness and minimal "buckling" of filament in the driven filament path.  Cut your section of tubing a little long for the location of the rewinder and the run to the ERCF slot position.  You can fine tune/trim the length after installation of the rewinder.  
## **It is recommended that you chamfer the inner edge of the tubing that is going into the Tensioner Mount with an Xacto knife or drill bit to ensure easy filament loading.  Also, depending on print quality you may want/need to clean up the filament path hole in the Tensioner Mount with a 1.75-2mm drill bit.**


# Tuning

The standard recommended method for tuning the system is with the Tensioner Arm clamping force.  The arm does not need an extreme amount of tension.  To tune the spring force, lift the tensioner and insert a section of filament through the o-ring bearing interface and into the bowden tube.  Hold the center roller by placing your thumb against the o-rings and try to pull the filament out.  You want the slip force to be slightly more than what the overall system drag is, so you have to imagine the range of gear motor pull force vs rewinder drag and set a slip range in-between the two "imaginary" lines.  Adjust the spring tensioner screw accordingly and err on the light side.  Run the rewinder (see test code below). If loose filament is forming around the filament spool during unload, tighten the spring tensioning screw.  If no loose filament is forming around the filament roll, gradually reduce the spring tension until loose filament starts to accumulate and then increase tension in ~1/2 screw turn increments until you feel you have the lightest tension that results in a tightly packed unload. This method will result in the ultimate wear-out of the o-rings.  Testing and extrapolation estimates that the wear-out point is ~4K cycles +/- 1K.  The impact of o-ring wear-out can be reduced by periodically swapping highly used rewinders with low use rewinders.  Ultimately o-rings can be replaced by the process described in section 3.2 of the Drive Roller Assembly section. 

An alternate method is to rely on spool rim slip against the rollers by running a high filament clamping force and selecting a rim surface other than the high friction rubber bands such as a soft PVC tape (electrical or gym floor line tape).  You will have to experiment with what works best for you, particularly on almost empty spools of low weight, and/or reach out to the Filamentalist Discord group for input (https://discord.com/channels/1208529298781372447/1208529299230031883).

# Troubleshoot

Please see [troubleshooting guide](troubleshoot.md) or join our discord server above for more help.

# Testing

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

# Version History

V2 - Public release

V2.1
- Added material around ECAS on Tensioner Mnt to reduce potential for cracking
- Revised Tensioner ARM Left/Right to create clearance for wider Tensioner Mnt
- Added Test Block.stl to check printing tolerances for 608 Bearing, 8mm Axle, and ECAS press fits as well as holes for 3mm screw thread cutting and 2.3mm filament hole.

# To DO

1. Add in reference and instructions for the parametric model.
2. Include instructions for the alternate tensioner screw mounting direction.
3. Add cal tool into STL's and instructions up front for checking fit.
