# Betaflight configs for various micros 

If you found your way here, welcome to my collection of Betaflight configs for various FPV builds. Shared as community reference starting points to help save someone some time. These are real, well-flown configs — use them to bootstrap a similar build and save some config time.

## How to Use

1. **Read the config first.** Review the hardware list in the header comment and note how your build differs.
2. **Do NOT blindly flash.** Lines marked `!! AIRCRAFT-SPECIFIC` are calibrated to this individual unit — you must recalibrate or adjust them for your own hardware.
3. **Paste into Betaflight Configurator → CLI tab.** Paste the entire file contents and press Enter. The config will apply and save automatically.
4. **Recalibrate your accelerometer.** After flashing, go to the Setup tab in Betaflight Configurator and run Accelerometer Calibration.
5. **Verify motor order, spin directions, and props** before arming. ALWAYS props-off for first tests.

---

## ⚠️ Aircraft-Specific Values — Must Adjust for Your Build

| Parameter | Why It's Hardware-Specific |
|---|---|
| `acc_calibration` | IMU calibration unique to each physical FC board. Always re-run Accelerometer Calibration. |
| `align_board_yaw` / `align_board_roll` | Depends on how your FC is physically oriented inside your frame. |
| `vbat_scale` | Voltage sensor calibration. Verify with a multimeter — differs per unit. |
| `ibata_scale` | Current sensor calibration. Calibrate against a known current draw. |
| `gyro_1_align_yaw` | Software gyro orientation — confirm for your specific board version. |
| `motor_output_reordering` | Matches motor wiring on this specific build. Verify your own wiring. |
| `resource MOTOR x` | Pin remapping specific to this AIO board's PCB layout. Confirm pinout for your board revision. |

---

## Builds

| Config File | Aircraft Image | Pack Sizes | VTX | Style |
|---|---|---|---|---|
| [Airbula65_Analog_Race_1S.txt](Airbula65_Analog_Race_1S.txt) | [Airbula65 R](images/Airbula65_Analog_Race_1S.png) | 1S Whoop | Analog | Racing backup / Indoor Freestyle |
| [BabyTurtle_Analog_1S_2inch.txt](BabyTurtle_Analog_1S_2inch.txt) | [Baby Turtle Custom 2"](images/BabyTurtle_Analog_1S_2inch.png) | 1S | Analog | Freestyle / Proximity |
| [Carnage_HDZero_3S-4S_3.5inch.txt](Carnage_HDZero_3S-4S_3.5inch.txt) | [Carnage V2 3.5"](images/Carnage_HDZero_3S-4S_3.5inch.png) | 3S–4S | HDZero | Freestyle |
| [Carnage_HDZero_4S_3inch.txt](Carnage_HDZero_4S_3inch.txt) | [Carnage V2 3"](images/Carnage_HDZero_4S_3inch.png) | 4S | HDZero | Freestyle |
| [Crux35_Analog_3S-4S_3.5inch.txt](Crux35_Analog_3S-4S_3.5inch.txt) | [Crux35 3.5"](images/Crux35_Analog_3S-4S_3.5inch.png) | 3S–4S | Analog | Freestyle |
| [Kayoumini_HDZero_2S_2.5inch.txt](Kayoumini_HDZero_2S_2.5inch.txt) | [Kayoumini 2.5"](images/Kayoumini_HDZero_2S_2.5inch.png) | 2S | HDZero | Freestyle / Yard Basher |
| [Mobula6_HDZero_Race_1S.txt](Mobula6_HDZero_Race_1S.txt) | [Mobula6 HD Eco Race](images/Mobula6_HDZero_Race_1S.png) | 1S Whoop | HDZero | Whoop Racing |
| [Mobula7_HDZero_1S.txt](Mobula7_HDZero_1S.txt) | [Mobula7 HD](images/Mobula7_HDZero_1S.png) | 1S Whoop | HDZero | Whoop Freestyle / Racing |
| [Mobula8_HDZero_2S_2inch.txt](Mobula8_HDZero_2S_2inch.txt) | [Mobula8 HD ECO](images/Mobula8_HDZero_2S_2inch.png) | 2S Whoop | HDZero | Whoop Freestyle |
| [TinyTrainer_V2_HDZero_3S.txt](TinyTrainer_V2_HDZero_3S.txt) | [Tiny Trainer V2 3"](images/TinyTrainer_V2_HDZero_3S.png) | 3S | HDZero | Racing / Freestyle |
| [Toothgrinder_MAX_Analog_2S.txt](Toothgrinder_MAX_Analog_2S.txt) | [Toothgrinder 2.5"](images/Toothgrinder_MAX_Analog_2S.png) | 2S | Analog | Freestyle / Yard Basher |

---

## General Notes

- All configs are `diff all` exports — only values that differ from Betaflight defaults are included.
- All builds use **bidirectional DSHOT** (RPM filtering enabled). Make sure your ESC firmware supports DSHOT300 bidir.
- Rate profiles include three presets per craft: **600°/s full**, **600@85% throttle**, and **533°/s**.
- OSD element positions are included as a reference layout — feel free to rearrange in Configurator.
- VTX band/channel/power settings reflect this pilot's personal preferences — set your own before flying.
- Battery capacity values are set for the batteries used on these specific builds. Adjust for your cell count and capacity.

## License / Usage

These configs are shared freely for the FPV community. Pay attention to notes in the configs, note the build differences, Tune responsibly — always verify settings for your specific hardware before flying.
