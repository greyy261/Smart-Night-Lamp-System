# UTS Praktikum Mikrokontroler - Smart Night Lamp

**Nama:** [Suci yanti]  
**NIM:** [24090620025]  
**Materi:** LCD I2C, ADC (Sensor LDR), dan PWM (LED Dimming)

---

## 📝 Deskripsi Proyek
Proyek ini adalah sistem **Lampu Tidur Pintar** berbasis Arduino Uno. Sistem ini secara otomatis mengatur tingkat kecerahan lampu (LED) berdasarkan intensitas cahaya di dalam ruangan menggunakan sensor LDR. Semua status dan data sensor ditampilkan secara real-time melalui LCD 16x2 I2C.

## 🛠️ Implementasi Materi Praktikum
Sistem ini mengintegrasikan tiga materi utama:
1. **Pertemuan 4 (LCD I2C):** Menggunakan LiquidCrystal_I2C untuk menampilkan status sistem dan persentase cahaya dengan hanya menggunakan 2 pin data (SDA & SCL).
2. **Pertemuan 5 (ADC):** Menggunakan Pin Analog (A0) untuk membaca data dari sensor Photoresistor (LDR) dengan resolusi 10-bit (0-1023).
3. **Pertemuan 6 (PWM):** Menggunakan fungsi `analogWrite` pada Pin 9 untuk mengontrol kecerahan LED secara halus (dimming) berdasarkan hasil pemetaan (mapping) data sensor.

## ⚙️ Cara Kerja Sistem
1. Saat simulasi dimulai, LCD akan menampilkan pesan pembuka.
2. **Tombol (Push Button):** Berfungsi sebagai saklar utama. Jika ditekan, sistem akan beralih antara mode **AKTIF** atau **STANDBY**.
3. **Mode AKTIF:**
   - Sensor LDR membaca intensitas cahaya.
   - Menggunakan fungsi `map()`, nilai ADC dibalik (Inverse Mapping). Semakin rendah cahaya yang diterima LDR (Gelap), semakin tinggi nilai PWM yang dikirim ke LED (Terang).
   - LCD menampilkan status "AKTIF" dan persentase intensitas cahaya.
4. **Mode STANDBY:** - LED akan mati total dan LCD menampilkan status "STANDBY".

## 🔌 Rangkaian (Wiring)
- **LCD I2C:** VCC -> 5V, GND -> GND, SDA -> A4, SCL -> A5.
- **LDR:** Pin A0 (dengan resistor pembagi tegangan 10k Ohm).
- **LED:** Pin 9 (dengan resistor 220 Ohm).
- **Button:** Pin 2 (Internal Pull-up).

## 🎥 Dokumentasi
- **Link Simulasi Tinkercad:** [https://www.tinkercad.com/things/230F2bY1WxK-smartlamp]
- **Link Video Demo:** [[Tempel link YouTube/Google Drive video kamu di sini](https://drive.google.com/drive/folders/1sRZRREcBPHnNli6WhvZtpj6nNPZJWxAC?usp=drive_link)]
