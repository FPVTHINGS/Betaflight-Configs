# Betaflight configs for various micros 

If you found your way here, welcome to my collection of Betaflight configs for various FPV builds. Shared as community reference starting points to help save someone some time. These are real, well-flown configs — use them to bootstrap a similar build and save some time.

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

| File | Aircraft | Size | Video | Style |
|---|---|---|---|---|
| [Airbula65_Analog_Race_1S.txt](Airbula65_Analog_Race_1S.txt) | Air65 R Custom | 1S Whoop | Analog | Racing backup / Indoor Freestyle |
| [BabyTurtle_Analog_1S_2inch.txt](BabyTurtle_Analog_1S_2inch.txt) | Baby Turtle Custom 2" | 2" | Analog | Freestyle / Indoor Proximity |
| [Carnage_HDZero_3S-4S_3.5inch.txt](Carnage_HDZero_3S-4S_3.5inch.txt) | Carnage V2 3.5" | 3S–4S 3.5" | HDZero | Freestyle |
| [Carnage_HDZero_4S_3inch.txt](Carnage_HDZero_4S_3inch.txt) | Carnage V2 3" | 4S 3" | HDZero | Freestyle |
| [Crux35_Analog_3S-4S_3.5inch.txt](Crux35_Analog_3S-4S_3.5inch.txt) | IFlight Crux35 3.5" (Modified) | 3S–4S 3.5" | Analog | Freestyle |
| [Kayoumini_HDZero_2S_2.5inch.txt](Kayoumini_HDZero_2S_2.5inch.txt) | Kayoumini 2.5" | 2S 2.5" | HDZero | Freestyle / Yard Basher |
| [Mobula6_HDZero_Race_1S.txt](Mobula6_HDZero_Race_1S.txt) | BetaFPV Mobula6 HD Eco Race | 1S Whoop | HDZero | Whoop Racing |
| [Mobula7_HDZero_1S.txt](Mobula7_HDZero_1S.txt) | HappyModel Mobula7 HD | 1S Whoop | HDZero | Whoop Freestyle / Racing |
| [Mobula8_HDZero_2S_2inch.txt](Mobula8_HDZero_2S_2inch.txt) | HappyModel Mobula8 HD ECO | 2S 2" Whoop | HDZero | Whoop Freestyle |
| [TinyTrainer_V2_HDZero_3S.txt](TinyTrainer_V2_HDZero_3S.txt) | Tiny Trainer V2 3" | 3S 3" | HDZero | Racing / Freestyle |
| [Toothgrinder_MAX_Analog_2S.txt](Toothgrinder_MAX_Analog_2S.txt) | Toothgrinder 2.5" | 2S 2.5" | Analog | Freestyle / Yard Basher |

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
