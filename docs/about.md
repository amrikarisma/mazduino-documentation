# About Mazduino ECU

## Overview

Mazduino ECU is a standalone Engine Control Unit (ECU) designed for automotive enthusiasts and professionals who need a flexible, open-source solution for engine management. Built around the powerful STM32F407VGT6 microcontroller, Mazduino offers exceptional performance and expandability for various engine control applications.

## Key Features

### Hardware Platform
- **Primary MCU**: STM32F407VGT6 (ARM Cortex-M4 @ 168MHz)
- **Future Compatibility**: Planned support for multiple STM32 variants
- **Open Hardware Design**: Fully documented schematics and PCB layouts
- **Robust Construction**: Automotive-grade components and connectors

### Firmware Options

#### rusEFI Firmware
Mazduino ECU primarily runs on **rusEFI**, a comprehensive open-source engine management firmware that provides:

- Advanced fuel injection control
- Ignition timing management
- Sensor data acquisition and processing
- Real-time tuning capabilities
- Extensive logging and diagnostics
- CAN bus communication
- Support for various engine configurations

#### Speeduino Compatibility
Due to the STM32F407VGT6 MCU, Mazduino is also compatible with **Speeduino firmware**. However, please note:

- **Custom firmware required** due to different pin mapping
- Pin assignments differ from popular and official Speeduino boards
- Community support available for custom configurations
- Full documentation provided for pin mapping differences

## Target Applications

Mazduino ECU is designed for:

- **Standalone Engine Management**: Complete replacement for factory ECUs
- **Racing Applications**: High-performance motorsport environments
- **Engine Swaps**: Modern engine management for classic vehicles
- **Research & Development**: Educational and experimental projects
- **Aftermarket Tuning**: Enhanced control for modified engines

## Open Source Philosophy

Mazduino embraces the open-source community by providing:

- **Open Hardware**: Complete schematics, PCB files, and BOM
- **Open Firmware**: Based on established open-source projects
- **Community Driven**: Collaborative development and support
- **Educational Resources**: Comprehensive documentation and tutorials
- **Customization Freedom**: Full access to modify and adapt

## Future Development

The Mazduino project continues to evolve with planned enhancements:

- **Multi-MCU Support**: Expanding to various STM32 family members
- **Enhanced I/O**: Additional sensor and actuator interfaces
- **Wireless Connectivity**: WiFi and Bluetooth integration options
- **Advanced Features**: Knock detection, flex fuel, and more
- **Community Contributions**: User-submitted improvements and variants

## Getting Started

Whether you're a seasoned tuner or new to standalone engine management, Mazduino provides the tools and documentation needed to successfully implement modern engine control in your project. Our comprehensive documentation covers everything from basic installation to advanced tuning strategies.

Join the Mazduino community and take control of your engine management with this powerful, flexible, and open-source ECU solution.