# Manual Tuning TunerStudio untuk ECU Mazduino

Manual ini berlaku untuk semua ECU Mazduino (Compact dan Mini 6CH) yang menggunakan firmware rusEFI dengan TunerStudio sebagai software tuning.

## Pengantar Mazduino dan TunerStudio

### Selamat Datang di Mazduino!

Selamat atas pilihan Anda untuk menggunakan Mazduino, sebuah Engine Control Unit (ECU) yang canggih dan serbaguna yang dirancang untuk tuning performa tinggi dan kustomisasi. Dengan software TunerStudio, Mazduino memberikan Anda kontrol tingkat lanjut, monitoring secara real-time, dan precision tuning untuk berbagai aplikasi, mulai dari kendaraan harian hingga kompetisi motorsport.

### Gambaran Umum

Seri Mazduino dapat terintegrasi dengan sempurna dengan software TunerStudio, menawarkan paket lengkap untuk manajemen mesin dan analisis data. Interface TunerStudio yang intuitif dan fitur-fiturnya yang handal memungkinkan baik pemula maupun profesional untuk memonitor, melakukan tuning, dan mengoptimalkan parameter mesin secara real-time.

### Fitur Utama dan Keuntungan

- **Monitoring Mesin Real-Time**  
  TunerStudio menyediakan data langsung untuk parameter mesin yang kritis, termasuk RPM, tekanan bahan bakar, air-fuel ratio, boost pressure, dan lainnya, membantu Anda memantau performa dengan mudah.

- **Opsi Tuning yang Dapat Disesuaikan**  
  Menyesuaikan pengaturan mesin untuk tujuan performa spesifik. Atur fuel map, ignition timing, dan boost level untuk memenuhi kebutuhan setiap kondisi berkendara.

- **Data Logging dan Analisis Tingkat Lanjut**  
  Merekam dan meninjau data performa kunci untuk mendapatkan wawasan tentang perilaku mesin. Analisis data log untuk memperbaiki parameter tuning dan meningkatkan efisiensi secara keseluruhan.

- **Interface yang User-Friendly dan Dapat Dikonfigurasi**  
  Interface TunerStudio memungkinkan dashboard yang dapat disesuaikan di mana Anda dapat mengatur tampilan data penting sesuai preferensi, memastikan kemudahan akses ke data yang diperlukan.

### Kebutuhan Sistem dan Instalasi

Untuk menggunakan TunerStudio dengan Mazduino, pastikan perangkat Anda memenuhi persyaratan minimum berikut:

- **Sistem Operasi**: Windows 10 atau yang lebih baru, macOS, atau Linux
- **Hardware**: Minimum RAM 4GB, processor 2GHz, dan storage tersedia 500MB
- **Koneksi**: Port USB untuk komunikasi langsung dengan Mazduino

**Instalasi**:

1. Download versi TunerStudio terbaru dari website resmi Mazduino
2. Ikuti petunjuk di layar untuk menginstal TunerStudio
3. Hubungkan Mazduino Anda melalui USB untuk membuat koneksi real-time data dan tuning

### Informasi Keselamatan dan Kepatuhan Penting

- **Keselamatan Utama**: Jangan pernah melakukan penyesuaian tuning saat kendaraan sedang bergerak. Pastikan mesin dimatikan sebelum mengubah pengaturan mesin apapun.
- **Kepatuhan dan Update**: Secara berkala periksa update software dari Mazduino untuk memastikan performa optimal dan kepatuhan dengan standar terbaru.

## Instalasi dan Informasi Wiring

### Mengapa Output untuk Beban Berat Membutuhkan Relay

ECU, termasuk Mazduino, menyediakan **output tingkat logika arus rendah** untuk mengontrol perangkat seperti fan, fuel pump, atau solenoid. Output ini tidak dirancang untuk menangani arus tinggi yang dibutuhkan oleh perangkat tersebut. Menggunakan relay memungkinkan ECU untuk mengontrol perangkat bertenaga tinggi dengan aman:

1. **Mengisolasi Arus Tinggi dari ECU**:
   - ECU hanya perlu mengirim sinyal kecil ke relay, yang menangani aliran arus tinggi ke perangkat
   - Ini mencegah kerusakan pada rangkaian output ECU

2. **Mencegah Kelebihan Beban**:
   - Menghubungkan perangkat beban tinggi langsung ke ECU dapat menyebabkan panas berlebih atau kerusakan permanen karena tarikan arus yang berlebihan

3. **Menyediakan Operasi yang Aman**:
   - Relay melindungi wiring dan komponen elektrik dengan bertindak sebagai switch, mengurangi risiko hubung singkat atau panas berlebih

### Rekomendasi untuk Wiring: Crimping vs. Soldering

#### Crimping Kabel

Crimping lebih disukai untuk wiring otomotif karena lebih cepat, tahan lama, dan tahan getaran jika dilakukan dengan benar:

1. **Alat yang Dibutuhkan**:
   - Gunakan **ratcheting crimp tool** yang dirancang untuk konektor otomotif
   - Sesuaikan mata crimp tool dengan jenis terminal (open barrel, insulated, dll.)

2. **Teknik**:
   - Kupas kabel sepanjang yang benar (biasanya 4-6mm) tanpa merusak untaian kawat
   - Masukkan kabel ke dalam terminal dan crimp dengan kuat
   - Periksa hasil crimp untuk memastikan kencang dan aman, tanpa untaian kawat yang lepas

3. **Heat Shrink**:
   - Gunakan heat shrink tubing di atas sambungan untuk melindungi dari kelembaban dan korosi

#### Soldering Kabel

Soldering memberikan konektivitas elektrik yang sangat baik tetapi kurang tahan getaran:

1. **Alat yang Dibutuhkan**:
   - Gunakan **soldering iron berkualitas tinggi** dan **solder grade otomotif** (rosin-core, leaded solder ideal)

2. **Teknik**:
   - Kupas kabel, puntir untaian kawat bersama, dan aplikasikan flux
   - Panaskan sambungan dengan soldering iron dan aplikasikan solder hingga mengalir dengan halus ke dalam sambungan
   - Biarkan dingin tanpa mengganggu sambungan

3. **Isolasi**:
   - Tutupi sambungan yang di-solder dengan heat shrink atau electrical tape untuk perlindungan

### Tips Instalasi ECU Aftermarket Umum

#### Persiapan

1. **Merencanakan Wiring**:
   - Gunakan diagram wiring yang spesifik untuk ECU dan kendaraan Anda
   - Beri label pada kabel dan rencanakan jalur untuk menghindari kebingungan selama instalasi

2. **Tes Sensor dan Perangkat**:
   - Verifikasi kesehatan dan kompatibilitas sensor (misalnya TPS, MAP, IAT) sebelum menghubungkannya ke ECU

#### Power dan Grounding

1. **Suplai Daya Khusus**:
   - Hubungkan ECU ke sumber daya +12V yang bersih dan menggunakan fuse
   - Gunakan rangkaian daya yang dikontrol relay untuk ECU agar memastikan mati saat ignition dimatikan

2. **Grounding**:
   - Pastikan semua ground (ECU, sensor, dan mesin) terhubung ke **titik ground bersama**
   - Gunakan kabel ground yang tebal dan berkualitas tinggi untuk meminimalkan voltage drop

### Pentingnya Grounding yang Tepat dalam Sistem ECU

Grounding adalah aspek kritis dari sistem elektrik apapun, terutama dalam aplikasi otomotif. Untuk ECU seperti Mazduino, grounding yang tepat memastikan operasi yang stabil, pembacaan sensor yang akurat, dan mencegah kerusakan pada komponen sensitif.

#### Mengapa Grounding yang Tepat Sangat Penting

1. **Melengkapi Rangkaian**:
   - Ground adalah jalur kembali untuk arus listrik, melengkapi rangkaian untuk semua perangkat
   - Ground yang buruk dapat menyebabkan koneksi listrik yang terputus-putus, mengakibatkan perilaku sistem yang tidak stabil

2. **Mencegah Noise Elektrik**:
   - Grounding yang baik meminimalkan interferensi elektrik, atau "noise," yang dapat mengganggu sinyal dalam rangkaian sensitif

3. **Memastikan Pengukuran yang Akurat**:
   - Banyak sensor bergantung pada referensi ground yang konsisten. Variasi dalam potensial ground dapat mengakibatkan pembacaan sensor yang tidak akurat

4. **Melindungi Komponen**:
   - Grounding yang tepat membantu membuang kelebihan arus dengan aman, melindungi ECU dan perangkat yang terhubung dari kerusakan

#### Mengapa Power Ground dan Sensor Ground Terpisah

ECU memiliki **power ground** dan **sensor ground** yang khusus karena rangkaian ini melayani tujuan yang berbeda dan memiliki persyaratan yang unik:

**1. Power Ground**
- **Tujuan**: Menangani arus balik dari perangkat bertenaga tinggi seperti injector, ignition coil, fuel pump, dan relay
- **Karakteristik**: Arus ini seringkali besar dan dapat berfluktuasi dengan cepat saat perangkat menyala dan mati
- **Dampak Koneksi yang Salah**: Jika arus power ground mengalir melalui rangkaian sensor ground, mereka dapat menimbulkan noise dan fluktuasi voltase

**2. Sensor Ground**
- **Tujuan**: Menyediakan titik referensi yang stabil dan bebas noise untuk sensor bertenaga rendah seperti TPS, MAP, dan IAT
- **Karakteristik**: Ground ini membawa arus yang sangat kecil, dan gangguan apapun dapat secara signifikan mempengaruhi integritas sinyal
- **Dampak Koneksi yang Salah**: Jika sensor ground tidak diisolasi, noise arus tinggi dari perangkat power dapat menyebabkan pembacaan sensor yang tidak menentu atau bahkan salah interpretasi ECU

### Best Practice untuk Grounding dalam Sistem Otomotif

1. **Gunakan Titik Ground Bersama**:
   - Hubungkan semua power ground ECU ke satu titik ground yang bersih (misalnya terminal negatif aki)
   - Pastikan sensor ground kembali langsung ke ECU tanpa melewati chassis

2. **Isolasi Sensor Ground**:
   - Jangan pernah hubungkan sensor ground langsung ke chassis. Gunakan pin sensor ground khusus ECU untuk semua sensor

3. **Pastikan Koneksi yang Aman**:
   - Gunakan teknik crimping atau soldering yang tepat dan bersihkan titik kontak untuk meminimalkan resistansi dan mencegah voltage drop

4. **Gunakan Kabel Berpelindung**:
   - Untuk sinyal sensitif (misalnya sensor crank dan cam), gunakan kabel berpelindung yang di-ground di satu ujung untuk mengurangi interferensi elektromagnetik

5. **Periksa Integritas Grounding**:
   - Secara berkala periksa koneksi ground untuk korosi, sambungan yang kendor, atau kabel yang rusak

**Pengingat Keselamatan**: Sebelum menginstal atau menangani wiring apapun, putuskan aki kendaraan untuk mencegah hubung singkat atau kerusakan pada komponen.

**Catatan Penting**:
- Pastikan semua koneksi wiring mengikuti spesifikasi yang direkomendasikan untuk performa dan keselamatan terbaik
- Gunakan hanya konektor berkualitas tinggi dan isolasi yang tepat untuk semua sambungan

## Pengantar TunerStudio

TunerStudio adalah software tuning yang digunakan untuk mengkonfigurasi dan memonitor ECU Mazduino. Software ini memungkinkan Anda untuk mengatur parameter mesin, melihat data sensor real-time, dan melakukan tuning untuk performa optimal.

Dokumentasi ini telah dibagi menjadi bagian-bagian terpisah untuk memudahkan navigasi dan pemahaman. Setiap menu konfigurasi memiliki panduan lengkap dengan contoh praktis dan rekomendasi untuk unit Plug & Play maupun Kit/DIY.

## Daftar Menu Konfigurasi

### 📥 [Instalasi TunerStudio](tunerstudio-instalasi.md)
Panduan lengkap instalasi TunerStudio untuk ECU Mazduino, meliputi:

- Download dan instalasi step-by-step
- Konfigurasi system requirements
- Troubleshooting masalah instalasi
- Setup driver dan koneksi USB

### ⚙️ [Konfigurasi Project TunerStudio](tunerstudio-konfigurasi.md)
Setup project baru dan konfigurasi ECU connection, mencakup:

- Membuat project baru dari awal
- Deteksi dan koneksi ECU Mazduino
- Konfigurasi communication settings
- Verifikasi koneksi dan troubleshooting

### 🖥️ [Interface dan Menu TunerStudio](tunerstudio-interface.md)
Panduan navigasi dan penggunaan interface TunerStudio, meliputi:

- Overview interface dan dashboard
- File menu (project dan tune management)
- Options menu (pengaturan interface)
- Data logging, communications, dan tools menu

### ⚙️ [Base Engine Settings](tunerstudio-base-engine.md)
Konfigurasi dasar engine untuk operasi ECU yang tepat, mencakup:

- Engine configuration (cylinders, displacement, firing order)
- Fuel strategy selection (Speed Density, MAF, Alpha-N, Lua)
- Engine metadata dan forced induction settings
- Layout selection dan best practices

### 🛡️ [Limits and Protection](tunerstudio-limits-protection.md)
Sistem proteksi untuk melindungi engine dari kerusakan, meliputi:

- Limits and Fallbacks (RPM, boost, injector duty cycle)
- Oil Pressure Protection
- Lambda Protection (AFR monitoring)
- Soft RPM limits dan electronic throttle limiting

### ⛽ [Fuel System Configuration](tunerstudio-fuel-system.md)
Konfigurasi komprehensif sistem bahan bakar, mencakup:

- Injection configuration dan hardware settings
- VE (Volumetric Efficiency) table tuning
- Target AFR table dan closed loop correction
- Acceleration enrichment dan fuel cutoff (DFCO)

### ⚡ [Ignition System Configuration](tunerstudio-ignition.md)
Setup sistem ignition untuk performance optimal, meliputi:

- Ignition mode selection (single coil, individual coils, wasted spark)
- Ignition timing table dan dwell configuration
- CLT/IAT timing corrections
- Multispark, knock control, dan cylinder trims

### 📊 [Sensor Configuration](tunerstudio-sensors.md)
Konfigurasi lengkap semua jenis sensor untuk monitoring dan kontrol engine, mencakup:

- Setup sensor analog dan digital
- Kalibrasi TPS, MAP, CLT, IAT dan sensor lainnya
- Konfigurasi O2 sensor dan wideband controller
- VR sensor threshold dan speed sensor setup

### 🌐 [CAN Bus Configuration](tunerstudio-canbus.md)
Setup komunikasi CAN Bus untuk integrasi dengan perangkat eksternal, meliputi:

- Konfigurasi CAN Bus communication settings
- Setup CAN O2 sensors dan EGT sensors
- CAN vehicle speed sensor configuration
- Integration dengan dashboard dan IO box

### 🎛️ [Controller & Diagnostics](tunerstudio-controller.md)
Tool diagnostik dan testing untuk troubleshooting sistem, mencakup:

- Bench testing injector dan ignition outputs
- Fancy Board configuration untuk ECU wire-in
- Traction control tables dan tuning
- SD Card logging dan rusEFI console

### 🔧 [Troubleshooting](tunerstudio-troubleshooting.md)
Panduan komprehensif untuk mengatasi masalah sistem Mazduino, meliputi:

- Diagnosis masalah umum (no RPM signal, sensor errors)
- Tool diagnostik dan raw sensor monitoring
- Error codes dan prosedur reset
- Best practices untuk maintenance preventif

### 📈 [Examples & Map Switching](tunerstudio-examples.md)
Contoh implementasi praktis dan fitur advanced, mencakup:

- Setup map switching untuk kondisi operasi berbeda
- Progressive tuning dan automatic switching
- Integration dengan launch control dan traction control
- Safety considerations dan best practices

## Kesimpulan

Manual TunerStudio Mazduino ini menyediakan panduan lengkap untuk mengoptimalkan performa engine management system. Dengan mengikuti dokumentasi ini secara sistematis, Anda akan dapat:

1. **Setup Sistem dengan Benar**: Instalasi dan konfigurasi yang tepat untuk operasi yang reliable
2. **Tuning yang Aman**: Implementasi protection system dan monitoring yang adequate
3. **Optimasi Performa**: Advanced tuning techniques untuk hasil maksimal
4. **Troubleshooting Efektif**: Diagnosis dan penyelesaian masalah dengan tool yang tepat

### Tips Sukses

- **Mulai dengan Conservative Settings**: Selalu mulai dengan pengaturan yang aman dan tingkatkan bertahap
- **Documentation**: Catat semua perubahan dan hasil testing untuk referensi masa depan  
- **Safety First**: Jangan pernah mengorbankan keandalan untuk performa
- **Continuous Learning**: Engine tuning adalah proses berkelanjutan yang memerlukan pembelajaran terus-menerus

### Support dan Komunitas

Untuk dukungan teknis dan diskusi dengan pengguna Mazduino lainnya:

- **Website Resmi**: [www.mazduino.com](https://www.mazduino.com)
- **Support Email**: support@mazduino.com
- **Forum Komunitas**: Bergabung dengan komunitas tuner Mazduino
- **Documentation Updates**: Manual ini akan terus diperbarui dengan fitur dan improvement baru

---

*Manual TunerStudio Mazduino v1.0 - Dokumentasi lengkap untuk engine management yang optimal.*

### � [Instalasi TunerStudio](tunerstudio-instalasi.md)
Panduan lengkap instalasi TunerStudio untuk ECU Mazduino, meliputi:

- Download dan instalasi step-by-step
- Konfigurasi system requirements
- Troubleshooting masalah instalasi
- Setup driver dan koneksi USB

### ⚙️ [Konfigurasi Project TunerStudio](tunerstudio-konfigurasi.md)
Setup project baru dan konfigurasi ECU connection, mencakup:

- Membuat project baru dari awal
- Deteksi dan koneksi ECU Mazduino
- Konfigurasi communication settings
- Verifikasi koneksi dan troubleshooting

### 🖥️ [Interface dan Menu TunerStudio](tunerstudio-interface.md)
Panduan navigasi dan penggunaan interface TunerStudio, meliputi:

- Overview interface dan dashboard
- File menu (project dan tune management)
- Options menu (pengaturan interface)
- Data logging, communications, dan tools menu

### ⚙️ [Base Engine Settings](tunerstudio-base-engine.md)
Konfigurasi dasar engine untuk operasi ECU yang tepat, mencakup:

- Engine configuration (cylinders, displacement, firing order)
- Fuel strategy selection (Speed Density, MAF, Alpha-N, Lua)
- Engine metadata dan forced induction settings
- Layout selection dan best practices

### �️ [Limits and Protection](tunerstudio-limits-protection.md)
Sistem proteksi untuk melindungi engine dari kerusakan, meliputi:

- Limits and Fallbacks (RPM, boost, injector duty cycle)
- Oil Pressure Protection
- Lambda Protection (AFR monitoring)
- Soft RPM limits dan electronic throttle limiting

### ⛽ [Fuel System Configuration](tunerstudio-fuel-system.md)
Konfigurasi komprehensif sistem bahan bakar, mencakup:

- Injection configuration dan hardware settings
- VE (Volumetric Efficiency) table tuning
- Target AFR table dan closed loop correction
- Acceleration enrichment dan fuel cutoff (DFCO)

### ⚡ [Ignition System Configuration](tunerstudio-ignition.md)
Setup sistem ignition untuk performance optimal, meliputi:

- Ignition mode selection (single coil, individual coils, wasted spark)
- Ignition timing table dan dwell configuration
- CLT/IAT timing corrections
- Multispark, knock control, dan cylinder trims

### �🔧 [Pengaturan Output Controls](tunerstudio-output-controls.md)
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