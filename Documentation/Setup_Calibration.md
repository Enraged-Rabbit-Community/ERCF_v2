# Hardware configuration, Movement and Homing


## Step 1. Install Happy Hare software
Please follow the [install guide for Happy Hare](https://github.com/moggieuk/Happy-Hare/tree/main?tab=readme-ov-file#---installation).


## Step 2. Validate your hardware configuration

### Location of configuration files
The Klipper configuration files for Happy Hare are modular and can be found in this layout in the Klipper config directory:

```yml
mmu/
  base/
    mmu.cfg
    mmu_filametrix.cfg
    mmu_hardware.cfg
    mmu_software.cfg
    mmu_sequence.cfg
    mmu_parameters.cfg

  optional/
    mmu_menu.cfg
    mmu_ercf_compat.cfg
    client_macros.cfg

  mmu_vars.cfg
```

This makes the minimal include into your printer.cfg easy: `[include mmu/base/*.cfg]`.  That will also ensure the correct load order!

<br>

### a) MCU and Pin Validation (mmu.cfg)
The `mmu.cfg` file is part of the hardware configuration but defines aliases for all of the pins used in `mmu_hardware.cfg`. The benefit of this is that configuration frameworks like [Klippain](https://github.com/Frix-x/klippain) can more easily incorporate. It is also in keeping with an organized modular layout.

<br>

### b) Hardware Configuration (mmu_hardware.cfg):
This can be daunting but the interactive installer will make the process easier for common mcu's designed for a MMU (e.g. ERCF EASY-BRD, Burrows ERB, etc) and perform most of the setup for you. A few tweaks remain and include the setting of endstop options, optional extruder "touch" homing as the usual pin invert checking, etc.

Endstop setup and options can be [found here](#---endstops-and-mmu-movement)

Note that all sensors can be setup with a simple section in `mmu_hardware.cfg`.  This ensures things are setup correctly and only requires you to supply the pins:
```yml
# FILAMENT SENSORS ---------------------------------------------------------------------------------------------------------
# Define the pins for optional sensors in the filament path. All but the pre-gate sensors will be automatically setup as
# both endstops (for homing) and sensors for visibility purposes.
#
# pre_gate_switch_pin_X: pre-gate sensor detects filament at entry to MMU. X=gate number (0..N)
# toolhead_switch_pin: 'toolhead' sensor detects filament after extruder entry
# extruder_switch_pin: 'extruder' sensor detects filament just before the extruder entry
# gate_switch_pin: shared 'gate' sensor detects filament at the gate of the MMU (alternative to encoder)
#
# Uncomment sensors that are fitted
#
[mmu_sensors]
pre_gate_switch_pin_0: mmu:MMU_SEL_ENDSTOP
pre_gate_switch_pin_1: mmu:MMU_SEL_ENDSTOP
pre_gate_switch_pin_2: mmu:MMU_SEL_ENDSTOP
pre_gate_switch_pin_3: mmu:MMU_SEL_ENDSTOP

gate_switch_pin: mmu:MMU_SEL_ENDSTOP
extruder_switch_pin: mmu:MMU_SEL_ENDSTOP
toolhead_switch_pin: PG13
```

<br>

### c) Variables file (mmu_vars.cfg):
This is the file where Happy Hare stores all calibration settings and state. It is pointed to by this section at the top of `mmu_software.cfg`:
```
[save_variables]
filename: /home/pi/printer_data/config/mmu/mmu_vars.cfg
```

Klipper can only have one `save_variables` file and so if you are already using one you can simply comment out the lines above and Happy Hare will append into your existing "variables" file.

If all other pin's and setup look correct *RESTART KLIPPER* and proceed to step 2.

<br>

## Step 3. Check endstops & Optional sensors
Verify that the necessary endstops are working and the polarity is correct. The recommended procedure is:
```yml
MMU_MOTORS_OFF
  # remove filament from ERCF and extruder, move selector to center of travel
QUERY_ENDSTOPS
  # or use the visual query in Mainsail or Fluuid
```
Validate that you can see:
```yml
mmu_sel_home:open (Essential)
toolhead:open (Optional if you have a toolhead sensor)
```
Then manually press and hold the selector microswitch and rerun `QUERY_ENDSTOPS`.<br>
Validate that you can see `mmu_sel_home:TRIGGERED` in the list.<br>
If you have toolhead sensor, feed filament into the extruder past the switch and rerun `QUERY_ENDSTOPS`.<br>
Validate that you can see `toolhead:TRIGGERED` in the list.

If either of these don't change state then the pin assigned to the endstop is incorrect.  If the state is inverted (i.e. enstop transitions to `open` when pressed) the add/remove the `!` on the respective endstop pin either in the `[stepper_mmu_selector]` block for selector endstop or in `[filament_switch_sensor toolhead_sensor]` block for toolhead sensor.

Other endstops like "touch" operation are advanced and are not cover by this inital setup.

<br>

## Step 4. Check motor movement and direction
Once pins are correct it is important to verify direction.  It is not possible for the installer to ensure this because it depends on the actual stepper wiring.  The recommended procedure is:
```yml
MMU_MOTORS_OFF
  # move selector to the center of travel
MMU_HOME
  # verify that the selector moves to the left towards the home position
```
If the selector doesn't move or moves the wrong way open up `mmu_hardware.cfg`, find the section `[stepper_mmu_selector]`:<br>
If selector doesn't move it is likley that the pin configuration for `step_pin` and/or `enable_pin` are incorrect. Verify the pin names and prefix the pin with `!` to invert the signal. E.g.
```yml
enable_pin: !mmu:MMU_SEL_ENABLE
  # or
enable_pin: mmu:MMU_SEL_ENABLE
```
If the selector moves the wrong way the `dir_pin` is inverted. Either add or remove the `!` prefix:
```yml
dir_pin: !mmu:MMU_SEL_DIR
  # or
dir_pin: mmu:MMU_SEL_DIR
```

Now repeat the exercise with the gear stepper:
```yml
MMU_MOTORS_OFF
  # remove any filament from your MMU
MMU_TEST_MOVE MOVE=100
  # verify that the gear stepper would pull filament towards the extruder
MMU_TEST_MOVE MOVE=-100
  # verify that the gear stepper is push filament away from the extruder
```
If the gear stepper doesn't move or moves the wrong way open up `mmu_hardware.cfg`, find the section `[stepper_mmu_gear]`:<br>
If gear doesn't move it is likley that the pin configuration for `step_pin` and/or `enable_pin` are incorrect. Verify the pin names and prefix the pin with `!` to invert the signal. E.g.
```yml
enable_pin: !mmu:MMU_GEAR_ENABLE
  # or
enable_pin: mmu:MMU_GEAR_ENABLE
```
If the gear moves the wrong way the `dir_pin` is inverted. Either add or remove the `!` prefix:
```yml
dir_pin: !mmu:MMU_GEAR_DIR
  # or
dir_pin: mmu:MMU_GEAR_DIR
```

<br>

## Step 5. Check Encoder
Ok, last sanity check.  We need to check that the Encoder is wired correctly. Run the command `MMU_ENCODER` and note the position displayed.
```yml
MMU_ENCODER
Encoder position: 23.4
```
Insert some filament (from either side) and pull backwards and forwards.  You should see the LED flashing.  Rerun `MMU_ENCODER` and validate the position displayed has increased (note that the encoder is not direction aware so it will always increase in reading)

If the encoder postion does not change, validate the `encoder_pin` is correct. It shouldn't matter if it has a `!` (inverted) or not, but it might require a `^` (pull up resister) to function.
```yml
[mmu_encoder mmu_encoder]
encoder_pin: ^mmu:MMU_ENCODER	
```

<br>

Attaching the Servo Arm (Finally!)

NOTE: this guide assumes you are using a Savox Servo. If you are using an MG90S or other servo, the angles you need to use will be different!

Run the command `MMU_SERVO POS=UP` prior to attaching the servo arm. When attaching the arm, do not twist the servo output shaft, or you will need to run the command again. As you attach the servo arm, you want it to be aligned as close to the body of the servo as possible given the position of the servo output shaft.

Once the servo arm is attached and screwed into place, run the command `MMU_SERVO ANGLE=30` (for Savox, 140 for MG90S) and slowly increase the angle to fine tune the correct "up" angle where the servo arm just hits the servo body. Save this value to you `mmu_parameters.cfg` as `servo_up_angle` on line 48.

Manually position selector over one of the gates. Run the command `MMU_SERVO POS=DOWN`.  The servo should move to the marked position on the tophat and the arrows should align, but not go too far.  If the angle isn't correct, then use `MMU_SERVO ANGLE=140` (for Savox, 30 for MG90S) to try angles close to current down angle to get exactly the right angle. See pic at the bottom of this page: [https://github.com/moggieuk/ERCF-Springy](https://github.com/moggieuk/ERCF-Springy)
Once you've got the angle correct, save it to you `mmu_parameters.cfg` as `servo_down_angle` on line 49.

Run the command `MMU_SERVO POS=MOVE`.  Servo will move to "move" position in the "cutout" on the top hat that allows for free movement. If the angle is not correct then use `MMU_SERVO ANGLE=30` (for Savox, 140 for MG90S) to try angles close to current move angle to get exacly the right position.
Once you've got the angle correct, save it to you `mmu_parameters.cfg` as `servo_move_angle` on line 50.

Restart Klipper. 

Put another way, the default installer will get you values close to correct, but you must fine tune these three positions.

Note: If servo moves in the wrong direction it is likely you picked the wrong servo when running the Happy Hare installer.... remove servo arm, read the notes in mmu_parameters.cfg, correct starting servo angles, restart klipper, and try again.

Further calibration steps and instructions can be found in the [Happy Hare repo](https://github.com/moggieuk/Happy-Hare?tab=readme-ov-file#---setup-and-calibration).
