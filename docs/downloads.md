# Downloads

This page provides firmware files and configuration files for both Mazduino ECU models. Choose the appropriate firmware and configuration files based on your ECU model and preferred engine management software.

## Mazduino Compact ECU

### rusEFI Firmware
rusEFI is the primary firmware for Mazduino Compact ECU with full feature support.

#### Firmware Files
- **Binary Format**: [rusefi.bin](files/rusefi/rusefi.bin)
- **Intel Hex Format**: [rusefi.hex](files/rusefi/rusefi.hex)

#### Configuration File
- **TunerStudio INI**: [rusefi_mazduino.ini](files/rusefi/rusefi_mazduino.ini)

### Speeduino Firmware
Custom Speeduino firmware specifically configured for Mazduino Compact ECU pin mapping.

#### Firmware Files
- **Binary Format**: [firmware.bin](files/speeduino/mazduino_compact/firmware.bin)

#### Configuration File
- **TunerStudio INI**: [speeduino.ini](files/speeduino/mazduino_compact/speeduino.ini)

---

## Mazduino Mini 6CH

### rusEFI Firmware
rusEFI firmware with full 6-channel support and advanced features.

#### Firmware Files
- **Binary Format**: [rusefi.bin](files/rusefi/rusefi.bin)
- **Intel Hex Format**: [rusefi.hex](files/rusefi/rusefi.hex)

#### Configuration File
- **TunerStudio INI**: [rusefi_mazduino.ini](files/rusefi/rusefi_mazduino.ini)

**Note**: Speeduino firmware for Mazduino Mini 6CH is currently in development.

---

## Installation Instructions

### rusEFI Installation

1. **Download Firmware**: Choose either `.bin` or `.hex` format
2. **Download Configuration**: Download the `rusefi_mazduino.ini` file
3. **Flash Firmware**: Use ST-Link, DFU mode, or rusEFI Console
4. **Configure TunerStudio**: Load the INI file in TunerStudio
5. **Initial Setup**: Configure basic engine parameters

### Speeduino Installation (Compact Only)

1. **Download Firmware**: Download `firmware.bin` file
2. **Download Configuration**: Download `speeduino.ini` file
3. **Flash Firmware**: Use Arduino IDE or ST-Link programmer
4. **Configure TunerStudio**: Load the INI file in TunerStudio
5. **Pin Mapping**: Verify pin assignments match Mazduino Compact layout

---

## Software Requirements

### TunerStudio
Download the latest version of TunerStudio from:
- **Official Website**: [tunerstudio.com](https://www.tunerstudio.com/index.php/downloads)
- **Recommended Version**: TunerStudio MS Ultra or higher

### Programming Tools

#### For rusEFI:
- **rusEFI Console**: Available from [rusEFI website](https://rusefi.com)
- **ST-Link Utility**: For direct STM32 programming
- **DFU Programmer**: For USB DFU mode flashing

#### For Speeduino:
- **Arduino IDE**: With STM32 support package
- **ST-Link Programmer**: Hardware programmer
- **platformio**: Alternative development environment

---

## Important Notes

### Firmware Compatibility
- **rusEFI**: Compatible with both Mazduino Compact and Mini 6CH
- **Speeduino**: Currently only available for Mazduino Compact
- **Version Compatibility**: Always use matching firmware and INI files

### Pin Mapping
- **Mazduino-Specific**: These files contain custom pin mappings for Mazduino ECUs
- **Not Interchangeable**: Do not use with other ECU boards
- **Verification Required**: Always verify pin assignments before connecting hardware

### Support Resources
- **rusEFI Wiki**: [wiki.rusefi.com](https://wiki.rusefi.com)
- **Speeduino Wiki**: [wiki.speeduino.com](https://wiki.speeduino.com)
- **Mazduino Documentation**: This documentation site
- **Community Support**: User forums and discussion groups

---

## Version History

### Latest Updates
- **rusEFI**: Latest stable release with Mazduino support
- **Speeduino Compact**: Custom build with Mazduino pin mapping
- **Configuration Files**: Updated for latest firmware versions

### Changelog
Check individual firmware repositories for detailed changelog information:
- rusEFI: Official rusEFI GitHub repository
- Speeduino: Official Speeduino GitHub repository

---

## Troubleshooting

### Common Issues
1. **Communication Problems**: Verify USB drivers and port settings
2. **Flash Failures**: Ensure correct programmer and connection
3. **Pin Mapping Errors**: Double-check INI file loading
4. **Sensor Reading Issues**: Verify wiring against pin mapping tables

### Getting Help
- Review the [troubleshooting guides](troubleshooting.md) for your specific ECU model
- Check community forums for similar issues
- Contact technical support for hardware-related problems

---

**Warning**: Always verify firmware compatibility with your specific Mazduino ECU model before flashing. Incorrect firmware can damage your ECU or cause unsafe engine operation.