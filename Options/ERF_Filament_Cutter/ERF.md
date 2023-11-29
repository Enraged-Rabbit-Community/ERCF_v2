# Enranged Rabbit Filametrix Filament Cutter
<table>
  <tr>
    <td width=30%><img src="Assets/Filametrix_Logo.png" alt='ER Filametrix'></td>
    <td>
      This options adds a lightweight filament cutting option for the Voron Stealthburner toolhead (with a few contributed options) for perfect filament tips without having to tune the traditional tip forming process. Thanks to contributors it supports a number of different hotends. This can lead to much greater reliability of your MMU.
    </td>
  </tr>
</table>

## Illustration
![Image](Assets/ERF.png)
![image](Assets/ERF2.png)

### Main Body

#### SB_CW2 Main Body with various sensor options
- SB_CW2_Main_Body_Cutting_With_2xD2F_ECAS
- SB_CW2_Main_Body_Cutting_With_D2F_ECAS
- SB_CS2_Main_Body_EBB_ECAS_D2F "CW2 main body for the ERCF w/ ECAs, bearing switch, and SB2209 Canbus mods" Thanks to [juliusjj25](https://github.com/juliusjj25)

#### LGX Lite
https://www.printables.com/de/model/576122-lgx-lite-stealthburner-filament-cutter

<br>Credit: tommorox234 via printables.

### Supported Hotends

#### Rapido
- TODO

Credit: [juliusjj25](https://github.com/juliusjj25)

#### Voron Revo
- SB_RevoVoron_back
- SB_RevoVoron_front

Credit: Russell Gower (NOTE currently untested)

#### Bambu Hotend!
- SB_Bambu_cutting_Printhead_back
- SB_Bambu_cutting_Printhead_front or SB_Bambu_cutting_Printhead_front_2
- Bambu_Adapter

Credi: "Jakub Kadlec" from Facebook

#### Mosquito (Slice Engingeering)
https://www.printables.com/de/model/614813-filametrix-mod-for-slice-engingeering-mosquito-hot

Credit: "https://www.printables.com/de/@MakeAUsername_285162"

## Inspiration
@sorted, the project lead for this wants to recognise the inspiration that came from Bambu Labs and the design by @pure100kim who has built the [ERCF_Filament_Cutting_MOD](https://github.com/pure100kim/ERCF_Filament_Cutting_MOD).

## See how it works

Proof of concept 1: https://youtube.com/shorts/HOMG8cVk_U4

Proof of concept 2: https://youtu.be/tTcrxttyths

Filametrix in action: https://www.youtube.com/watch?v=tfMZWQRqtvY

## Good to know

Please be aware:
- We will need to use one of the ADXL mounting threads
- Depending on the setup and position of the cutting point we will most probably not lose any build volume
- For the main body i remixed the ECAS version from [Alexanderor](https://www.printables.com/de/model/433797-clockwork-2-ecas-fitting-for-ercf)

## What you need
### Print list
#### Toolhead
- 1x SB (hotend name) cutting Printhead back
- 1x SB (hotend name) cutting Printhead front
- 1x SB Main body Cutting with ECAS (or with sensor)
- 1x SB motor plate (as Stealthburner has seen a small update the newest plate does not fit anymore. So please use the one from this git)
- 1x SB latch ECAS
- 1x Cutting arm
- 1x Knife holder

#### Cutting point on gantry
- 1x depressor mount
- 1x depressor

#### Cutting point on gantry with servo
- tbd...

### Parts list - considering you already have a Stealthburner with Dragon Hotend

#### Toolhead: 
- Loctite
- 1x M3 nut (DIN934; ideally a countersunk tool to modify the nut for proper filament insertion)
- 2x M3 washer (0.5mm)
- 1x M3x18 SHCS (it repleaces the top left M3x25 SHCS from the SB-Cover mount) 
- 2x Voron heat inserts
- 1x M3x18 FHCS (counter sunk screw)
- 1x M3x8 SHCS
- 1x M2.5x16 SHCS (15-18mm works)
- Spring 0.4x4x15 or alternative of ballpoint pen (L=15mm; D<=4,5mm) (I've ordered some for testing, to have a "defined" spring)
- Type 4 metal hobby blades (we will cut it to length) [Link](https://de.aliexpress.com/item/1005005117830095.html?spm=a2g0o.order_detail.order_detail_item.9.47c26368QwSbBr&gatewayAdapt=glo2deu) Amazon link, these need glue to be held in but work fine (USA) [Link](https://www.amazon.com/dp/B07QP8L1QG)
- ![Image](Assets/Number4_Blades.png)

#### Cutting point on gantry
- 1x M3x16 BHCS
- 1x M3 nut
- 1x M3x8 FHCS
- 2x M3 SHCS (Lengths: 6mm - no backers, 10mm - titanium backers, 12mm - MGN9 rails)
- 2x Voron heat inserts

## Assembly
### Cutting arm
#### Cut skalpel to length l=26mm
![image](Assets/Skalpel_Before_Cut.png)

##### Result
![image](Assets/Skalpel_After_Cut.png)

#### Insert skalpel into knife holder
Insert the skalpel (which is cut to 26mm) into the knife holder until you see it in the little hole. Use pliers to push it into the knife holder. Some force should be needed as the skalpel should stay in place due to the "pressfit". If that's not the case add some glue.(Depending on skalpel tolerances)
![image](Assets/Skalpel_Insertion.png)

#### Put knife holder into cutting arm
The M2.5x15 screw is directly screwed into the plastic of the knife holder. The tip of the screw should be flush with the cutting arm or no more than 0.1-0.3mm above it.
Check the orientation of the hole for the M2.5 screw in the knife holder. It needs to be on the bottom side.

**!! The knife holder must move up and down without friction in the cutting arm but shoult not have a lot play. Maybe some grinding is needed. !!**

![image](Assets/Knife_Holder1.png)
![image](Assets/Knife_Holder2.png)

### Add heat inserts

Tip here for the heat set that goes above the cutter I would suggest drilling the threads out with a ~2.5mm drill bit. On the hotend holder side below the cutter make sure you flare out the PTFE tube to help guide the filament.
#### Main body
![image](Assets/SB_Main_Body.png)
#### SB cutting Printhead back
![image](Assets/SB_Cutting_Printhead.png)
#### Depressor - one on either end, end with ribs should be flush with surface below ribs with no plastic sticking up past surface
![image](Assets/Depressor.png)

#### Finished cutting point assembly should look like this
Note: for titanium backers, the backer should be centered between belt clamps and the end of the depressor mount should be flush with the end of the backer. This will work for all backers with 10/20/40mm spacing with the furthest back hole 5-15mm from the end. Height of depressor should be adjusted to press in the depression on the cutting arm and the BHCS can be adjusted in and out for the right positioning and locked in place with the M3 nut.
![image](Assets/Depressor_Mount.png)


TODO... Add doc page to Happy Hare

### In mmu_parameters.cfg:
set form_tip_macro: _MMU_CUT_TIP

set toolhead_extruder_to_nozzle and toolhead_sensor_to_nozzle to corresponding measured values of your toolhead.

set force_form_tip_standalone: 1


