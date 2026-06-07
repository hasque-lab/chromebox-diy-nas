## 🔌 AC-DC PSU

| Field        | Value                                                               |
| ------------ | ------------------------------------------------------------------- |
| Current part | **Mean Well RPS-65-12**                                             |
| Output       | 12 V / 5.42 A                                                       |
| Rated power  | 65 W                                                                |
| Function     | Internal power supply for the Chromebox and drives                  |
| Notes        | I do **not** recommend replacing this PSU with a random alternative |

<br>

> [!CAUTION]
> This part works with mains voltage. Incorrect AC wiring, poor insulation, missing strain relief, or unsafe mounting may cause electric shock, fire, hardware damage, injury, or death.
> Do not work on the PSU while it is connected to mains power. Verify wiring, polarity, insulation, clearances, and mechanical fixation before first power-on.

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
    <td width="50%"><img src="pictures/PSU_front.jpg" width="100%"></td>
    <td width="50%"><img src="pictures/PSU_back.jpg" width="100%"></td>
  </tr>
</table>

</details>
