# Ender 3 v2 Klipper Configuration

## Hardware
* Base: Ender 3 v2 (2020)
* Mainboard: SKR Mini E3 V3.0
* Hotend Assembly: Hero Me Gen 6 (TODO: Stealthburner)
  * Hotend: TriangleLab V6 (PTFE Heatbreak for PLA)
  * Extruder: Orbiter v1.5
  * Hotend fan: Sunon MF40202V2-A99 24V
  * Part fan: 2x WINSINN 5015 24V "Dual Ball" Hydraulic Bearing
  * ABL: Antclabs BLTouch Smart V3.1 (genuine)

## Slicer Config

### Start G-Code

```
M104 S0 ; removes slicer "set hotend temp"
M140 S0 ; removes slicer "set bed temp"
M107 ; turn off fans
START_PRINT BED_TEMP={first_layer_bed_temperature} EXTRUDER_TEMP={first_layer_temperature}
```

### End G-Code

```
END_PRINT
```

