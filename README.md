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
       2.	Buka Arduino IDE dan upload script program berikut ke ESP32 untuk melakukan scan jaringan Wi-Fi.
       3.	Buka serial monitor dan akan muncul tampilan seperti gambar 1 di bawah ini
![1](https://user-images.githubusercontent.com/121161133/209560941-d454459f-5e37-4c6f-b4e2-ca7432d0b715.png)

       4.	Buatlah flow chart program diatas.

     B.Menghubungkan ESP32 dengan Jaringan Wi-Fi 
       1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, kemudian dokumentasikan outputnya. 
![2](https://user-images.githubusercontent.com/121161133/209560979-ce43e6c3-17ad-421c-a43a-a55bbfb37072.png)

       3. Buatlah flow chart program diatas.

     C.Menghubungkan Kembali (Re-connect) ESP32 dengan Jaringan Wi-Fi 
       1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, kemudian matikan paket data sebentar hingga koneksi ESP32 dengan jaringna Wi-Fi terputus. Setelah itu, nyalakan lagi paket data. Dokumentasikan proses yang terjadi. 
![3](https://user-images.githubusercontent.com/121161133/209561068-6205933a-621c-4dc5-8fd1-4d4cc7e06257.png)

       3. Buatlah flow chart program diatas.

     D.Mengganti Hostname ESP32 
       1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
       2. Buka serial monitor, kemudian aktifkan mode koneksi Wi-Fi pada SmartPhone atau Laptop. Lakukan scan dan lihat daftar jaringan Wi-Fi yang tersedia. Dokumentasikan hasil keluarannya. 
![4](https://user-images.githubusercontent.com/121161133/209561133-d6612e48-963c-42dc-a446-7304bd476dfd.png)

       3. Buatlah flow chart program diatas.

     E.Mengirim Data Sensor ke Database 
       1. Buatlah rangkaian seperti Gambar di bawah ini.
![5](https://user-images.githubusercontent.com/121161133/209561264-74fc29f9-529e-46f3-a631-a485e01e348a.png)

       2. Install library Asynch Web Server dan Asycnh TCP untuk ESP 32 dengan cara download dari link berikut ini. 
          a. https://github.com/me-no-dev/ESPAsyncWebServer 
          b. https://github.com/me-no-dev/AsyncTCP/archive/master.zip 
          Install library tersebut secara manual dengan cara menyalin folder hasil ekstraksi file.zip ke direktori libarary Arduino di folder Document.
       3. Buatlah script program seperti berikut ini.
       4. Upload program di atas. Kemudian buka serial monitor untuk mengetahui IP Address ESP32. 
![6](https://user-images.githubusercontent.com/121161133/209561313-f9443799-5047-4aba-8b8c-40f4bd8810e4.png)
![7](https://user-images.githubusercontent.com/121161133/209561333-5bc6d647-04b6-4a58-af2f-bdf5654e46c7.png)

       5. Akses IP Address ESP32 pada browser laptop. Dokumentasikan hasilnya dan buatlah flow chart dari program tersebut.
