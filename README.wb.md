wb-cc2652p-flasher
==========================================

This utility allows firmware update for WBE2R-R-ZIGBEE v.2 module.

## Usage

Two usage modes are supported:

### 1. With manual firmware file:

`wb-cc2652p-flasher <module number> <firmware file>`

Example, for module installed in MOD4 slot:

`wb-cc2652p-flasher 4 /mnt/data/CC1352P2_CC2652P_launchpad_coordinator_20250321.hex`

### 2. With automatic latest firmware download:

`wb-cc2652p-flasher <module number> -last`

Example, for module installed in MOD4 slot:

`wb-cc2652p-flasher 4 -last`

## Notes

- You need to stop zigbee2mqtt before updating module firmware: `systemctl stop zigbee2mqtt`
- After flashing, start zigbee2mqtt: `systemctl start zigbee2mqtt`
- The `-last` option requires internet connection to download firmware from GitHub
