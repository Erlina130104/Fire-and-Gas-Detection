Sistem Deteksi Api dan Gas Berbasis Arduino
Proyek ini merupakan sistem monitoring bahaya kebakaran dan kebocoran gas menggunakan Arduino, sensor api (flame sensor), sensor gas MQ-2, buzzer, dan LCD I2C. Sistem ini akan menampilkan status di LCD dan memberikan peringatan melalui buzzer dan LED jika terdeteksi kondisi berbahaya.
Fitur Utama
- Mendeteksi keberadaan api menggunakan sensor flame
- Mendeteksi keberadaan gas berbahaya menggunakan sensor MQ-2
- Menampilkan status bahaya di LCD 16x2 I2C
- Memberikan peringatan menggunakan buzzer dan LED
- Menampilkan data sensor ke Serial Monitor
 Komponen yang Digunakan
1.	Arduino (Uno/Mega), berfungsi sebagai  mikrokontroler utama           
2.	Sensor Api (Flame ), berfungsi untuk mendeteksi cahaya api          
3.	Sensor Gas MQ-2, berfungsi untuk endeteksi gas berbahaya       
4.	Buzzer, berfungsi untuk alarm suara peringatan         
5.	LED Merah, berfungsi untuk indikator bahaya api
6.	 LED Kuning ), berfungsi untuk indikator bahaya gas       
7.	 LCD 16x2 I2C ), berfungsi untuk menampilkan informasi bahaya 
8.	 Kabel Jumper,  berfungsi untuk koneksi antar komponen         

 Pin Konfigurasi
1.	Sensor Api, pin arduino A0          
2.	Sensor Gas (MQ-2), pin arduino A1          
3.	Buzzer, pin arduino 11          
4.	LED Api, pin arduino 9           
5.	LED Gas, pin arduino 6           
6.	LCD SDA/SCL, pin arduino A4 / A5 (Uno) / 20/21 (Mega) 
Cara Kerja
- Jika sensor api mendeteksi nilai di bawah ambang (`< 100`), maka:
  - LCD menampilkan “deteksi ada Api!”
  - Buzzer berbunyi
  - LED merah menyala
- Jika sensor MQ-2 mendeteksi nilai gas di atas ambang (`> 500`), maka:
  - LCD menampilkan “deteksi ada Gas!”
  - Buzzer berbunyi
  - LED kuning menyala
- Jika tidak ada bahaya:
  - LCD menampilkan “Tidak ada bahaya”
  - Semua alarm dan LED dimatikan
 Data Serial
Setiap 1 detik, nilai sensor ditampilkan di Serial Monitor.
