## CAD Design Guidelines (in case you were interested)
* No overhangs over 45 degrees
* No supports (unless they are absolutely needed, and if that's the case they must be built in to the part)
* 0.4mm chamfer on surfaces that touch the print bed (and no fillets on the build surface--breaks the 45 degree overhang rule)
* General "nice" aesthetic
* Take note of part orientation to make sure the part is strong in the directions it needs to be.
* Countersunk holes "overhanging" the print surface should have a chamfer on them or other method like that to prevent issues
* Think about minimum perimeters/shells--try to avoid really thin features
* Design with common screws/hardware in mind. Ie, stick with M3x6,8,12,16,20,25,30,35,40, M5x10,16,30,40 when possible (for V1/V2)
* Counterbore bridging for holes [[1]](#counterbore)
* Always orient STLs such that no reorientation is necessary (stricter that just thinking about it in design)
* Consider fillets for all edges that are sharp and might be touched by people, 0.5-1.0 tends to be good
* Loose joints generally oversized by 0.3-0.4mm diameter for loose fit or 0.1mm for press fit. 3.4mm for M3 hardware, 5.4mm for M5 hardware

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

