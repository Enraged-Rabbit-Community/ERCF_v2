## Debugging Tips for Loose Filament During Rewinder Operation

After a fast load movement, the spool may rotate a bit further due to inertia and causing some filament slack around the spool. This behavior is the same as any roller based spool holder and should not cause any issue for printing. 
*In all other Filamentalist operations, there should be no slack forming for any standardly sized spool.*
If you observe excessive slack, please read the troubleshooting information below.


### Issue: Slack Forming Around the Spool in the Rewind/Unload Direction

**Causes and Solutions:**
- **Tensioner Settings:** Ensure that the tensioner is not overly loose. It should maintain enough tension so that filament movements drives the rollers.
- **One-way Bearing Direction** Check that the bearing is not installed in reverse.  
- **Scratches:** Check for parts that might be causing scratches or binding to the rollers
- **Spool Slippage:** If the problem occurs when the spool is nearly empty and the spool is slipping on the roller, make sure you have the rubber bands or another material with high enough friction on the large rollers. 

### Issue: Slack Forming Around the Spool in the Print/Load Direction

**Causes and Solutions:**
- **One-Way Bearing Disengagement:** The issue typically indicates that the one-way bearing is failing to switch to free-wheel mode.
  
  **Assembly Checks:**
  - **Spacing and Alignment:** The one-way bearing should not be tightly sandwiched between two spacers and large rollers. Instead, the spacers should have a small allowable movement (about 0.1mm to 0.4mm) on the shaft.
  
  **Friction Concerns:**
  - **Bearing Friction:** The friction of the one-way bearing should be less than that of the two 608 bearings on the large rollers. Check to ensure the 608 bearing does not spin excessively on the shaft. If it does:
    - **Greasing:** You might need to reapply heavy grease to the 608 bearings to increase friction.
    - **Bearing Quality:** Lower-quality 608 bearings, often heavily greased, may match the performance needed better than higher-quality ones.

**Quality Variations in Components:**
- **One-Way Bearing and Shaft Compatibility:** Verify that the one-way bearing rotates freely on the shaft. Measure the diameter of the shaft; successful setups typically report diameters between 7.93mm to 7.96mm. If your measurements are close to or exceed 8mm, the shaft may be too large for the bearing.
  - **Adjustment:** Consider lightly sanding the shaft's center to improve the bearing's rotation if it appears too tight.


