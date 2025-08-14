# ZMK Config for Cipther Keyboard

This repository contains the ZMK configuration for the Cipther keyboard, based on the Bastard KB Skeletyl layout.

## Keyboard Layout

The Cipther uses a 36-key split ergonomic layout with:
- 3x5 main key matrix per side
- 3 thumb keys per side
- Split design with wireless connectivity

## Layout Matrix

The keyboard follows the Bastard KB Skeletyl matrix configuration:

```
┌─────┬─────┬─────┬─────┬─────┐   ┌─────┬─────┬─────┬─────┬─────┐
│  Q  │  W  │  E  │  R  │  T  │   │  Y  │  U  │  I  │  O  │  P  │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│  A  │  S  │  D  │  F  │  G  │   │  H  │  J  │  K  │  L  │  ;  │
├─────┼─────┼─────┼─────┼─────┤   ├─────┼─────┼─────┼─────┼─────┤
│  Z  │  X  │  C  │  V  │  B  │   │  N  │  M  │  ,  │  .  │  /  │
└─────┴─────┴─────┼─────┼─────┼─────┼─────┼─────┼─────┴─────┴─────┘
                  │ GUI │ LWR │ SPC │ ENT │ RSE │ ALT │
                  └─────┴─────┴─────┴─────┴─────┴─────┘
```

## Layers

### Default Layer (0)
Standard QWERTY layout with home row positioning optimized for the Skeletyl form factor.

### Lower Layer (1)
- Numbers 1-0 on top row
- Bluetooth controls on home row
- Arrow keys on right side

### Raise Layer (2)
- Symbols and special characters
- Brackets and operators
- Function keys

## Building Firmware

The firmware is automatically built using GitHub Actions when you push changes to this repository. The built firmware files will be available as artifacts in the Actions tab.

## Hardware Requirements

- Nice!Nano v2 controllers (2x)
- Bastard KB Skeletyl PCBs or compatible handwired build
- 36 mechanical switches
- 36 1N4148 diodes
- Battery for wireless operation

## Pin Configuration

The configuration uses the following pin assignments compatible with the Skeletyl matrix:

**Rows (both halves):**
- Row 0: Pin 21
- Row 1: Pin 18  
- Row 2: Pin 5
- Row 3: Pin 4

**Columns:**
- Left half: Pins 19, 20, 10, 6, 7
- Right half: Pins 7, 6, 10, 20, 19 (reversed)

## Customization

To customize the keymap:
1. Edit `config/cipther.keymap`
2. Modify layer definitions as needed
3. Push changes to trigger new build

For hardware modifications:
1. Update pin assignments in overlay files
2. Modify matrix transform if changing physical layout
3. Update configuration files as needed

## Flashing

1. Download firmware files from GitHub Actions artifacts
2. Put controller into bootloader mode (double-tap reset)
3. Copy appropriate `.uf2` file to the mounted drive
4. Repeat for second half of split keyboard

## Support

For ZMK-specific issues, refer to the [ZMK Documentation](https://zmk.dev/).
For hardware-related questions about the Skeletyl, check the [Bastard KB community](https://discord.gg/bastardkb).