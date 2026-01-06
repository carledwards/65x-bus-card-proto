# 65x Bus Prototype Cards

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

Prototype cards for the 65x Bus system in 5V and 3.3V variants.

## Overview

This repository contains two prototype card designs for custom circuit development on the 65x Bus. Both use extended depth (220mm) to maximize prototyping space and include address decoding logic.

## Variants

### 5V Prototype Card (`/hardware/5v/`)

General-purpose prototyping area for 5V TTL circuits.

| Parameter | Value |
|-----------|-------|
| Board Format | Eurocard 3U, 160mm × 220mm |
| Logic Level | 5V TTL |
| Proto Area | ~140 × 180 mm |
| Default Address | $8300–$83FF (Slot 3) |
| Address Decode | 74HCT688 + 74HCT138 (8 × 32-byte regions) |

### 3.3V Prototype Card (`/hardware/3v3/`)

Prototyping area for 3.3V LVCMOS circuits with level shifting.

| Parameter | Value |
|-----------|-------|
| Board Format | Eurocard 3U, 160mm × 220mm |
| Logic Level | 3.3V LVCMOS |
| Proto Area | ~140 × 160 mm |
| Default Address | $8400–$84FF (Slot 4) |
| Level Shifters | 74LVC245 (bidirectional data, unidirectional control) |
| 3.3V Regulator | AMS1117-3.3 LDO (500 mA) |

## Features (Both Cards)

- Jumper-selectable I/O slot address (0–15)
- 74HCT138 sub-address decode (8 × 32-byte regions)
- Bus signal header with address, data, and control signals
- +5V/+3.3V and GND power rails along proto area edges
- Optional DiagModule connector

## Hardware

- 5V card: `/hardware/5v/`
- 3.3V card: `/hardware/3v3/`

### Status

🚧 **In Development**

## Related

- [65x Bus Specification](https://github.com/carledwards/65x-bus-spec) — Full bus specification and documentation

## License

This work is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

You are free to use, modify, and manufacture this design for personal, non-commercial purposes with attribution. Commercial use requires permission from the author.

