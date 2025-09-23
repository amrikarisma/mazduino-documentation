# Unduhan

Halaman ini menyediakan file firmware dan file konfigurasi untuk kedua model ECU Mazduino. Pilih firmware dan file konfigurasi yang sesuai berdasarkan model ECU Anda dan software manajemen mesin yang diinginkan.

## Mazduino Compact ECU

### Firmware rusEFI
rusEFI adalah firmware utama untuk Mazduino Compact ECU dengan dukungan fitur lengkap.

#### File Firmware
- **Format Binary**: [rusefi.bin](myfiles/rusefi/rusefi.bin)
- **Format Intel Hex**: [rusefi.hex](myfiles/rusefi/rusefi.hex)

#### File Konfigurasi
- **TunerStudio INI**: [rusefi_mazduino.ini](myfiles/rusefi/rusefi_mazduino.ini)

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

#### File Firmware
- **Format Binary**: [rusefi.bin](myfiles/rusefi/rusefi.bin)
- **Format Intel Hex**: [rusefi.hex](myfiles/rusefi/rusefi.hex)

#### File Konfigurasi
- **TunerStudio INI**: [rusefi_mazduino.ini](myfiles/rusefi/rusefi_mazduino.ini)

**Catatan**: Firmware Speeduino untuk Mazduino Mini 6CH saat ini sedang dalam pengembangan.

---

## Petunjuk Instalasi

### Instalasi rusEFI

1. **Unduh Firmware**: Pilih format `.bin` atau `.hex`
2. **Unduh Konfigurasi**: Unduh file `rusefi_mazduino.ini`
3. **Flash Firmware**: Gunakan ST-Link, mode DFU, atau rusEFI Console
4. **Konfigurasi TunerStudio**: Muat file INI di TunerStudio
5. **Setup Awal**: Konfigurasi parameter dasar mesin

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
- **rusEFI Console**: Tersedia dari [website rusEFI](https://rusefi.com)
- **ST-Link Utility**: Untuk programming STM32 secara langsung
- **DFU Programmer**: Untuk flashing mode USB DFU

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

### Sumber Dukungan
- **rusEFI Wiki**: [wiki.rusefi.com](https://wiki.rusefi.com)
- **Speeduino Wiki**: [wiki.speeduino.com](https://wiki.speeduino.com)
- **Dokumentasi Mazduino**: Situs dokumentasi ini
- **Dukungan Komunitas**: Forum pengguna dan grup diskusi

---

## Riwayat Versi

### Update Terbaru
- **rusEFI**: Rilis stabil terbaru dengan dukungan Mazduino
- **Speeduino Compact**: Build khusus dengan pin mapping Mazduino
- **File Konfigurasi**: Diperbarui untuk versi firmware terbaru

### Changelog
Periksa repositori firmware individual untuk informasi changelog detail:
- rusEFI: Repositori GitHub resmi rusEFI
- Speeduino: Repositori GitHub resmi Speeduino

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