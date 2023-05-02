# ERCF v2 Community Project

This is the, perhaps temporary, repository for community development of the next generation v2 Enraged Rabbit Carrot Feeder (ERCF). This project is endorsed by ERCF its creator Ette

## Development Team:
* @moggieuk V0.1503 | V2.4088
* @sneakytreesnake V2.3804 V2.3804
* @mneuhaus VT.483
* @gneu V2.5345
* @bombela V2.4393


## Goals:
- Simplify construction (without any significant additional costs)
- Aim for out of the gate reliability (i.e. wider tolerance for certain parts)
- Quicker set up time / less config
- Align with current BOM and design as closely as possible.


## Components:
1. Sturdy backbone (Sturdy Bunny from @sneakytreesnake V2.3804 V2.3804)
2. Reliable encoder (Binky from @mneuhaus VT.483)
3. Remove need for top hats with sprung servo (Springy from @moggieuk V0.1503 | V2.4088)
4. Remove snag points on reverse filament flow (for EndlessSpool support)
5. Improve gate mechanism so filament does not slip back through accidentally (perhaps removing the need for the magnetic gate?) (Triple Decky from @gneu V2.5345)
6. Remove high wear parts / those prone to breakage (the servo arm improvements / bearing)
7. Formal filament bypass (including position in selector array)
8. Standardized layout so things like calibrating the selector is mostly automatic (the geometry is sufficiently fixed)
9. Rationalize command line set in Happy Hare for consistency
10. Magnetically closed connector cover on encoder (the current one is prone to breaking)
11. Updated manual


## Other Planned Companion Projects:
* ERCP v2 (new buffer system) which could be the auto rewind idea from @mneuhaus VT.483 (because I think there are enough options to the current ERCP).
* Pellet purge system to remove the need for the wipe tower and to unify tip creation to one place. @bombela V2.4393 has really good starting point.
* Idea: Integrated dIsplay / control panel.  Integrated low spec rpi running a further customized version of KlipperScreen that is solely for managing ERCF.  The pi could also drive ERCF motors and servo

