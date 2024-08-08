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

- **Tight One-Way Bearing:** Verify that the one-way bearing rotates freely on the shaft (has equal to, or leass resistance than a 608 bearing). If one-way bearing feels tight/draggy when rotated on the shaft in the unlocked direction the inner plastic spring/retainer my be too tight.  Ttry reworking the bearing using the procedure below:
  - **One-Way Bearing Rework Procedure** - see video of procedure [here](https://photos.app.goo.gl/rgrtAJLfc5br5F7E9)
      1. Place bearing on end of axle rod/tube.
      2. Heat bearing with heat gun or blow dryer until bearing gets hot.  Rotate bearing while heating to get uniform heating
         - **Since power/heat of heat guns vary it is possible to overheat the bearing and melt the inner plastic!** Check result on the first bearing with every 20-30 seconds of heating by following steps c. and d. below until you determine the correct amount of heating required for your heat gun and tight bearings.
      3. While holding the the heated bearing and axle with a towel or (anything to protect your hands from getting burnt), rotate the bearing on the shaft in the unlocked direction until the bearing cools down.
      4. The bearing should now rotate on the axle with little to no resistance in the unlocked direction but still lock tightly in the opposite direction.  If you still feel excessive resistance (greater than a 608 bearing's resistance), repeat the procedure adding even more heat/time.
  - **Lubrication:** Use a light lubricant (thin layer of lithium grease or silicone lubricant) on the center portion of the shaft where the one-way bearing will sit.
  - **5/16" Diameter Axles:**" As a last resort, purchasing 5/16" diameter shaft or stainless steel tubing should result in an axle diameter less than 8mm

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
