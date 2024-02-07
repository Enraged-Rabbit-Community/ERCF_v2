# STL organization Notes
1. All STLs are prepended by the extruder or tool head name as appropriate.
- Ex: `SB_CW2_Body_Toolhead Sensor_HARTKPCB` belongs to the Stealthburner (SB) with Clockwork 2 (CW2) extruder.
2. Toolhead and entry sensors are in various combinations as noted in the folder names.  
The files which work with all (or multiple variations) are in the top level:
- `[a]_ALL_Knife_Holder.stl`
- `[a]_G2E_Cutting_Arm.stl`
- `[a]_SB_Cutting_Arm.stl`
3. The G2E cutting arm works with the printheads in the `Printheads>G2E Mods folder`. The SB Cutting arm works with printheads in the `Printheads>StealthBurner` Mod Variants folder.  
4. Files for the lever depressor which mounts to the Y rail are in the `Depressor` folder.