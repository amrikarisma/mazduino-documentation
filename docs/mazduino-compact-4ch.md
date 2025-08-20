# Mazduino Compact ECU

## Overview

The Mazduino Compact ECU is a 4-channel standalone engine control unit designed for versatile engine management applications. Made specifically for rusEFI and Speeduino firmware, it provides comprehensive engine control in a compact package suitable for 4-cylinder full sequential or 8-cylinder paired operation.

![Mazduino Compact 4ch](img/mazduino-compact-4ch.jpg)

## Key Features

### Engine Control Capabilities
- **4 Channel Operation**: 4 injectors and 4 ignition outputs
- **Flexible Configuration**: 4-cylinder full sequential or 8-cylinder paired
- **Sequential Control**: Full sequential fuel injection and ignition control
- **Idle Control**: PWM/IACV idle air control valve support
- **Air Conditioning**: Integrated AC control system

### Advanced Engine Management
- **Launch Control**: Advanced launch control system
- **Boost Control**: Turbo/supercharger boost management
- **Anti-Lag System (ALS)**: Turbo anti-lag functionality
- **Flat Shift**: Seamless gear changes without lift
- **Rev Limiter**: Both hard and soft cut options
- **Closed-loop Lambda Control**: O2 feedback for precise fuel control

## Technical Specifications

### Engine Control Outputs
- **Injection Channels**: 4 high-current injector outputs
- **Ignition Channels**: 4 ignition outputs
- **Idle Control**: 1 PWM/IACV output
- **Low Current Outputs**: Tachometer, fuel pump, fan, AC compressor

### Sensor Inputs
- **Engine Position**: CKP/CMP hall or optical sensor input
- **Engine Sensors**: O2, MAP, IAT, TPS, coolant temperature
- **Vehicle Inputs**: Clutch, AC switch/blower, VSS/speedometer
- **Additional**: Multiple analog and digital sensor inputs

### Communication & Data Logging
- **SD Card**: Onboard data logging capability
- **CANbus**: Communication support for external devices
- **Tuning Interface**: Full tuning via TunerStudio software

### Connectivity Options
Two connector configurations available:
- **Option 1**: 30-pin Molex Micro-Fit 3.0 (6-pin + 24-pin)
- **Option 2**: 33-pin Automotive Connector

## Firmware Compatibility

### rusEFI
- **Native Support**: Designed specifically for rusEFI firmware
- **Full Feature Set**: Complete access to all rusEFI capabilities
- **Real-time Tuning**: TunerStudio integration for live tuning
- **Advanced Features**: Launch control, boost control, ALS, and more

### Speeduino
- **Compatible**: Fully compatible with Speeduino firmware
- **Custom Configuration**: Mazduino-specific pin mapping available
- **Performance Optimized**: Optimized for reliable operation
- **Community Support**: Active community and documentation

## Supported Engine Configurations

### 4-Cylinder Engines
- **Full Sequential**: Individual cylinder control for maximum performance
- **Naturally Aspirated**: Complete engine management for NA engines
- **Forced Induction**: Turbo and supercharger support with boost control

### 8-Cylinder Engines
- **Paired Operation**: 8-cylinder support using paired injection/ignition
- **Wasted Spark**: Efficient ignition control for V8 applications
- **Performance Tuning**: Advanced tuning capabilities for high-performance V8s

### Universal Applications
- **Engine Swaps**: Modern control for classic vehicle conversions
- **Racing**: Professional motorsport applications
- **Custom Builds**: Flexible configuration for unique projects

## Advanced Features

### Performance Control Systems
- **Launch Control**: Configurable launch RPM and timing control
- **Boost Control**: Closed-loop wastegate and boost control
- **Anti-Lag System (ALS)**: Turbo anti-lag for improved response
- **Flat Shift**: No-lift shifting for seamless gear changes
- **Rev Limiter**: Soft cut (fuel) and hard cut (ignition) options

### Fuel & Ignition Management
- **Sequential Injection**: Individual cylinder fuel control
- **Closed-loop Lambda**: O2 sensor feedback for precise AFR control
- **Ignition Control**: Advanced timing control with knock protection
- **Fuel Pump Control**: Variable speed fuel pump management

### Data Logging & Communication
- **SD Card Logging**: High-speed onboard data recording
- **CANbus Support**: Integration with dashboard and other ECUs
- **TunerStudio**: Full-featured tuning software compatibility
- **Real-time Data**: Live monitoring and adjustment capabilities

## Applications

### Ideal Use Cases
- **4-Cylinder Builds**: Complete sequential control for 4-cyl engines
- **V8 Conversions**: Paired operation for V8 engine swaps
- **Turbo Applications**: Advanced boost and anti-lag control
- **Racing**: Professional motorsport engine management
- **Street Performance**: Enhanced control for modified street cars

### Installation Flexibility
- **Connector Options**: Choice of Molex or automotive connectors
- **Compact Design**: Space-efficient installation
- **Professional Grade**: Reliable operation in demanding environments

## Wiring and Installation

### Connector Pin Mapping

The Mazduino Compact ECU uses a 30-pin connector with the following pin assignments:

![Mazduino Compact 30-pin Connector](img/compact-30p-connector.jpg)

#### Connector Layout
```
 1   2   3       7   8   9  10  11  12  13  14  15  16  17  18
 4   5   6      19  20  21  22  23  24  25  26  27  28  29  30
```

#### Pin Assignments

| Pin | Function | Description |
|-----|----------|-------------|
| 1 | Clutch | Clutch position input |
| 2 | AC Switch | AC switch/digital input |
| 3 | CANH/Spare Analog 1 | CAN High or spare analog input (solder jumper) |
| 4 | VSS | Vehicle speed sensor |
| 5 | GND | Ground |
| 6 | CANL/Main Relay | CAN Low or main relay (solder jumper) |
| 7 | 12V | Main power supply |
| 8 | 5V | 5V reference output |
| 9 | Fan | Fan relay control |
| 10 | Tacho | Tachometer output |
| 11 | Idle PWM | Idle air control PWM |
| 12 | Injector 4 | Injector channel 4 |
| 13 | Injector 3 | Injector channel 3 |
| 14 | Injector 2 | Injector channel 2 |
| 15 | Injector 1 | Injector channel 1 |
| 16 | CMP | Camshaft position sensor |
| 17 | TPS | Throttle position sensor |
| 18 | MAP | Manifold absolute pressure |
| 19 | GND | Ground |
| 20 | GND | Ground |
| 21 | AC Compressor | AC compressor relay |
| 22 | Fuel Pump | Fuel pump relay |
| 23 | Ignition 1 | Ignition channel 1 |
| 24 | Ignition 2 | Ignition channel 2 |
| 25 | Ignition 3 | Ignition channel 3 |
| 26 | Ignition 4 | Ignition channel 4 |
| 27 | CKP | Crankshaft position sensor |
| 28 | IAT | Intake air temperature |
| 29 | CLT | Coolant temperature |
| 30 | O2 | Oxygen sensor |

### MCU Pin Mapping

For advanced users and firmware development, here are the STM32F407VGT6 pin assignments:

| Function | MCU Pin |
|----------|---------|
| Ignition Output 1 | PE15 |
| Ignition Output 2 | PE14 |
| Ignition Output 3 | PD13 |
| Ignition Output 4 | PE5 |
| Injection Output 1 | PD8 |
| Injection Output 2 | PB15 |
| Injection Output 3 | PB14 |
| Injection Output 4 | PB13 |
| MAP Sensor | PA0 |
| TPS | PA3 |
| IAT Sensor | PA5 |
| CLT Sensor | PA4 |
| O2 Sensor | PA1 |
| Battery/Voltage Ref | PA2 |
| Analog Spare Input 1 | PB1 |
| AC Input | PB0 |
| Clutch Input | PE13 |
| VSS | PD7 |
| CKP | PD3 |
| CMP | PD4 |
| Tacho | PC9 |
| Fuel Pump Relay | PC8 |
| FAN Relay | PA15 |
| AC Compressor Relay | PC7 |
| Main Relay | PE8 |
| Idle 1 | PD9 |
| TXD1 | PA9 |
| RXD1 | PA10 |
| TXD3 | PB10 |
| RXD3 | PB11 |
| TXCAN | PD1 |
| RXCAN | PD0 |
| SD CS | PD2 |
| SPI3 CLK | PC10 |
| SPI3 MISO | PC11 |
| SPI3 MOSI | PC12 |

### Solder Jumpers

The PCB includes solder jumpers on the back for configuration:
- **Pin 3**: CANH or Spare Analog Input 1
- **Pin 6**: CANL or Main Relay Control
- **Ignition voltage selection**: Choose appropriate voltage for ignition coils

### Installation Steps
1. **Mounting**: Secure ECU in suitable location
2. **Power Connection**: Connect main power (pin 7) and ground (pins 5, 19, 20)
3. **Sensor Wiring**: Connect engine sensors per pin mapping above
4. **Actuator Wiring**: Wire injectors and ignition coils to respective pins
5. **Verification**: Check all connections before power-up

### Wiring Notes
- **Sensor Ground**: Use pins 19 and 20 for sensor ground connections
- **5V Reference**: Pin 8 provides 5V reference for sensors
- **CAN Configuration**: Use solder jumpers to select CAN or relay functions (pins 3 & 6)
- **Wiring Compatibility**: Wiring is compatible with Speeduino standards
- **Reference**: Additional wiring information available at [Speeduino Wiki](https://wiki.speeduino.com/en/wiring/system)

## Tuning and Configuration

### Base Maps
- **Generic 4-cylinder**: Starting point for most engines
- **Motorcycle**: Optimized for bike applications
- **Turbo/Supercharged**: Forced induction starting maps

### Tuning Process
1. **Engine Configuration**: Set basic engine parameters
2. **Sensor Calibration**: Calibrate all input sensors
3. **Base Timing**: Set initial ignition timing
4. **Fuel Maps**: Configure injection timing and duration
5. **Fine Tuning**: Optimize for performance and emissions

## Support and Resources

### Documentation
- Installation guide - Complete setup instructions
- Wiring diagrams - Detailed connector pin assignments (see above)
- Tuning guide - Engine configuration and optimization
- Troubleshooting - Common issues and solutions

### Firmware & Configuration Files
- [Download Page](downloads.md) - Get the latest firmware and TunerStudio configuration files
- rusEFI and Speeduino firmware available
- Custom pin mapping configuration files included

### Community Support
- User forums and discussion groups
- Technical support channels
- Firmware updates and releases
- Community-contributed configurations

## Ordering Information

The Mazduino Compact ECU is available with two connector options and multiple purchase variants to suit different installation requirements:

### Connector Options
- **Option 1**: 30-pin Molex Micro-Fit 3.0 (6-pin + 24-pin configuration)
- **Option 2**: 33-pin Automotive Connector

### Purchase Variants

#### PCB Only
- Mazduino Compact ECU bare PCB
- For experienced builders who source their own components

#### PCB + Components
- Mazduino Compact ECU PCB
- All electronic components included
- Self-assembly required

#### Full Assembly (Ready to Use)
- Mazduino Compact ECU fully assembled and tested
- 1 pair of connectors (male/female) included
- 3D printed ABS case included
- USB programming cable
- SD card for data logging
- Quick start guide
- Access to TunerStudio software and base maps

**Note**: Wiring harnesses are sold separately and can be customized based on your specific application requirements.

Contact your local Mazduino distributor or visit our website for current pricing and availability.
