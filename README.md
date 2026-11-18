# UV-K1 / UV-K5 v3 apps (F4WAT)

*English · [Français](README.fr.md)*

Overlay apps for Armel's F4HWN firmware on the Quansheng UV-K1 and UV-K5 v3 radios. They run on top of the firmware without replacing it. This repository is a distribution point to find the latest up-to-date version of each app, in particular for the ADRASEC 27 radios.

The apps here are receive, decode and direction-finding tools. None of them transmits.

## Available apps

| App | Version | Size | Role | Download |
|-----|---------|------|------|----------|
| Scan 406 | 1.9 | 4564 B | Sweeps the Cospas-Sarsat 406 MHz channels, raises an alarm on a burst and hands off to EPIRB 406 for decoding | [Scan406-v1.9.app](apps/scan406/Scan406-v1.9.app?raw=true) |
| EPIRB 406 | 3.6 | 5022 B | Decodes first-generation 406 MHz distress beacons on the radio: 15-hex identifier, country, protocol, position, BCH check | [EPIRB406-v3.6.app](apps/epirb406/EPIRB406-v3.6.app?raw=true) |
| Sig Finder | 2.1 | 3669 B | Direction finding with a directional antenna; detects the characteristic sweep of a 121.5 / 243 MHz distress beacon and flags it | [SigFinder-v2.1.app](apps/sigfind/SigFinder-v2.1.app?raw=true) |

Each app lives in `apps/<name>/`. The file name carries the version. When a new version ships, the versioned file is added next to the old one and the table above points to the latest. Earlier versions stay available in the folder.

## Requirements

A recent F4HWN firmware (Labs or Fusion) on the radio, with app API level 3 or higher. Scan 406 and Sig Finder need EPIRB 406 installed for the hand-off. The firmware and its source code are at Armel's: https://github.com/armel/uv-k1-k5v3-firmware-custom

## Installation

These `.app` files load onto the radio with the F4HWN firmware's overlay-app loader. The file name does not matter to the radio: the version and name shown come from the app header. See the firmware documentation for the loading procedure.

## Source and licence

These apps are derived from Armel's F4HWN firmware. The full source code of each app is public in that repository, on the `feature_update_v7` branch:

- Scan 406: `App/apps/scan406/`
- EPIRB 406: `App/apps/epirb406/`
- Sig Finder: `App/apps/sigfind/` (derived from Armel's FoxHunt app)

Upstream repository: https://github.com/armel/uv-k1-k5v3-firmware-custom

## Use

Amateur radio and emergency (ADRASEC) tools. Receive and decode only. Follow the amateur radio regulations in force.

73, Johan F4WAT
