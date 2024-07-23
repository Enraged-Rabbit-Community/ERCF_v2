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
    - **Greasing:** Apply a heavy grease to the 608 bearings.
    - **Bearing Quality:** Lower-quality 608 bearings, often heavily greased, may match the performance needed better than higher-quality ones.


