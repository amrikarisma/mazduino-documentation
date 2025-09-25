# Manual Tuning TunerStudio untuk ECU Mazduino

Manual ini berlaku untuk semua ECU Mazduino (Compact dan Mini 6CH) yang menggunakan firmware rusEFI dengan TunerStudio sebagai software tuning.

## Pengantar

TunerStudio adalah software tuning yang digunakan untuk mengkonfigurasi dan memonitor ECU Mazduino. Software ini memungkinkan Anda untuk mengatur parameter mesin, melihat data sensor real-time, dan melakukan tuning untuk performa optimal.

Dokumentasi ini telah dibagi menjadi bagian-bagian terpisah untuk memudahkan navigasi dan pemahaman. Setiap menu konfigurasi memiliki panduan lengkap dengan contoh praktis dan rekomendasi untuk unit Plug & Play maupun Kit/DIY.

## Daftar Menu Konfigurasi

### 🔧 [Pengaturan Output Controls](tunerstudio-output-controls.md)
Konfigurasi komprehensif untuk semua kontrol output ECU, meliputi:

- Main Relay dan Fuel Pump Control
- Tachometer dan Speedometer Output  
- Fan Cooling (Dual Fan Support)
- Starter Control dan Safety Features
- Check Engine Light Configuration

### ❄️ [Pengaturan Air Conditioning (A/C)](tunerstudio-ac-settings.md)
Kontrol sistem A/C yang terintegrasi dengan ECU, mencakup:

- Input dan Output Controls A/C
- Timing dan Protection Settings
- Kompensasi Idle Speed
- Kontrol Tekanan Sistem
- Status Monitoring dan Indikator

### 📋 Menu Konfigurasi Lainnya
*(Dalam pengembangan - akan ditambahkan secara bertahap)*

Menu tambahan yang akan tersedia:

- Pengaturan Fuel System
- Ignition Timing Control  
- Sensor Configuration
- Data Logging Setup
- Advanced Tuning Options

## Troubleshooting dan Diagnostik

Bagian ini menyediakan panduan komprehensif untuk mengidentifikasi dan menyelesaikan masalah umum yang ditemui selama operasi ECU Mazduino. Setiap masalah mencakup gejala, penyebab potensial, dan solusi yang direkomendasikan untuk memastikan fungsionalitas yang tepat.

### Masalah Umum dan Solusi

#### 1. Tidak Ada Sinyal RPM
**Gejala**: Mesin tidak menyala; gauge RPM tetap nol saat cranking.

**Kemungkinan Penyebab**:

- Sensor crankshaft atau camshaft tidak dipasang dengan benar
- Kabel sensor rusak atau terputus
- Jenis sensor atau konfigurasi salah di software

**Solusi**:

- Verifikasi pemasangan sensor crank dan cam yang tepat, pastikan alignment dan gap yang benar
- Periksa kabel yang rusak atau longgar dan pastikan semua koneksi aman
- Konfirmasi jenis sensor yang benar (Hall atau VR) dan konfigurasi di software Mazduino

#### 2. Pembacaan Sensor O2 Wideband Salah
**Gejala**: Pembacaan AFR tidak akurat atau tidak ditampilkan.

**Kemungkinan Penyebab**:

- Scaling sensor salah yang dikonfigurasi di software
- Kabel atau grounding sensor wideband rusak
- Miskonfigurasi sinyal CAN atau analog

**Solusi**:

- Verifikasi jenis sensor dan input scaling di software Mazduino (misal AEM, PLX, atau Custom)
- Inspeksi koneksi power dan ground ke controller wideband
- Konfirmasi konfigurasi CAN ID atau channel input analog yang benar

#### 3. Mesin Misfire atau Kasar
**Gejala**: Idle kasar, hesitasi saat akselerasi, atau misfire saat beban.

**Kemungkinan Penyebab**:

- Setting timing pengapian atau bahan bakar salah
- Busi rusak atau gap tidak tepat
- Driver injector atau koil gagal

**Solusi**:

- Gunakan timing light untuk verifikasi timing pengapian sesuai dengan base timing yang dikonfigurasi
- Inspeksi dan ganti busi jika aus atau gap salah
- Lakukan bench test untuk verifikasi output injector dan pengapian

#### 4. Tegangan Sensor Di Luar Rentang
**Gejala**: Peringatan error sensor di diagnostik; pembacaan sensor tidak menentu atau tidak ada.

**Kemungkinan Penyebab**:

- Kabel sensor rusak atau grounding salah
- Ketidakcocokkan kalibrasi antara sensor dan ECU
- Sensor rusak atau malfunction

**Solusi**:

- Periksa kabel sensor untuk kontinuitas dan grounding yang tepat
- Gunakan sinyal tegangan sensor mentah di menu diagnostik untuk konfirmasi pembacaan
- Ganti sensor jika rusak

#### 5. Alert Tekanan Bahan Bakar atau Oli
**Gejala**: Peringatan tekanan rendah atau engine shutdown saat beban.

**Kemungkinan Penyebab**:

- Kegagalan mekanis pada sistem delivery bahan bakar atau oli
- Threshold sensor tekanan salah konfigurasi
- Sensor tekanan rusak

**Solusi**:

- Inspeksi pompa bahan bakar, filter, dan pompa oli untuk masalah mekanis
- Sesuaikan threshold tekanan di software Mazduino sesuai spesifikasi sistem
- Ganti sensor yang rusak

#### 6. Error Kalibrasi Throttle
**Gejala**: ETB (Electronic Throttle Body) gagal kalibrasi; masalah respon throttle.

**Kemungkinan Penyebab**:

- Kalibrasi TPS dan PPS salah atau tidak lengkap
- Sensor posisi throttle atau pedal rusak
- Masalah kabel atau power supply

**Solusi**:

- Lakukan kalibrasi TPS dan PPS seperti yang dijelaskan di bagian setup
- Ganti sensor rusak jika kalibrasi gagal
- Pastikan kabel dan konektor utuh dan bertenaga dengan benar

### Tips Umum

- **Backup konfigurasi secara berkala** untuk menghindari kehilangan data
- **Gunakan menu diagnostik bawaan** untuk mereset kode error setelah menyelesaikan masalah
- **Untuk masalah yang persisten**, hubungi support Mazduino atau gunakan remote assistance untuk bantuan tambahan

Panduan ini memastikan pendekatan metodis untuk troubleshooting sistem Mazduino Anda, menggunakan alat diagnostik yang tersedia untuk performa yang andal.


---

*Manual ini akan terus diperbarui dengan penambahan menu konfigurasi baru. Pastikan Anda menggunakan versi terbaru untuk informasi yang akurat.*