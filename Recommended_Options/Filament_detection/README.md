# Enraged Rabbit Toolhead Filament detection

Welcome to the dedicated page for exploring the various options available for Toolhead Filament detection as part of the Enraged Rabbit Project. This crucial step is implemented to meticulously check for any potential errors that might occur during the filament's loading and unloading phases. The ERCFv2 team advocates for the utilization of a toolhead sensor only or dual-sensor system. In this section, you will find a comprehensive collection of standalone sensor options compatible with popular toolheads.

## Note
**secured bowden**
> This guide predominantly endorses configurations where the Bowden tube is securely fastened using a Push-Fit or ECAS connection. We wish to highlight that there are certain toolheads, such as the stock cw2, where the Bowden tube is simply inserted without any additional securing mechanism. Such setups present a heightened risk of the Bowden tube dislodging from its holder in the event of a filament clog. Due to this increased risk factor, we do not recommend these types of setups.
---
**using a filament cutter toolhead**
> For users who have integrated the ERF filament cutter into their systems, it is essential to refer to the toolhead modifications outlined in [the specific folder](../ERF_Filament_Cutter). Please be aware that the setups discussed here do not include a cutting feature. Our aim is to provide you with a thorough understanding and the necessary resources to ensure optimal performance and reliability in your filament inspection process.
---

## Options
**1. Toolhead and Entry Sensor**  
This setup allows the firmware (Happy Hare) to quickly load bowden and optionally home prior to extruder, then home to toolhead sensor before loading to the nozzle. The entry sensor also allow for easier calibration of the bowden length.  The twin sensors also allows for precise location of the filament in an error situation which increases the chances of automatic recovery. The downside is that you need two switch inputs to your MCU. **This is the luxury option.**  
   
✔ physical clogg detection between ERCF and Extruder (It is detected whether the filament is fed to the toolhead extruder.)  
✔ physical clogg detection after Extruder (It is detected whether the filament is being fed by the toolhead extruder into the nozzle.)  

**2. Toolhead Sensor only**  
Which this setup the firmware can quickly load close to the nozzle and then precisely home to the toolhead sensor inside the extruder. The presence of the toolhead sensor is highly valuable in a MMU so the firmware allowing detection of correct behavior, smooth loading and auto recovery. This is usually an easy setup to accomodate and many toolhead boards or MCUs provide for this input. This option has no physical detection if the filament stuck in front of the extruder. **This is the most common recommended option.**  
  
✘ no clogg detection  between ERCF and Extruder (Aside from the ERCF encoder, there is no detection of whether the filament is being fed to the toolhead extruder.)  
✔ physical clogg detection after Extruder (It is detected whether the filament is being fed by the toolhead extruder into the nozzle.)  


**3. Entry Sensor only**  
Which this setup the firmware can quickly load close to the extruder and then precisely home to the toolhead sensor inside the extruder. The presence of the toolhead sensor is highly valuable in a MMU so the firmware allowing detection of correct behavior, smooth loading and auto recovery. This is usually an easy setup to accomodate and many toolhead boards or MCUs provide for this input. **This is better then nothing.**  
     
✔ physical clogg detection between ERCF and Extruder (It is detected whether the filament is fed to the toolhead extruder.)  
✘ no clogg detection after Extruder (Aside from the ERCF encoder, there is no detection whether the filament is being fed by the toolhead extruder into the nozzle.)  

**4. No Sensor**  
This setup has no sensors and is thus not recommended but it can be used if you have not other options with Happy Hare. It does include a secure bowden connection (ECAS or push fit) which is essential because the filament will be colliding with the extruder entrance. If you have no pyhsical sensor your should look for a software detection like ([Happy-Hare](https://github.com/moggieuk/Happy-Hare)). **This is not recommended.**  
  
✘ no clogg detection between ERCF and Extruder (Aside from the ERCF encoder, there is no detection whether the filament is being fed to the toolhead extruder.)  
✘ no clogg detection between after and Nozzle (Aside from the ERCF encoder, there is no detection whether the filament is being fed the toolhead extruder into the nozzle.)  
  
<img src="./Assets/sensor_explained.png" alt="Position of the sensor" width="200"/>
<p><em>Position of the sensor</em></p>

---

## Parts

<details>
<summary><strong>Expand for Stealthburner Options</strong></summary>
<table>
  <tr>
    <th>Extruder</th>
    <th>1. Toolhead &amp; Entry Sensor</th>
    <th>2. Toolhead Sensor</th>
    <th>3. Entry Sensor</th>
    <th>4. No Sensor</th>
  </tr>
  <tr>
    <td>Clockwork 2</td>
   <td> <a href="./stls/1_toolhead_entry_sensors/[a]_cw2_latch.stl">Latch</a> <br> <a href="./stls/1_toolhead_entry_sensors/cw2_body.stl">Body</a> <br> <a href="./stls/1_toolhead_entry_sensors/cw2_plate.stl">Plate</a> <br> additional items: <br> 1x ECAS <br> 2x D2F-5 <br>2x ball 5,5mm <br> 4x self tapping screw M2x10 <br> design by Petr Kašpar</a></td>
    <td> <a href="./stls/2_toolhead_sensor/cw2_body.stl">Body</a> <br> <a href="./stls/2_toolhead_sensor/[a]_cw2_latch.stl">Latch</a> <br>additional items: <br> 1x ECAS <br> 1x D2F-5 <br>1x ball 5,5mm <br> 2x self tapping screw M2x10 <br> design by Garth Snyder </td>
    <td></td>
    <td> <a href="./stls/4_no_sensor/cw2_body.stl">Body</a> <br>additional items: <br> 1x ECAS <br> design by Garth Snyder </td>
  </tr>
  <tr>
    <td>Orbiter 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>LGX Lite</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Galileo 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>other extruder</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
</details>

<details>
<summary><strong>Expand for XOL2 Options</strong></summary>
<table>
  <tr>
    <th>Extruder</th>
    <th>1. Toolhead &amp; Entry Sensor</th>
    <th>2. Toolhead Sensor</th>
    <th>3. Entry Sensor</th>
    <th>4. No Sensor</th>
  </tr>
  <tr>
    <td>Clockwork 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Orbiter 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>LGX Lite</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Galileo 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>other extruder</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>

</details>
<details>
<summary><strong>Expand for other toolhead options</strong></summary>
<table>
  <tr>
    <th>Extruder</th>
    <th>1. Toolhead &amp; Entry Sensor</th>
    <th>2. Toolhead Sensor</th>
    <th>3. Entry Sensor</th>
    <th>4. No Sensor</th>
  </tr>
  <tr>
    <td>Clockwork 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Orbiter 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>LGX Lite</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Galileo 2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>other extruder</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>
</details>
