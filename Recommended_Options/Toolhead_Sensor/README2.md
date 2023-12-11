# Enraged Rabbit Toolhead Filament detection Options Detailed Overview

Welcome to the dedicated page for exploring the various options available for Toolhead Filament detection as part of the Enraged Rabbit Project. This crucial step is implemented to meticulously check for any potential errors that might occur during the filament's loading and unloading phases. The ERCFv2 team staunchly advocates for the utilization of a dual-sensor system, incorporating both an entry and toolhead sensor. In this section, you will find a comprehensive collection of standalone sensor options compatible with popular toolheads.

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

## Modified parts for Filament Detection on popular toolheads

<details>
<summary>Stealthburner Options</summary>

<table>
<tr>
<td>Extruder:</td>
<th>Toolhead & Entry Sensors</th>
<th>Toolhead Sensor Only</th>
<th>Entry Sensor Only</th>
<th>No Sensor</th>
</tr>

<tr>
  <td>
    CW2
  </td>

  <td>
    <ul>
      <li>Part_X
      <li>Part_Y
    </ul>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>
</tr>

<tr>
  <td>
    Galileo2
  </td>

  <td>
    <ul>
      <li>Part_X
      <li>Part_Y
    </ul>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>
</tr>

<tr>
  <td>
    LGX
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <ul>
      <li><a href="Stls/Foo.stl">Part_X</a>
      <li><a href="Stls/Foo.stl">Part_X</a>
      <li><a href="Stls/Foo.stl">Part_Y</a>
    </ul>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>
</tr>

<tr>
  <td>
    Other
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <ul>
      <li><a href="Stls/Foo.stl">Part_X</a>
      <li><a href="Stls/Foo.stl">Part_X</a>
      <li><a href="Stls/Foo.stl">Part_Y</a>
    </ul>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>
</tr>
</table>

</details>

<details>
<summary>XOL Options</summary>

<table>
<tr>
<td>Extruder:</td>
<th>Toolhead & Entry Sensors</th>
<th>Toolhead Sensor Only</th>
<th>Entry Sensor Only</th>
<th>No Sensor</th>
</tr>

<tr>
  <td>
    XOL 2
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>

  <td>
    <ul>
      <li><a href="Stls/Foo.stl">Part_X</a>
      <li><a href="Stls/Foo.stl">Part_X</a>
    </ul>
  </td>

  <td>
    <sub><i>contribute</i></sub>
  </td>
</tr>

</table>

#### Toolhead & Entry Sensors
This setup allows the firmware (Happy Hare) to quickly load bowden and optionally home prior to extruder, then home to toolhead sensor before loading to the nozzle. The entry sensor also allow for easier calibration of the bowden length.  The twin sensors also allows for precise location of the filament in an error situation which increases the changes of automatic recovery. The downside is that you need two switch imputs to your MCU. **This is the luxury option.**

#### Toolhead Sensor Only
Which this setup the firmware can quickly load close to the extruder and then precisely home to the toolhead sensor inside the extruder. The presence of the toolhead sensor is highly valuable in a MMU so the firmware allowing detection of correct behavior, smooth loading and auto recovery. This is usually an easy setup to accomodate and many toolhead boards or MCUs provide for this input. **This is the most common recommended option**

#### Entry Sensor Only
xxxxxx

#### No Sensor
This setup has no sensors and is thus not recommended but it can be used if you have not other options with Happy Hare. It does include a secure bowden connection (ECAS or push fit) which is essential because the filament will be colliding with the extruder entrance.


---

## AS BEFORE

## Option 1 (recommended): 
This setup allows for checking if the filament gets stuck at the entrance to the extruder and if it gets stuck at the entrance of the nozzle. This setup is recommended to avoid failed prints.
Currently, the following toolheads are available for this variant:
### 1.1 Stealthburner Toolhead
#### Clockwork Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
### 1.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
### 1.3 other Toolheads
#### Sherpa Mini Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder

---

## Option 2: 
This setup checks if the filament gets stuck at the entrance to the extruder. Once it passes the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.

### 2.1 Stealthburner Toolhead
#### Clockwork Extruder
- [Main Body](./stls/option2/cw2_main_body_with_ECAS_and_sensor.stl) + [latch](./stls/misc/[a]_latch.stl) by [Garth Snyder](https://github.com/GarthSnyder)
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
- 
### 2.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add

### 2.3 other Toolheads
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
---

### Option 3: 
This setup checks if the filament gets stuck at the entrance to the nozzle. If the filament cant pass the extruder, any jamming can only be detected by the encoder.
The following toolheads can be equipped with this variant.
### 3.1 Stealthburner Toolhead
#### Clockwork Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
### 3.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
### 3.3 other Toolheads
#### Sherpa Mini Extruder
- feel free to add
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
---

### Option 4 (not recommended):
This setup has only a bowden secure (ecas or push fit).
### 4.1 Stealthburner Toolhead
#### Clockwork Extruder
- [Main Body](./stls/option4/cw2_main_body_with_ECAS.stl) + [latch](./stls/misc/[a]_latch.stl) by [Garth Snyder](https://github.com/GarthSnyder)

#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
### 4.2 XOL 2 Toolhead
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
### 4.3 other Toolheads
#### Sherpa Mini Extruder
- feel free to add 
#### LGX Extruder
- feel free to add
#### Galileo Extruder
- feel free to add
#### Orbiter Extruder
- feel free to add
#### Other Extruder
- feel free to add
  
