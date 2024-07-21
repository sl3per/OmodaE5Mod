# OmodaE5Mod

## Auto On/Off Seat Ventilation when AC On/Off
> [!CAUTION]
> **!!! Disclaimer : Segala kerusakan terkait mobil anda diluar tanggung jawab developer aplikasi ini, pastikan mengerti konsekuensinya**
> > [!IMPORTANT]
> **!!! Penting : Pastikan anda mengerti tentang apa itu _adb, adb shell, adb push, pm install_**
1. Download   [E5-AutoOnOffSeatVent-V1.1.apk](https://github.com/sl3per/OmodaE5Mod/raw/main/E5-AutoOnOffSeatVent-V1.1.apk)
     - V1.1 : Penambahan fitur Gear Speed
3. Push apk dan install apk ke HU, pastikan ADB sudah enabled, caranya ada dibagian bawah
4. Masuk ke homescreen (4 titik kanan bawah), scroll ke bawah, klik apps **AutoSeatVent**
5. Aplikasi akan running setiap kondisi layar HU nyala, bila Automasi tidak jalan, jalankan no 3 lagi


https://github.com/user-attachments/assets/c66aacf2-d840-45dc-a1d7-6817c38b49a3


## OBD monitoring khusus Omoda E5 untuk Android, mirip carscanner

- Apk ini di install di HP (tidak semua HP support, cuma tes di Samsung A52), bukan di HU, paling enak install di carlinkit
- Untuk dongle OBD2, gunakan yg versi ELM327 v2.2, yg murah dibawah 100 rb tidak support, bisa pake "vgate iCar 2 OBD2 ELM327", harga 200 rb an
- Kodingan asal, ada proteksi untuk sleep ketika aki < 13 V
- Masuk ke setting, pilih Bluetooth OBD2 yang sudah di pair
- Ketika buka lagi, tap di icon Konek di sebelah kanan atas
- Apk file : 
  [(E5OBD-1.1.apk](https://github.com/sl3per/OmodaE5Mod/raw/main/E5OBD-1.1.apk))]
![image](https://github.com/user-attachments/assets/d1c20bb1-74f3-4b97-a430-73164f1dec0f)
![image](https://github.com/user-attachments/assets/65d3bef3-611b-44cd-9035-a24004fa8b3a)


## Install apk di HU Omoda E5
1. Cara masuk ke hidden menu
  - Masuk ke Local Setting - System Setting
  - Tap 10x di kiri tengah - atas
2. Cara enable ADB
  - Tap Encryption
  - Kalikan 6 digit terakhir serialId /  productId dengan 802018
  - Masukkan 6 digit terakhir di kolom password
  - Masuk ke menu ADB, pilih Open
3. Cara Install apk di HU
  - Enable ADB
  - Koneksikan adb client (windows only) ke HU melalui kabel USB-A
  - Install apk seperti biasa (adb push - pm install)
  - pertama, "adb push" dulu apk ke /data/local/tmp, kemudian masuk ke "adb shell", baru "pm install" apknya

## More coding 
1. Disable AEB + DMS
   - moduleid : 327681, cmdid : 37 , payload (1 = ON, 2 = OFF) // AEB
   - moduleid : 327681, cmdid : 195 , payload (1 = ON, 2 = OFF) // DMS
     
2. Auto Seat Vent if AC ON
  - Subs moduleid : 327690, cmdid : 1
  - Turn on Seat Vent :
     - moduleid : 327681, cmdid : 94 , payload (1 = OFF, 2-4 = Speed) // Driver side
     - moduleid : 327681, cmdid : 93 , payload (1 = OFF, 2-4 = Speed) // Pasenger side







