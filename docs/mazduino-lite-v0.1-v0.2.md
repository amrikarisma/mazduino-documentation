# Mazduino LITE

## Pengantar

Mazduino LITE adalah varian terbaru dari keluarga ECU Mazduino yang dirancang khusus untuk aplikasi engine 4-silinder dengan 4 channel injector dan 2 channel ignition. LITE menawarkan solusi ECU yang compact namun tetap powerful dengan fitur-fitur modern seperti CAN Bus, USB Type-C, dan data logging SD card.

![Mazduino LITE ECU](img/lite/mazduino-lite-with-case.jpeg)

**Mazduino LITE tersedia dalam 2 versi: v0.1 dan v0.2** dengan perbaikan signifikan pada v0.2.

## Perbandingan Versi

### v0.1 vs v0.2

| Aspek | v0.1 | v0.2 |
|-------|------|------|
| **IGBT Footprint** | Footprint tidak umum (issue) | D2Pak to 263 (umum & mudah ditemukan) |
| **Rekomendasi Penggunaan** | Coil On Plug atau IGBT Eksternal | Internal IGBT atau semua aplikasi |
| **Barometer Internal** | Tidak tersedia | Optional (tidak terpasang default) |
| **Jalur PCB** | Standard | Perbaikan jalur & koreksi untuk jumper |
| **IGBT Internal** | Tidak disarankan (footprint issue) | Disarankan |

### Rekomendasi Penggunaan

**Mazduino LITE v0.1**: 

  - Ideal untuk **Coil On Plug** setup
  - Gunakan dengan **IGBT Eksternal** (tersedia di Toko Mazduino)
  - Tidak disarankan untuk IGBT internal karena footprint yang tidak umum

**Mazduino LITE v0.2**: 

  - **Pilihan utama** untuk semua aplikasi
  - **IGBT internal** dengan footprint D2Pak to 263 yang mudah ditemukan
  - **Barometer internal optional** (dapat diminta saat pembelian)
  - **Jalur PCB yang diperbaiki** untuk kemudahan jumper

![Mazduino LITE PCB](img/lite/mazduino-lite-open.jpeg)


## Fitur Utama

### Sistem Input
- **Trigger Input**: CKP dan CMP untuk Hall/Optical sensors
- **VR Support**: Variable Reluctance sensors dengan konditioner module
- **Analog Inputs**: 6x (0-5V) untuk MAP, TPS, IAT, CLT, O2, dan spare
- **Digital Inputs**: 5x pullup untuk AC Switch, VSS, Clutch, dan launch control
- **Sensor Power**: 5V regulated dengan internal fuse protection
- **Barometer Internal**: Tersedia pada v0.2 (optional, tidak terpasang default kecuali diminta)

### Sistem Output
- **Injection**: 4x high-current drivers untuk sequential atau batch mode
- **Ignition**: 2x outputs dengan Smart Coil (5V/12V) dan IGBT support
  - **v0.1**: IGBT footprint tidak umum (gunakan IGBT eksternal atau COP)
  - **v0.2**: IGBT footprint D2Pak to 263 yang umum dan mudah ditemukan
- **Control**: 5x relay outputs untuk fuel pump, fan, AC, main relay, tachometer
- **Idle Control**: 2x PWM outputs untuk ISC valve

### Komunikasi
- **USB Type-C**: Modern connector untuk tuning dan programming
- **CAN Bus**: 4-pin connector dengan power selection (5V/12V)
- **Serial**: RX/TX pins untuk additional communication

### Penyimpanan dan Timing
- **SD Card**: Micro SD untuk onboard data logging (max 32GB)
- **RTC**: Battery-backed real-time clock
- **Processor**: ARM Cortex-M4 STM32F4 series

## Sistem Konektor

### Konektor Utama 33-Pin

![Connector Layout](img/lite/mazduino-lite-connector-layout.jpeg)

#### Layout Konektor
```
11  10   9   8   7   6   5   4   3   2   1
22  21  20  19  18  17  16  15  14  13  12
33  32  31  30  29  28  27  26  25  24  23
```

#### Pin Assignment

| Pin | Fungsi | Deskripsi |
|-----|----------|-------------|
| 1 | Idle 1 | Output kontrol idle 1 |
| 2 | Idle 2 | Output kontrol idle 2 |
| 3 | CKP/Digital1 | Crankshaft position |
| 4 | VR1- | VR sensor negatif |
| 5 | Ignition 1 | Channel pengapian 1 |
| 6 | Main Relay | Kontrol relay utama |
| 7 | Ignition 2 | Channel pengapian 2 |
| 8 | Tacho/RPM | Output tachometer |
| 9 | Ground Coil | Ground untuk coil |
| 10 | +5V | Output referensi 5V |
| 11 | +12V | Catu daya utama |
| 12 | Injector 3 | Channel injektor 3 |
| 13 | Injector 4 | Channel injektor 4 |
| 14 | CMP/Digital2 | Camshaft position |
| 15 | VR2- | VR sensor negatif 2 |
| 16 | VR2+ | VR sensor positif 2 |
| 17 | AC Relay | Kontrol relay AC |
| 18 | Fuel Pump Relay | Kontrol pompa bahan bakar |
| 19 | Fan Relay | Kontrol relay kipas |
| 20 | IAT | Intake air temperature |
| 21 | TPS | Throttle position sensor |
| 22 | Ground ECU | Ground ECU |
| 23 | Injector 2 | Channel injektor 2 |
| 24 | Injector 1 | Channel injektor 1 |
| 25 | Ground Sensor | Ground sensor |
| 26 | Ground Sensor | Ground sensor |
| 27 | VR1+ | VR sensor positif 1 |
| 28 | MAP | Manifold absolute pressure |
| 29 | Clutch/Digital3 | Input posisi kopling |
| 30 | CLT | Coolant temperature |
| 31 | AC Switch Input | Input switch AC (Aktif Ground) |
| 32 | VSS/Digital4 | Vehicle speed sensor |
| 33 | O2 Sensor | Sensor oksigen |

### CAN Bus Konektor (4-Pin)

| Pin | Fungsi |
|-----|----------|
| 1 | Power (12V/5V selectable) |
| 2 | CAN Low |
| 3 | CAN High |
| 4 | Ground |

## Pin Mapping MCU

Untuk pengguna lanjutan dan pengembangan firmware:

| Fungsi | Pin MCU |
|----------|---------|
| Ignition Output 1 | PE15 |
| Ignition Output 2 | PE14 |
| Injection Output 1 | PD8 |
| Injection Output 2 | PB15 |
| Injection Output 3 | PB14 |
| Injection Output 4 | PB13 |
| MAP Sensor | PA0 |
| TPS | PA3 |
| IAT Sensor | PA5 |
| CLT Sensor | PA4 |
| O2 Sensor | PA1 |
| Battery/Voltage Reff | PA2 |
| Analog Spare Input 1 | PB1 |
| AC Input | PB0 |
| Clutch Input | PE13 |
| VSS | PD7 |
| CKP | PC6 |
| CMP | PE11 |
| VR1 | PD3 |
| VR2 | PD4 |
| Tacho | PC9 |
| Fuelpump Relay | PC8 |
| FAN Relay | PA15 |
| AC Compresor Relay | PC7 |
| Main Relay | PE8 |
| Idle 1 | PD9 |
| Idle 2 | PD10 |
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

## Konfigurasi Hardware

### Pengaturan Jumper Kritis

⚠️ **PENTING**: Konfigurasi jumper harus benar sebelum power-up!

#### Top Side Board
- **Coil Voltage**: 12V/5V selection (default berdasarkan coil type)
- **CAN Terminator**: Enable/disable resistor terminator
- **VR Conditioner**: 8-pin connector untuk VR module

#### Bottom Side Board
- **Tacho Signal**: 5V/12V output selection (default 12V)
- **IGN1/IGN2 Mode**: Smart Coil/IGBT selection (JP3/JP4)
  - **v0.1**: Gunakan Smart Coil atau IGBT eksternal (footprint IGBT tidak umum)
  - **v0.2**: IGBT internal dengan footprint D2Pak to 263 (umum & mudah ditemukan)
- **VR1/Hall, VR2/Hall**: Input type selection
- **Digital Pullup**: Enable internal pullup resistors
- **CAN Power**: 12V/5V pada CAN connector

#### Perbaikan pada v0.2
- **Jalur PCB**: Perbaikan routing dan koreksi jalur untuk kemudahan jumper
- **IGBT Compatibility**: Footprint yang lebih umum dan mudah ditemukan
- **Barometer Support**: Mounting untuk sensor barometer internal (optional)

### Peringatan Keselamatan

⚠️ **PERINGATAN**:
- **Jangan hubungkan sinyal 12V langsung ke ECU input**
- **Verifikasi coil voltage jumper sebelum koneksi**
- **Gunakan sensor ground terpisah dari power ground**
- **Check all jumper settings sebelum first power-up**

⚠️ **PERINGATAN KHUSUS VERSI**:
- **v0.1**: Hindari penggunaan IGBT internal karena footprint yang tidak umum
- **v0.1**: Gunakan IGBT eksternal atau setup Coil On Plug untuk reliability
- **v0.2**: IGBT internal aman digunakan dengan footprint D2Pak to 263
- **v0.2**: Barometer internal tersedia opsional (request saat pembelian)

## Kesimpulan

### Rekomendasi Pemilihan Versi

**Pilih v0.1 jika:**
- Menggunakan setup **Coil On Plug**
- Memiliki atau berencana menggunakan **IGBT Eksternal**
- Budget terbatas dan tidak membutuhkan IGBT internal

**Pilih v0.2 jika:**
- Membutuhkan **IGBT Internal** dengan komponen yang mudah ditemukan
- Memerlukan **Barometer Internal** (optional)
- Menginginkan **jalur PCB yang diperbaiki** untuk kemudahan instalasi
- **Direkomendasikan untuk pengguna baru** dan semua aplikasi umum

Mazduino LITE v0.2 direkomendasikan untuk kebanyakan aplikasi karena perbaikan IGBT footprint dan jalur PCB.

---

*Mazduino LITE - Compact Power untuk Modern Engine Management*