# Enraged Rabbit Filament Inspection Options
On this page, you will learn more about Filament Inspection. This step is necessary to check whether any errors have occurred during the loading and unloading process. 
ERCFv2 team highly recommends a entry + toolhead sensor. This folder contains standalone sensor options for popular toolheads.

## Example:
<td><img src="./Assets/sensor_explained.png" alt='Sensor' style='width: 30%;'></td>


> [!NOTE]
> This page only recommends setups where the Bowden is fixed with a Push-Fit or ECAS. There are other toolheads (stock cw2) where the Bowden is merely inserted. In these cases, there is a risk that the Bowden may slip out of the holder in the event of a clog, hence these setups are not recommended.

> [!NOTE]  
> If you are using the ERF filament cutter then you should use the toolhead modification found in that folder. These lack cutting ability.


## Table of Content
**[Variant 1: Toolheads with entry sensor and toolhead sensor (recommended)](#Variant-1)**<br>
**[Variant 2: Toolheads with entry sensor ](#Variant-2)**<br>
**[Variant 3: Toolheads with toolhead sensor ](#Variant-3)**<br>
**[Variant 4: no Sensor](#Variant-4)**<br>


### Variant 1: 
This setup allows for checking if the filament gets stuck at the entrance to the extruder and if it gets stuck at the entrance of the nozzle. This setup is recommended to avoid failed prints.
Currently, the following toolheads are available for this variant:
#### StealthBurner CW2
- SB_CW2_Main_Body_With_2xD2F_ECAS.stl (Entry Sensor + Toolhead Sensor + ECAS)  Credit: [juliusjj25](https://github.com/juliusjj25)  
#### Galileo 2
- Comming soon... please help! 
#### LGX Lite
- Comming soon... please help!
#### Others
- Comming soon... please help!

### Variant 2: 
This setup checks if the filament gets stuck at the entrance to the extruder. Once it passes the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.
#### StealthBurner CW2
- SB_CW2_Main_Body_With_Entry_D2F_ECAS.stl (Entry Sensor + ECAS)
  - Credit: [juliusjj25](https://github.com/juliusjj25)
#### Galileo 2
- Comming soon... please help! 
#### LGX Lite
- Comming soon... please help!
#### Others
- Comming soon... please help!

### Variant 3: 
This setup checks if the filament gets stuck at the entrance to the nozzle. If the filament cant pass the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.
#### StealthBurner CW2
- SB_CW2_Main_Body_With_Entry_D2F_ECAS.stl (Entry Sensor + ECAS)
  - Credit: [juliusjj25](https://github.com/juliusjj25)
#### Galileo 2
- Comming soon... please help! 
#### LGX Lite
- Comming soon... please help!
#### Others
- Comming soon... please help!

### Variant 4 (not recommend): 
This setup needs no special parts. The filament jamming can be detected by the encoder
