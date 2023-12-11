# Enraged Rabbit Toolhead Filament Inspection Options Detailed Overview

Welcome to the dedicated page for exploring the various options available for Toolhead Filament Inspection as part of the Enraged Rabbit Project. This crucial step is implemented to meticulously check for any potential errors that might occur during the filament's loading and unloading phases. The ERCFv2 team staunchly advocates for the utilization of a dual-sensor system, incorporating both an entry and toolhead sensor. In this section, you will find a comprehensive collection of standalone sensor options compatible with popular toolheads.

---
**NOTE: secured bowden**
> This guide predominantly endorses configurations where the Bowden tube is securely fastened using a Push-Fit or ECAS connection. We wish to highlight that there are certain toolheads, such as the stock cw2, where the Bowden tube is simply inserted without any additional securing mechanism. Such setups present a heightened risk of the Bowden tube dislodging from its holder in the event of a filament clog. Due to this increased risk factor, we do not recommend these types of setups.
---
**NOTE: using a filament cutter toolhead**
> For users who have integrated the ERF filament cutter into their systems, it is essential to refer to the toolhead modifications outlined in [the specific folder](../ERF_Filament_Cutter). Please be aware that the setups discussed here do not include a cutting feature. Our aim is to provide you with a thorough understanding and the necessary resources to ensure optimal performance and reliability in your filament inspection process.
---
## Illustrative Diagram:
<td><img src="./Assets/sensor_explained.png" alt='Sensor' style='width: 30%;'></td>

---

## Table of Content

- **[Option 1 (recommended): entry sensor and toolhead sensor](#option-1-recommended-entry-sensor-and-toolhead-sensor)**
  - [1.1 Stealthburner Toolhead](#11-stealthburner-toolhead)
  - [1.2 XOL 2 Toolhead](#12-xol-2-toolhead)
  - [1.3 other Toolheads](#13-other-toolheads)
  
- **[Option 2: entry sensor](#option-2-entry-sensor)**
  - [2.1 Stealthburner Toolhead](#21-stealthburner-toolhead)
  - [2.2 XOL 2 Toolhead](#22-xol-2-toolhead)
  - [2.3 other Toolheads](#23-other-toolheads)
  
- **[Option 3: toolhead sensor](#option-3-toolhead-sensor)**
  - [3.1 Stealthburner Toolhead](#31-stealthburner-toolhead)
  - [3.2 XOL 2 Toolhead](#32-xol-2-toolhead)
  - [3.3 other Toolheads](#33-other-toolheads)
  
- **[Option 4 (not recommended): no sensor](#option-4-not-recommended-no-sensor)**
  - [4.1 Stealthburner Toolhead](#41-stealthburner-toolhead)
  - [4.2 XOL 2 Toolhead](#42-xol-2-toolhead)
  - [4.3 other Toolheads](#43-other-toolheads)


---

## Option 1 (recommended): 
This setup allows for checking if the filament gets stuck at the entrance to the extruder and if it gets stuck at the entrance of the nozzle. This setup is recommended to avoid failed prints.
Currently, the following toolheads are available for this variant:
### 1.1 StealthBurner Toolhead
#### Clockwork Extruder
- 
#### LGX Extruder
-
#### Galileo 2 Extruder
-
#### Other Extruder

---
### 1.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- 
#### LGX Extruder
-
#### Galileo 2 Extruder
-
#### Other Extruder

---
### 1.3 other Toolheads
#### Sherpa Mini Extruder
- 
#### LGX Extruder
-
#### Galileo 2 Extruder
-
#### Other Extruder



## Option 2: 
This setup checks if the filament gets stuck at the entrance to the extruder. Once it passes the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.

### 2.1 StealthBurner Toolhead
#### Clockwork Extruder
- [Main Body](./stls/option2/cw2_main_body_with_ECAS_and_sensor.stl) + [latch](./stls/misc/[a]_latch.stl) by [Garth Snyder](https://github.com/GarthSnyder)
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### 2.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### 2.3 other Toolheads
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---

### Option 3: 
This setup checks if the filament gets stuck at the entrance to the nozzle. If the filament cant pass the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.
### StealthBurner Toolhead
#### Clockwork Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### other Toolheads
#### Sherpa Mini Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder


### Option 4 (not recommended):
This setup has only a bowden secure (ecas or push fit).
### StealthBurner Toolhead
#### Clockwork Extruder
- [Main Body](./stls/option4/cw2_main_body_with_ECAS.stl) + [latch](./stls/misc/[a]_latch.stl) by [Garth Snyder](https://github.com/GarthSnyder)

#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder

---
### other Toolheads
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo 2 Extruder
- feel free to add
#### Other Extruder
