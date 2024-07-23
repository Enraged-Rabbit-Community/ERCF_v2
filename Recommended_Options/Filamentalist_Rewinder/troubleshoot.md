# Filamentalist Troubleshooting Guide

## Debugging Tips for Loose Filament During Rewinder Operation

After a fast load movement, a full spool may rotate a bit further due to inertia and cause a small amount of filament slack around the spool. This behavior is the same as any roller based spool holder and should not cause any issue for printing. 
*In all other Filamentalist operations, there should be no slack forming on the spool.*
If you observe excessive slack, please read the troubleshooting information below.

### Issue: Slack Forming Around the Spool in the Rewind/Unload Direction

**Causes and Solutions:**
- **Tensioner Settings:** Ensure that the tensioner is not overly loose. It should maintain enough tension so that filament movement drives the rollers.
- **One-way Bearing Direction** Check that the bearing is not installed in reverse. See section 3. Drive Roller Assembly in the main readme.md doc.  
- **Spool Slippage:** If the problem occurs when the spool is nearly empty and the spool is slipping on the roller, make sure you have a high traction material such as rubber bands or bicycle inner tube bands on the rim rollers. 

### Issue: Slack Forming Around the Spool in the Print/Load Direction

**Causes and Solutions:**
- **One-Way Bearing Disengagement:** The issue typically indicates that the one-way bearing is failing to switch to free-wheel mode.
  
  **Assembly Checks:**
  - **Spacing and Alignment:** The one-way bearing should not be tightly sandwiched between the two CDR Spacers and Rim Rollers. Instead, the spacers should have a small allowable movement on the shaft (approximately 0.2mm to 0.5mm) .
  
  **Friction Concerns:**

**Quality Variations in Components:**
- **One-Way Bearing and Shaft Compatibility:** Verify that the one-way bearing rotates freely on the shaft. Measure the diameter of the shaft; successful setups typically report diameters between 7.92mm to 7.96mm (or 5/16" nominal). If your measurements are close to or exceed 8mm, the shaft may be too large for the bearing.
  - **Adjustment:** Consider lightly lathing/sanding the shaft's center section to to reduce the diameter.
  - **5/16" Diameter Axles:**" Purchasing 5/16" diameter shaft or stainless steel tubing has also produced good results

  - **Bearing Friction:** The friction of the one-way bearing should be less than that of the four 608 bearings on the Rim and Idler Rollers. Although it is rare that this will be the case, if you suspect that more 608 bearing resistance is required then:
    - **Idler Roller Bearing Lateral Loading:** Resistance can be increased on the rear Idler Roller by "side-loading" the 608 bearings.  This can be accomplished by increasing the tension on the Rear Roller axle screws.  It may be necessary to slightly shorten the Idler Axle by sanding the end(s) down a small amount (~0.2mm) and then tightening the axle screws until an increase in resistance is noted.
    - **Greasing:** Apply a heavy grease to the 608 bearings.
    - **Bearing Quality:** Lower-quality 608 bearings, often heavily greased, may match the performance needed better than higher-quality ones.

## Gear Motor Stalling

**Causes and Solutions:**
- **Excessive Spring Tension on Tensioner Assembly:**  The tensioner screw may be set too tight not allowing the Tensioner Arm to lift and allow for slip when needed
- **Filament Path Resistance:**
  - Excessive filament path length and bends increases system resistance.  Minimize the filament path length and turns between the Filamentalist and the MMU.
  - Increase bowden ID.  2.5mm ID is the recommended diameter for a baseline setup but 3mm ID may be required for long/high-resistance filament paths.
- **Rubbing/Interference of Filamentalist Components:**
  - Remove the filament from the rewinder and spin the Center Drive Roller assembly and the Rear Idler Roller.  Listen and feel for scraping, rubbing, or excessive resistance. If you feel this then the rewinder may need to be dissassembled and reassembled.  When reassembling check that:
    -  the Rim Roller spacing allows the CDR Spacers to free float
    -  the Rear Idler axle screws are not overly tight and causing lateral compresion on the 608 bearing races
    -  the Rim Rollers are not rubbing against anything
    -  the one-way bearing is free of debris
