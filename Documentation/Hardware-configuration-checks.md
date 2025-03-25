#### Page Sections:
  - [Checks You Should Have Done Already](#checks-you-should-have-done-already)
  - [Step 1. Check Endstop & Optional Sensors](#step-1-check-endstop--optional-sensors)
  - [Step 2. Check motor movement and direction](#step-2-check-motor-movement-and-direction)
  - [Step 3. Check the Encoder](#step-3-check-the-encoder)
  - [Step 4. Check other sensors (if fitted)](#step-4-check-other-sensors-if-fitted)
  - [Step 5. Check Servo](#step-5-check-servo)

*\[This guide was adapted from the [Happy Hare Wiki](https://github.com/moggieuk/Happy-Hare/wiki) for ERCF v2. Thanks Moggie!\]*


## Checks You Should Have Done Already

All of these checks and adjustments were covered in the Build Manual, and should have been done while building your ERCF.

-Filament path / BMG Gear alignment (Manual page 71)

-(if using a Geared setup) Adjustment of GT2 pulley and belt tension (Covered in the Geared Drive sub-Manual)

-Encoder path adjustment (page 114)

-Setting GT2 pulley and belt tension (page 127)

-Setting 8mm rod depth (page 136)

**If you haven't done these steps, go review the manual!**

<br>


Now that you've completed the [Happy Hare Configuration](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Happy-Hare-Configuration.md), you should be greeted by a large warning on your console:

```yml
Prerequsite calibration steps are not complete:
Use MMU_CALIBRATE_SELECTOR to calibrate selector for gates: 0,1,2,3,4,5,6,7
Use MMU_CALIBRATE_GEAR (with gate 0 selected) to calibrate gear rotation_distance on gate: 0
Use MMU_CALIBRATE_ENCODER (with gate 0 selected)
Use MMU_CALIBRATE_GEAR (with gate selected) or MMU_CALIBRATE_GATES GATE=xx to calibrate gear rotation_distance on gates: 1,2,3,4,5,6,7
Use MMU_CALIBRATE_BOWDEN
```

That is normal, do not worry. Before we tackle that, we need to make sure all of the hardware is configured correctly!


## Step 1. Check Endstop & Optional Sensors

Verify that the Selector endstop, and any installed extruder or toolhead sensors are working. The recommended procedure is:

`MMU_MOTORS_OFF`

Now remove filament from ERCF and extruder, and move the Selector to the center of travel.

`QUERY_ENDSTOPS`

(Or use the visual query in Mainsail or Fluuid). Validate that you can see:

```yml
mmu_sel_home:open
extruder:open
toolhead:open
[...]
```

> [!NOTE]
> You will only see the sensors you have installed. You will additionally see any endstops or sensors installed on your printer.

Then manually press and hold the selector microswitch and rerun `QUERY_ENDSTOPS`.

Validate that you can see `mmu_sel_home:TRIGGERED` in the list.

If you have an extruder sensor installed, feed filament into the extruder past the switch and rerun `QUERY_ENDSTOPS`.

Validate that you can see `extruder:TRIGGERED` in the list.

If you have a toolhead sensor installed, feed filament into the toolhead past the switch and rerun `QUERY_ENDSTOPS`.

Validate that you can see `toolhead:TRIGGERED` in the list.

If any of these don't change state, then the pin assigned to the endstop is incorrect. If the state is inverted (i.e. enstop transitions to `open` when pressed) then add/remove the `!` on the respective endstop pin in `mmu_hardware.cfg`. 

Other endstops like "touch" operation and pregate sensors are advanced and are not cover by this inital setup.


## Step 2. Check motor movement and direction

Once pins are correct it is important to verify direction.  It is not possible for the installer to ensure this because it depends on the actual stepper wiring.  The recommended procedure is:

Run the command `MMU_MOTORS_OFF` Now move the Selector to the center of travel. 

Next, run the command `MMU_HOME` and verify that the Selector moves towards the endstop / home position

If the Selector doesn't move it is likley that the pin configuration for `step_pin` and/or `enable_pin` are incorrect. Open up `mmu_hardware.cfg`, and find the section `[stepper_mmu_selector]`.

Verify the pin names and prefix the pin with `!` to invert the signal. E.g.

```yml
enable_pin: !mmu:MMU_SEL_ENABLE
 (or)
enable_pin: mmu:MMU_SEL_ENABLE
```

If the selector moves the wrong way the `dir_pin` is inverted. Either add or remove the `!` prefix:

```yml
dir_pin: !mmu:MMU_SEL_DIR
 (or)
dir_pin: mmu:MMU_SEL_DIR
```

Now repeat the exercise with the gear stepper:

```yml
MMU_MOTORS_OFF
  (remove any filament from your MMU)
MMU_TEST_MOVE MOVE=100 SPEED=50
  (verify that the gear stepper would push filament towards the extruder / pull filament from the spool)
MMU_TEST_MOVE MOVE=-100 SPEED=50
  (verify that the gear stepper is pulling filament away from the extruder / pushing filament back to the spool)
```

If the gear stepper doesn't move or moves the wrong way open up `mmu_hardware.cfg`, find the section `[stepper_mmu_gear]`:<br>
If gear doesn't move it is likley that the pin configuration for `step_pin` and/or `enable_pin` are incorrect. Verify the pin names and prefix the pin with `!` to invert the signal. E.g.

```yml
enable_pin: !mmu:MMU_GEAR_ENABLE
 (or)
enable_pin: mmu:MMU_GEAR_ENABLE
```

If the gear moves the wrong way the `dir_pin` is inverted. Either add or remove the `!` prefix:

```yml
dir_pin: !mmu:MMU_GEAR_DIR
  # or
dir_pin: mmu:MMU_GEAR_DIR
```


## Step 3. Check the Encoder

We need to check that the Encoder is wired correctly. Run the command `MMU_ENCODER` and note the position displayed.

```yml
MMU_ENCODER
Encoder position: 23.4
```

Insert some filament (from either side) and pull backwards and forwards.  You should see the red LED flashing behind the enraged rabbit's eyes. Rerun `MMU_ENCODER` and validate the position displayed has increased (note that the encoder is not direction aware, so it will always increase in reading).

If the encoder postion does not change, validate the `encoder_pin` is correct. It shouldn't matter if it has a `!` (inverted) or not, but it might require a `^` (pull up resister) to function.

```yml
[mmu_encoder mmu_encoder]
encoder_pin: ^mmu:MMU_ENCODER	
```


## Step 4. Check other sensors (if fitted)

Other sensors are generally filament sensors and act on a switch. The easiest way to check these is to run something similar to the following for each sensor/switch.

```yml
QUERY_FILAMENT_SENSOR SENSOR=mmu_gate_sensor
Filament Sensor mmu_gate_sensor: filament not detected
```

Activate the sensor with a piece of filament and run again:

```yml
QUERY_FILAMENT_SENSOR SENSOR=mmu_gate_sensor
Filament Sensor mmu_gate_sensor: filament detected
```

Note that endstops / filament sensors that are wired normally open (NO) frequently require `^` (pull up resister) to correctly function.


## Step 5. Check Servo

> [!IMPORTANT] 
> The Servo Arm should *not* be installed yet for this test!

Ok, last sanity check. Check that the servo you have fitted is operational. Run this simple commmand. The servo should wiggle somewhere short of the configured 'up' and 'down' positions. Don't worry yet about calibration. That comes next.

```yml
MMU_TEST_BUZZ_MOTOR MOTOR=servo
```

You can also try:
```yml
MMU_SERVO POS=down
MMU_SERVO POS=up
```

All we are checking is that the servo is wired and operational.

> [!NOTE] 
> It is normal for the Gear motor to move back and forth slightly during a `MMU_SERVO POS=down` command. This is to ensure that the BMG gears mesh properly.


### ERCF Setup Steps:
- [Flashing Your Local MCU](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Flashing-Local-MCU.md)
- [Installing Happy Hare](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Installing-Happy-Hare.md)
- [Happy Hare Configuration](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Happy-Hare-Configuration.md)
- Hardware Configuration Checks
- [Hardware Calibration](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Hardware-Calibration.md)
- [Toolhead Distances](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Toolhead-Distances.md)
- [Installing KlipperScreen Happy Hare](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Installing-KlipperScreen.md)
- [Slicer Setup](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Slicer-Setup.md)
- [Further Mods to Consider](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/main/Documentation/Further-Mods.md)

#### Even more Happy Hare info can be found at:
- [Happy Hare Wiki](https://github.com/moggieuk/Happy-Hare/wiki)