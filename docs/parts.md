# 🧩 Parts list

This page lists the hardware parts required to build the **Chronology NAS** physical enclosure.

The current build uses a custom 3D-printed case, an x86 Chromebox board, internal AC-DC power supply, internal drive with hot-swap approach.

> [!CAUTION]
> This build contains mains-powered AC-DC components. Use only suitable parts, proper insulation, strain relief, and safe wiring practices.

---

## 🧭 Parts navigation

| ID | Part                       | Section                                          |
| -: | -------------------------- | ------------------------------------------------ |
| 01 | x86 Chromebox              | [Chromebox](#01-chromebox)                       |
| 02 | 3D-printed enclosure       | [Enclosure](#02-3d-printed-enclosure)            |
| 03 | AC-DC PSU                  | [AC-DC PSU](#03-ac-dc-psu)                       |
| 04 | AC input parts             | [AC input](#04-ac-input-parts)                   |
| 05 | Low-voltage wiring         | [DC wiring](#05-low-voltage-dc-wiring)           |
| 06 | Chromebox power connector  | [Power connector](#06-chromebox-power-connector) |
| 07 | Storage interface          | [Storage interface](#07-storage-interface)       |
| 08 | Drive sleds                | [Drive sleds](#08-drive-sleds)                   |
| 09 | SATA drives                | [Drives](#09-sata-drives)                        |
| 10 | Screws, inserts, standoffs | [Fasteners](#10-fasteners-inserts-and-standoffs) |
| 11 | Thermal service parts      | [Thermal parts](#11-thermal-service-parts)       |
| 12 | Vibration damping          | [Vibration damping](#12-vibration-damping)       |
| 13 | Optional cooling           | [Optional cooling](#13-optional-cooling)         |

---

<a id="01-chromebox"></a>

## 01 — 💻 Chromebox

| Field        | Value                                                |
| ------------ | ---------------------------------------------------- |
| Page link    | TBD                                                  |
| Function     | Main x86 board                                       |
| Notes        | TBD |

<details>
  
<summary><strong>How to choose an alternative / reference notes</strong></summary>

<br>

Look for:

* ASUS / HP / Acer / Dell Chromebox models;
* Intel or AMD x86_64 CPU;
* removable case;
* accessible motherboard;
* USB 3.0 ports;
* Ethernet port;
* replaceable RAM and SSD if possible.

Avoid:

* ARM ChromeOS devices;
* devices with unknown firmware state;
* units with liquid damage;
* units without power adapter unless you are ready to verify the required voltage/current.

Reference photos to add:

```text
assets/photos/parts/chromebox-front.jpg
assets/photos/parts/chromebox-opened.jpg
assets/photos/parts/chromebox-board.jpg
assets/photos/parts/chromebox-power-input.jpg
```

</details>

---

<a id="02-3d-printed-enclosure"></a>

## 02 — 🧱 3D-printed enclosure

| Field        | Value                                                |
| ------------ | ---------------------------------------------------- |
| Page link    | TBD                                                  |
| Function     | Main x86 board                                       |
| Notes        | TBD |

---

<details>
The enclosure contains:

| Field                    | Value                                                     |
| ------------------------ | --------------------------------------------------------- |
| **Core chassis**         | Main load-bearing internal structure                      |
| **Outer support frame**  | Secondary frame installed over the core chassis           |
| **Outer shell**          | External visible body / facade of the enclosure           |
| **Drive ejector levers** | Printed levers used to push drives out                    |
| **Power button bracket** | Small internal beam/bracket for mounting the power button |
| **Top cover parts**      | Decorative protective covers above ventilation openings   |
| **I/O port cover**       | Cover for the Chromebox board I/O port area               |

<br>


```text
cad/enclosure/
cad/drive-sleds/
assets/photos/parts/enclosure-overview.jpg
assets/photos/parts/enclosure-top-mesh.jpg
assets/photos/parts/enclosure-drive-bay.jpg
```

</details>

---

<a id="03-ac-dc-psu"></a>

## 03 — 🔌 AC-DC PSU

| Field        | Value                                                               |
| ------------ | ------------------------------------------------------------------- |
| Current part | **Mean Well RPS-65-12**                                             |
| Output       | 12 V / 5.42 A                                                       |
| Rated power  | 65 W                                                                |
| Function     | Internal power supply for the Chromebox and drives                  |
| Notes        | I do **not** recommend replacing this PSU with a random alternative |

> [!CAUTION]
> This part works with mains voltage. Incorrect AC wiring, poor insulation, missing strain relief, or unsafe mounting may cause electric shock, fire, hardware damage, injury, or death.
> Do not work on the PSU while it is connected to mains power. Verify wiring, polarity, insulation, clearances, and mechanical fixation before first power-on.


<details>


The current build uses a **Mean Well RPS-65-12**.

>I do not recommend replacing it with a random low-cost AC-DC module. The RPS series is a certified medical/open-frame power supply family designed for built-in equipment (medical / biochemical inspection instruments / BF-rated patient-contact medical equipment when used with appropriate system design). It provides proper isolation, documented safety approvals, low >leakage current, and standard protection features such as short-circuit, overload, and overvoltage protection.

The 65 W rating is also intentionally oversized for this build.

Measured maximum power consumption in the current test setup:

| Test condition                                                      | Measured power |
| ------------------------------------------------------------------- | -------------: |
| CPU + iGPU + RAM stress test + HDD Victoria mechanical/surface test |         < 35 W |
| IDLE + HDD not parked                                               |         < 18 W |
| IDLE + HDD parked                                                   |         < 14 W |
| System OFF                                                          |          < 1 W |


This means the PSU is not operated near its limit during the tested worst-case load. The remaining power margin is intentional and helps avoid running the PSU at the edge of its rating.

<table>
  <tr>
    <td width="50%"><img src="../gallery/parts/PSU_front.jpg" width="100%"></td>
    <td width="50%"><img src="../gallery/parts/PSU_back.jpg" width="100%"></td>
  </tr>
</table>

</details>

---

<a id="04-ac-input-parts"></a>

## 04 — ⚡ AC input parts

<a id="04-ac-input-parts"></a>

## 04 — ⚡ AC input parts


| Field        | Value                                                  |
| ------------ | ------------------------------------------------------ |
| Current part | TBD                                                    |
| Function     | Mains power input for the internal AC-DC PSU           |
| Notes        | The socket must match the specified dimensions exactly |

> [!CAUTION]
> This part is connected to mains voltage. Incorrect wiring, poor insulation, or exposed live terminals may cause electric shock, fire, injury, or death.

<details>

The AC input socket must match the specified size and shape exactly.

The enclosure design uses minimal mechanical tolerances around this component. A socket with a different body shape, mounting hole spacing, flange size, terminal position, or overall depth may not fit the printed enclosure.

Before buying an alternative, verify:

<table>
  <tr>
    <td width="50%"><img src="../gallery/parts/AC-socket.jpg" width="100%"></td>
    <td width="50%"><img src="../gallery/parts/AC-socket.jpg" width="100%"></td>
  </tr>
</table>

</details>


---

<a id="05-low-voltage-dc-wiring"></a>

## 05 — 🔋 Low-voltage DC wiring


| Field    | Value                                         |
| -------- | --------------------------------------------- |
| Required | ✅ Yes                                         |
| Quantity | 1 set                                         |
| Voltage  | 12 V DC                                       |
| Function | Distributes 12 V power inside the enclosure   |
| Notes    | Wire gauge depends on drive count and current |



---

<a id="07-storage-interface"></a>

## 07 — 💾 Storage interface


| Field        | Value                                            |
| ------------ | ------------------------------------------------ |
| Current part | TBD                                              |
| Function     | Connects SATA drives to the Chromebox            |
| Notes        | Exact implementation depends on the final design |

<details>
<summary><strong>How to choose an alternative / reference notes</strong></summary>

<br>

Search keywords:

```text
USB 3.0 SATA adapter UASP
USB SATA bridge board
USB 3.0 to SATA 22 pin
USB SATA adapter 3.5 HDD 12V
```

Check:

* USB 3.0 support;
* UASP support;
* SATA connector orientation;
* 2.5" / 3.5" drive compatibility;
* external 12 V power support if needed;
* bridge chip reputation;
* board dimensions;
* cable direction.

Avoid:

* bus-powered 3.5" HDD setups;
* very thin USB cables;
* adapters without clear power input;
* boards that physically block drive sled movement.

Reference photos to add:

```text
assets/photos/parts/storage-interface-board.jpg
assets/photos/parts/storage-interface-mounted.jpg
assets/photos/parts/sata-connector-alignment.jpg
```

</details>

---

<a id="12-vibration-damping"></a>

## 12 — 🧽 Vibration damping

| Field        | Value                                   |
| ------------ | --------------------------------------- |
| Required     | Recommended                             |
| Quantity     | 1 set                                   |
| Current part | Rubber feet / pads                      |
| Function     | Reduces HDD vibration and surface noise |
| Notes        | More important for 3.5" HDD builds      |

Typical parts:

* rubber feet;
* silicone pads;
* thin foam strips;
* anti-vibration washers.

<details>
<summary><strong>How to choose alternatives</strong></summary>

<br>

Search keywords:

```text
rubber feet electronics
silicone vibration pad
HDD anti vibration washer
adhesive rubber bumper
```

Check:

* temperature resistance;
* adhesive strength;
* compression;
* clearance;
* whether the material touches hot components.

Reference photos to add:

```text
assets/photos/parts/rubber-feet.jpg
assets/photos/parts/vibration-pad-placement.jpg
```

</details>
