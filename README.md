# Jobsheet3_Embedded-System
TOPOLOGI JARINGAN LOKAL DAN WIFI

I. PENJELASAN SINGKAT

Wireless Fidelity atau yang lebih awam kita sebut wifi adalah suatu teknologi yang menggunakan gelombang radio dalam rentang 2,4GHz sampai dengan 5GHz untuk menghubungkan perangkat seperti PC/laptop, smartphone, dan perangkat microcontroller seperti ESP32 dan ESP8266 ke jaringan lokal wireless untuk bisa mengakses internet. Berbagai data yang kita minta atau kirimkan melalui wifi didistribusikan melalui gelombang radio di udara. Supaya data tersebut bisa terbaca maka harus ada yang namanya wireless adaptor yang menghubungkan ke wifi. Gelombang radio yang berwujud sinyal ini lalu dikirim menuju router untuk memecahkan kode. Setelah terbaca maka data dikirim ke jaringan internet yang memanfaatkan koneksi ethernet. Karena jaringan wifi ini bekerja dua arah maka tiap data yang diterima dalam waktu yang sama menjadi kode pada tiap paket data lalu dikirim kembali dalam bentuk sinyal radio yang diterima adaptor komputer nirkabel. 

II. ALAT DAN BAHAN

    1) ESP32
    2) Breadboard
    3) Kabel jumper
    4) Sensor DHT 11, RFID
    5) LED (5) dan Push Button (3)
    6) Servo
    7) Resistor 330,1K, 10K Ohm (@ 3)

III. LANGKAH PERCOBAAN 

     A.ESP32 Wi-Fi Modes dan Wifi-Scan
       1.	Pada ESP32, terdapat 3 mode akses untuk Wifi, yaitu WIFI_STA (station mode : ESP32 sebagai client yang terkoneksi ke access point), WIFI_AP (access point mode : ESP32 berperan sebagai access point), WIFI_STA_AP (access point and station : ESP32 dapat terkoneksi dengan access point yang lain).
       2.	Buka Arduino IDE dan upload script program ESP32WifiModesScan.ino ke ESP32 untuk melakukan scan jaringan Wi-Fi.
       3.	Buka serial monitor dan hasilnya akan seperti gambar A1 di bawah ini
![A1](https://user-images.githubusercontent.com/121161133/209753952-91df1a86-f586-4df7-b4e3-4ba9e15fb9fa.png)

       4.	Buatlah flow chart program diatas.

     B.Menghubungkan ESP32 dengan Jaringan Wi-Fi 
       1. Buatlah program seperti script MenghubungkandenganWifi.ino , kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, hasilnya akan seperti gambar B1 berikut ini 
![B1](https://user-images.githubusercontent.com/121161133/209753965-72ec2014-e9fb-4076-9423-c050fa6273ad.png)

       3. Buatlah flow chart program diatas.

     C.Menghubungkan Kembali (Re-connect) ESP32 dengan Jaringan Wi-Fi 
       1. Buatlah program seperti script Reconnect.ino , kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, kemudian matikan paket data sebentar hingga koneksi ESP32 dengan jaringna Wi-Fi terputus. Setelah itu, nyalakan lagi paket data.
Hasilnya akan seperti pada gambar C1 berikut ini
![C1](https://user-images.githubusercontent.com/121161133/209753991-00f7734c-6924-4e9e-8ccf-47754a98580a.png)

       3. Buatlah flow chart program diatas.

     D.Mengganti Hostname ESP32 
       1. Buatlah program seperti script Mengganti Hostname ESP32.ino , kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, kemudian aktifkan mode koneksi Wi-Fi pada SmartPhone atau Laptop. Lakukan scan dan lihat daftar jaringan Wi-Fi yang tersedia.
Hasilnya akan seperti pada gambar D1 di bawah ini
![D1](https://user-images.githubusercontent.com/121161133/209754018-d2ac4f61-0d10-47ee-9f35-74ca1210e783.png)

       3. Buatlah flow chart program diatas.

     E.Mengirim Data Sensor ke Database 
       1. Buatlah rangkaian seperti Gambar di bawah ini. (gambar ke-2 merupakan dokumentasi rangkaian yang telah dibuat)
![E1](https://user-images.githubusercontent.com/121161133/209754041-6c7b75c7-b828-4eb1-a6c2-fea3d1144c1b.png)
![E2](https://user-images.githubusercontent.com/121161133/209754815-999739a0-cfb6-405c-8b78-41656a5032be.png)

       2. Install library Asynch Web Server dan Asycnh TCP untuk ESP 32 dengan cara download dari link berikut ini. 
          a. https://github.com/me-no-dev/ESPAsyncWebServer 
          b. https://github.com/me-no-dev/AsyncTCP/archive/master.zip 
          Install library tersebut secara manual dengan cara menyalin folder hasil ekstraksi file.zip ke direktori libarary Arduino di folder Document.
       3. Buatlah script program seperti berikut ini.
       4. Upload program seperti pada script DataSensorKeDataBase.ino , kemudian buka serial monitor untuk mengetahui IP Address ESP32.
Maka, hasilnya akan seperti gambar E3 di bawah ini
![E3](https://user-images.githubusercontent.com/121161133/209754093-8a5531e9-4985-4cea-bfd2-9574278d43df.png)

       5. Akses IP Address ESP32 pada browser laptop. Dokumentasikan hasilnya dan buatlah flow chart dari program tersebut.
Hasilnya akan seperti gambar E4 berikut ini
![E4](https://user-images.githubusercontent.com/121161133/209755148-cc1baa54-04d5-4419-bb9b-f96644d8a156.png)

