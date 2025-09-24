# Unduhan

Halaman ini menyediakan file firmware dan file konfigurasi untuk kedua model ECU Mazduino. Pilih firmware dan file konfigurasi yang sesuai berdasarkan model ECU Anda dan software manajemen mesin yang diinginkan.

## Mazduino Compact ECU

### Firmware rusEFI
rusEFI adalah firmware utama untuk Mazduino Compact ECU dengan dukungan fitur lengkap.

#### Download Firmware
- **GitHub Actions**: [https://github.com/amrikarisma/fw-custom-mazduino/actions](https://github.com/amrikarisma/fw-custom-mazduino/actions)
- Pilih build terbaru yang berhasil (status hijau ✓)
- **Pilihan Download**:
    - **File .hex**: Firmware format Intel Hex (untuk programmer)
    - **File .bin**: Firmware format binary (untuk DFU/ST-Link)
    - **Bundle (.zip ~40MB)**: **REKOMENDASI** - Paket lengkap termasuk firmware, driver, dan file .ini untuk TunerStudio

#### File Konfigurasi
- **TunerStudio INI**: Sudah termasuk dalam bundle (selalu update otomatis)

### Firmware Speeduino
Firmware Speeduino khusus yang dikonfigurasi secara spesifik untuk pin mapping Mazduino Compact ECU.

#### File Firmware
- **Format Binary**: [firmware.bin](myfiles/speeduino/mazduino_compact/firmware.bin)

#### File Konfigurasi
- **TunerStudio INI**: [speeduino.ini](myfiles/speeduino/mazduino_compact/speeduino.ini)

---

## Mazduino Mini 6CH

### Firmware rusEFI
Firmware rusEFI dengan dukungan 6-channel penuh dan fitur-fitur canggih.

#### Download Firmware
- **GitHub Actions**: [https://github.com/amrikarisma/fw-custom-mazduino/actions](https://github.com/amrikarisma/fw-custom-mazduino/actions)
- Pilih build terbaru yang berhasil (status hijau ✓)
- **Pilihan Download**:
    - **File .hex**: Firmware format Intel Hex (untuk programmer)
    - **File .bin**: Firmware format binary (untuk DFU/ST-Link)
    - **Bundle (.zip ~40MB)**: **REKOMENDASI** - Paket lengkap termasuk firmware, driver, dan file .ini untuk TunerStudio

#### File Konfigurasi
- **TunerStudio INI**: Sudah termasuk dalam bundle (selalu update otomatis)

**Catatan**: Firmware Speeduino untuk Mazduino Mini 6CH saat ini tidak dilanjutkan. Hanya mendukung firmware rusEFI saja.

---

## Petunjuk Instalasi

### Instalasi rusEFI

**Opsi 1: Bundle (REKOMENDASI)**

1. **Unduh Bundle**: Kunjungi [GitHub Actions](https://github.com/amrikarisma/fw-custom-mazduino/actions)
2. **Pilih Build**: Pilih workflow run terbaru dengan status berhasil (✓)
3. **Download Bundle**: Pilih bundle (.zip ~40MB) yang berisi firmware, driver, dan file .ini terbaru
4. **Extract**: Extract file .zip ke folder kerja Anda
5. **Flash Firmware**: Pilih metode flashing di bawah
6. **Konfigurasi TunerStudio**: Muat file .ini yang sudah disertakan dalam bundle

#### Metode Flashing Firmware

**A. STM32CubeProgrammer + ST-Link (REKOMENDASI untuk instalasi pertama kali)**

1. **Install STM32CubeProgrammer**: Download dari [website ST](https://www.st.com/en/development-tools/stm32cubeprog.html)
2. **Koneksi Hardware**: Hubungkan ST-Link ke Mazduino ECU via SWD (4-pin)
3. **Buka STM32CubeProgrammer**: Pilih ST-Link sebagai interface
4. **Connect**: Klik Connect untuk terhubung ke MCU
5. **Load File**: Browse dan pilih file .hex atau .bin dari bundle
6. **Program**: Klik "Download" untuk flash firmware

**B. rusEFI Console (Untuk update firmware)**

- Gunakan setelah firmware pertama kali sudah ter-install
- Mendukung flashing via USB

**C. DFU Mode (USB)**

- Untuk ECU yang sudah memiliki bootloader
- Tidak memerlukan programmer eksternal

**Opsi 2: Download Individual (Hanya untuk jika hanya perlu file tertentu)**


### Instalasi Speeduino (Hanya Compact)

1. **Unduh Firmware**: Unduh file `firmware.bin`
2. **Unduh Konfigurasi**: Unduh file `speeduino.ini`
3. **Flash Firmware**: Gunakan Arduino IDE atau programmer ST-Link
4. **Konfigurasi TunerStudio**: Muat file INI di TunerStudio
5. **Pin Mapping**: Verifikasi pin assignment sesuai dengan layout Mazduino Compact

---

## Kebutuhan Software

### TunerStudio
Unduh versi terbaru TunerStudio dari:

- **Website Resmi**: [tunerstudio.com](https://www.tunerstudio.com/index.php/downloads)
- **Versi yang Disarankan**: TunerStudio MS Ultra atau lebih tinggi

### Tool Programming

#### Untuk rusEFI:
- **STM32CubeProgrammer**: **REKOMENDASI** untuk instalasi firmware pertama kali dengan ST-Link
- **rusEFI Console**: Tersedia dari [website rusEFI](https://rusefi.com)
- **ST-Link Utility**: Untuk programming STM32 secara langsung (legacy)
- **DFU Programmer**: Untuk flashing mode USB DFU

#### Hardware Programming:
- **ST-Link V2/V3**: Programmer hardware untuk koneksi SWD ke Mazduino ECU
- **Kabel SWD**: 4-pin connector (VCC, GND, SWDIO, SWCLK)

#### Untuk Speeduino:
- **Arduino IDE**: Dengan paket dukungan STM32
- **Programmer ST-Link**: Programmer hardware
- **platformio**: Environment pengembangan alternatif

---

## Catatan Penting

### Kompatibilitas Firmware
- **rusEFI**: Kompatibel dengan Mazduino Compact dan Mini 6CH
- **Speeduino**: Saat ini hanya tersedia untuk Mazduino Compact
- **Kompatibilitas Versi**: Selalu gunakan firmware dan file INI yang sesuai

### Pin Mapping
- **Khusus Mazduino**: File-file ini berisi pin mapping khusus untuk ECU Mazduino
- **Tidak Dapat Ditukar**: Jangan gunakan dengan board ECU lain
- **Verifikasi Diperlukan**: Selalu verifikasi pin assignment sebelum menghubungkan hardware

### Kompatibilitas File .ini
- **Gunakan Bundle**: **PENTING** - Selalu gunakan bundle untuk memastikan file .ini cocok dengan firmware
- **Hindari File Terpisah**: File .ini yang didownload terpisah mungkin tidak kompatibel dengan firmware terbaru
- **Auto Update**: Bundle selalu berisi file .ini yang sudah ditest dengan firmware yang sama

### Sumber Dukungan
- **rusEFI Wiki**: [wiki.rusefi.com](https://wiki.rusefi.com)
- **Speeduino Wiki**: [wiki.speeduino.com](https://wiki.speeduino.com)
- **Dokumentasi Mazduino**: Situs dokumentasi ini
- **Dukungan Komunitas**: Forum pengguna dan grup diskusi

---

## Pemecahan Masalah

### Masalah Umum
1. **Masalah Komunikasi**: Verifikasi driver USB dan pengaturan port
2. **Kegagalan Flash**: Pastikan programmer dan koneksi yang benar
3. **Error Pin Mapping**: Periksa kembali pemuatan file INI
4. **Masalah Pembacaan Sensor**: Verifikasi wiring terhadap tabel pin mapping

### Mendapatkan Bantuan
- Tinjau dokumentasi untuk model ECU spesifik Anda untuk panduan pemecahan masalah
- Periksa forum komunitas untuk masalah serupa
- Hubungi dukungan teknis untuk masalah terkait hardware

---

**Peringatan**: Selalu verifikasi kompatibilitas firmware dengan model ECU Mazduino spesifik Anda sebelum flashing. Firmware yang salah dapat merusak ECU Anda atau menyebabkan operasi mesin yang tidak aman.