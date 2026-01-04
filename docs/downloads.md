# Downloads - Firmware dan Konfigurasi ECU Mazduino

Halaman ini menyediakan firmware dan file konfigurasi untuk semua model ECU Mazduino. Pilih firmware yang sesuai berdasarkan model ECU Anda dan software manajemen mesin yang diinginkan.

## Firmware Downloads

### rusEFI Firmware

#### Official rusEFI Firmware
Gunakan build resmi dari rusEFI untuk kompatibilitas standar:

- **mega100-F4** atau **F407 Discovery** builds dari [rusEFI Build Server](https://rusefi.com/build_server/)
- **Catatan**: Pin mapping mungkin perlu disesuaikan manual untuk ECU Mazduino

#### Custom Mazduino Firmware
Firmware rusEFI yang dioptimalkan khusus untuk semua board Mazduino:

- **Download**: [Mazduino Custom Firmware](https://github.com/amrikarisma/fw-custom-mazduino/actions/workflows/build-firmware.yaml)
- **Pilih build terbaru** dengan status berhasil
- **Format tersedia**:
  - **Bundle (.zip ~40MB)**: **REKOMENDASI** - Firmware + driver + file .ini TunerStudio
  - **File .hex**: Firmware format Intel Hex (untuk programmer)
  - **File .bin**: Firmware format binary (untuk DFU/ST-Link)

#### Keuntungan Custom Firmware:
- Pin mapping pre-configured untuk semua versi Mazduino
- File .ini included dengan konfigurasi yang sudah ditest
- Driver support untuk Windows/Linux/macOS
- Auto-update compatibility antara firmware dan TunerStudio config

### Speeduino Firmware

#### Custom Speeduino untuk Mazduino
- **Download**: [Speeduino Custom Releases](https://github.com/amrikarisma/speeduino-custom/releases)
- **PENTING**: Mazduino ECU **TIDAK MENDUKUNG** official Speeduino firmware
- **Kompatibilitas**: Mazduino Compact dan Mini 6CH v1.3

#### Catatan Speeduino:
- **Official Speeduino**: Tidak kompatibel dengan Mazduino
- **Custom version only**: Pin mapping khusus untuk Mazduino
- **Mini 6CH v1.0-v1.2**: Tidak didukung, gunakan rusEFI saja

## Compatibility Matrix

| ECU Model | rusEFI Official | rusEFI Custom | Speeduino Custom |
|-----------|----------------|---------------|------------------|
| **Compact v1** | Manual config | Ready to use | Supported |
| **Compact v2.1** | Manual config | Ready to use | Supported |
| **Compact v2.2** | Manual config | Ready to use | Supported |
| **Mini 6CH v1.0-v1.2** | Manual config | Ready to use | Not supported |
| **Mini 6CH v1.3** | Manual config | Ready to use | Supported |

---

## Petunjuk Instalasi

### Instalasi rusEFI Custom (REKOMENDASI)

#### Langkah 1: Download Bundle

1. **Kunjungi**: [GitHub Actions](https://github.com/amrikarisma/fw-custom-mazduino/actions/workflows/build-firmware.yaml)
2. **Pilih build terbaru** dengan status berhasil
3. **Download Bundle**: Pilih file .zip (~40MB) 
4. **Extract**: Extract ke folder kerja Anda

#### Langkah 2: Flash Firmware

**A. STM32CubeProgrammer + ST-Link (REKOMENDASI untuk first-time install)**

1. **Install STM32CubeProgrammer**: Download dari [ST website](https://www.st.com/en/development-tools/stm32cubeprog.html)
2. **Connect Hardware**: Hubungkan ST-Link ke ECU via SWD (4-pin)
3. **Open STM32CubeProgrammer**: Pilih ST-Link sebagai interface
4. **Connect**: Klik Connect ke MCU
5. **Load File**: Browse file .hex/.bin dari bundle
6. **Program**: Klik "Download" untuk flash

**B. DFU Mode (USB) - untuk ECU yang sudah ada bootloader**

1. **Set DFU Mode**: Tekan tombol Boot + Reset pada ECU
2. **Connect USB**: Hubungkan ECU ke PC via USB
3. **Flash via DFU**: Gunakan STM32CubeProgrammer atau DFU tools

**C. rusEFI Console (untuk firmware updates)**

1. **Install rusEFI Console**: Download dari [rusefi.com](https://rusefi.com)
2. **Connect ECU**: Via USB setelah firmware pertama ter-install
3. **Update**: Gunakan built-in firmware update feature

#### Langkah 3: Konfigurasi TunerStudio

1. **Install TunerStudio**: Download dari [tunerstudio.com](https://www.tunerstudio.com)
2. **Load .ini file**: Gunakan file .ini yang included dalam bundle
3. **Connect**: Hubungkan ke ECU via USB
4. **Base tune**: Load base map sesuai aplikasi mesin Anda

### Instalasi Speeduino Custom

#### Download dan Install

1. **Download**: [Speeduino Custom Releases](https://github.com/amrikarisma/speeduino-custom/releases)
2. **Flash**: Gunakan STM32CubeProgrammer atau Arduino IDE
3. **TunerStudio**: Load file .ini yang disertakan
4. **Pin Mapping**: Verifikasi sesuai dengan ECU Mazduino yang didukung

---

## Kebutuhan Software & Hardware

### Software Requirements
- **TunerStudio MS**: [tunerstudio.com](https://www.tunerstudio.com) - Ultra version recommended
- **STM32CubeProgrammer**: [ST website](https://www.st.com/en/development-tools/stm32cubeprog.html) - for firmware flashing
- **rusEFI Console**: [rusefi.com](https://rusefi.com) - for rusEFI management
- **USB Drivers**: Included in firmware bundle

### Hardware Requirements  
- **ST-Link V2/V3**: Hardware programmer untuk SWD connection
- **USB Cable**: Type-C untuk komunikasi dengan ECU
- **SWD Cable**: 4-pin (VCC, GND, SWDIO, SWCLK) untuk programming

---

## Catatan Penting & Best Practices

### Critical Notes
- **Official vs Custom**: Official rusEFI memerlukan manual pin configuration
- **Speeduino Official**: TIDAK kompatibel dengan Mazduino - hanya gunakan custom version
- **Bundle Priority**: Selalu gunakan bundle untuk memastikan firmware + .ini compatibility
- **Hardware Specific**: Firmware ini khusus untuk Mazduino - jangan gunakan di ECU lain

### Best Practices
1. **Always backup**: Backup konfigurasi sebelum update firmware
2. **Use Bundle**: Download bundle lengkap untuk compatibility terjamin
3. **Verify Hardware**: Pastikan model ECU sesuai dengan firmware
4. **Test Safe**: Test di bench sebelum install di kendaraan
5. **Documentation**: Baca dokumentasi hardware spesifik ECU Anda

### Troubleshooting
- **Connection Issues**: Periksa USB drivers dan port settings  
- **Flash Failures**: Pastikan programmer dan connection yang benar
- **Pin Mapping Errors**: Gunakan file .ini dari bundle yang sama
- **Sensor Reading**: Verifikasi wiring sesuai pin mapping dokumentasi

### Support Resources
- **Mazduino Wiki**: [github.com/amrikarisma/Mazduino/wiki](https://github.com/amrikarisma/Mazduino/wiki)
- **rusEFI Wiki**: [wiki.rusefi.com](https://wiki.rusefi.com)
- **Speeduino Wiki**: [wiki.speeduino.com](https://wiki.speeduino.com)
- **TunerStudio Manual**: Tersedia di dokumentasi ini

---

**SAFETY WARNING**: Selalu verifikasi kompatibilitas firmware dengan model ECU Mazduino spesifik Anda sebelum flashing. Firmware yang salah dapat merusak ECU atau menyebabkan operasi mesin yang tidak aman. Test selalu di bench terlebih dahulu sebelum instalasi final.