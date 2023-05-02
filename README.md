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
1. Sturdy backbone (based on Sturdy Bunny from @sneakytreesnake V2.3804 V2.3804)
2. Reliable encoder (based on Binky from @mneuhaus VT.483)
3. Remove need for top hats with sprung servo (based on Springy from @moggieuk V0.1503 | V2.4088)
4. Remove snag points on reverse filament flow (for EndlessSpool support)
5. Improve gate mechanism so filament does not slip back through accidentally (perhaps removing the need for the magnetic gate?) (based on Triple Decky from @gneu V2.5345)
6. Remove high wear parts / those prone to breakage (the servo arm improvements / bearing)
7. Formal filament bypass (including position in selector array)
8. Standardized layout so things like calibrating the selector is mostly automatic (the geometry is sufficiently fixed)
9. Rationalize command line set in Happy Hare for consistency
10. Magnetically closed connector cover on encoder (the current one is prone to breaking)
11. Updated manual


## Other Planned Companion Projects:
* ERCP v2 (new buffer system) which could be based on the auto rewind idea from @mneuhaus VT.483
* Pellet purge system to remove the need for the wipe tower and to unify tip creation to one place. Based on @bombela V2.4393 Assisted Purge System work
* Idea: Integrated dIsplay / control panel.  Integrated low spec rpi running a further customized version of KlipperScreen that is solely for managing ERCF.  The pi could also drive ERCF motors and servo

## CAD Design Guidelines

### Features

* no overhangs over 45 degrees
* no supports (unless they are absolutely needed, and if that's the case they must be built in to the part)
* 0.4mm chamfer on surfaces that touch the print bed (and no fillets on the build surface--breaks the 45 degree overhang rule)
* general "nice" aesthetic
* Take note of part orientation to make sure the part is strong in the directions it needs to be.
* Countersunk holes "overhanging" the print surface should have a chamfer on them or other method like that to prevent issues
* Think about minimum perimeters/shells--try to avoid really thin features
* Design with common screws/hardware in mind. Ie, stick with M3x6,8,12,16,20,25,30,35,40, M5x10,16,30,40 when possible (for V1/V2)
* Counterbore bridging for holes [[1]](#counterbore)
* always orient STLs such that no reorientation is necessary (stricter that just thinking about it in design)
* consider fillets for all edges that are sharp and might be touched by people, 0.5-1.0 tends to be good
* loose joints generally oversized by 0.3-0.4mm diameter for loose fit or 0.1mm for press fit. 3.4mm for M3 hardware, 5.4mm for M5 hardware

### Screw Holes
* Loose fit screw holes - Make the hole 0.4mm bigger
* Thread into the plastic - Make the hole 0.1mm smaller

### Press Fits/Bearings
* Make the feature .2mm bigger. A 10mm diameter bearing would be 10.2mm [[3]](#press-fit)

### Heatsets
* Heatset holes should be 4.7mm in diameter
* blind heatset holes should be 5mm deep
* add a 0.4 chamfer to all heatsets entrance edges on build surface (helps with insertion)

### References
* [1] <a href="https://github.com/Finn2708/CounterboreBridging" id="counterbore">Fusion360 Counterbore Addon</a>
