# 🧰 Chronology - Chromebox based DIY NAS

Turn an old x86 Chromebox into a compact DIY NAS-style home server.


> [!IMPORTANT]
>
> ## ⚠️ Safety and liability disclaimer
>
> This guide includes soldering, hardware modification, and the use of an AC-DC power supply connected to mains voltage. Mistakes during assembly may damage your Chromebox, destroy connected hardware, cause data loss, create a fire hazard, or result in electric shock, serious injury, or death.
>
> Follow this guide only if you understand the risks and have the required skills to work safely with electronics and mains-powered equipment. Do not work on live circuits. Always check wiring, polarity, insulation, grounding, and mechanical stability before applying power.
>
> The information in this project is provided **“as is”** and without any warranty. You are solely responsible for deciding whether the build is suitable for your hardware and for performing the work safely.
>
> By repeating this build, you assume all risks. The author is not responsible for damage to equipment, loss of data, personal injury, death, fire, electric shock, or any other direct or indirect consequences resulting from the use of this guide.

---

![Logo](/gallery/assets/BlueprintImage.png)

📸 Final build gallery ➡️ **[photos are stored on a separate gallery pagey](gallery/README.md)**

---

<a id="navigation"></a>

## 🧭 Navigation

* [📸 Final build gallery](gallery/gallery.md)
* [🎯 Project goal](#project-goal)
* [🚧 Project status](#project-status)
* [🏗️ Hardware concept](#hardware-concept)
* [🧩 Parts list](/parts.md)
* [🛠️ Assembly guide](/assembly.md)
* [💻 Chromebox preparation](/chromebox-preparation.md)
* [📜 License](#license)



<a id="project-goal"></a>

## 🎯 Project goal

The goal is to reuse a small x86 Chromebox as a compact, low-power, budget-friendly NAS-like home server.

The hardware build is designed around:

* a reused x86 Chromebox board;
* a custom 3D-printed enclosure;
* an internal AC-DC power supply;
* support for internal 2.5" / 3.5" SATA drives;
* hot-swap-style drive sleds;
* a compact, clean, self-contained build;
* reproducible parts selection with reference photos for finding alternatives.

---

<a id="project-status"></a>

## 🚧 Project status

| Area                  | Status          |
| --------------------- | --------------- |
| Parts list            | In progress     |
| Physical build        | In progress     |
| Mechanical assembly   | In progress     |
| BIOS / firmware guide | Not covered yet |
| OS installation       | Not covered yet |
| NAS software          | Not covered yet |

---

<a id="hardware-concept"></a>

## 🏗️ Hardware concept

The final device is not just a loose Chromebox with external USB drives.

The intended build is a compact self-contained NAS-style unit:

```text
3D-printed enclosure
├─ Chromebox mainboard
├─ Internal AC-DC PSU
├─ Internal power wiring
├─ SATA storage connection
├─ Hot-swap-style drive sleds
└─ Internal 2.5" / 3.5" drive bays
```

The current tests show that the storage section works well without forced HDD cooling in this configuration. Because of this, the build is currently designed as a relatively passive system, with airflow and heat management handled mainly by enclosure geometry and component placement.

> [!NOTE]
> Passive HDD cooling results are based on the current tested configuration. A temperature of 55 degrees on the hottest drive under a 24-hour Victoria Mechanic test + Cinebench R21 load at a room temperature of 22 degrees Celsius is considered an acceptable level of heat. Different drives, ambient temperature, workload may require additional airflow.

---

## 🧩 Parts list

The full parts list is maintained on a separate page:

➡️ **[Open parts list](/parts.md)**

---

## 🛠️ Assembly guide

The full physical assembly guide is maintained on a separate page:

➡️ **[Open assembly guide](/assembly.md)**

---

## 💻 Chromebox preparation

The Chromebox-specific preparation guide is maintained separately:

➡️ **[Open Chromebox preparation guide](/chromebox-preparation.md)**

---

<a id="license"></a>
## 📜 License

Project documentation, photos, diagrams, BOM, CAD files, and 3D-printable models are licensed under **CC BY-NC 4.0**.

You may copy, share, modify, and build upon these materials for **non-commercial purposes only**, provided that you credit the original project and author, link back to the original repository, and clearly mark any modifications.

Commercial use, resale, inclusion in commercial kits, paid services, or commercial publications is not allowed without explicit written permission.
