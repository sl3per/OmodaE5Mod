# OmodaE5Mod
Omoda E5 Mod


/////// OBD monitoring khusus Omoda E5 untuk Android, mirip carscanner
- Kodingan asal, ada proteksi untuk sleep ketika aki < 13 V
- Masuk ke setting, pilih Bluetooth OBD2 yang sudah di pair
- Ketika buka lagi, tap di icon Konek di sebelah kanan atas
- Apk file : 
  [([https://github.com/sl3per/OmodaE5Mod/blob/main/E5OBD.apk](https://github.com/sl3per/OmodaE5Mod/raw/main/E5OBD-1.1.apk))](https://github.com/sl3per/OmodaE5Mod/raw/main/E5OBD-1.1.apk)
![image](https://github.com/user-attachments/assets/d1c20bb1-74f3-4b97-a430-73164f1dec0f)
![image](https://github.com/user-attachments/assets/65d3bef3-611b-44cd-9035-a24004fa8b3a)


/////// Install apk di HU Omoda E5
1. Cara masuk ke hidden menu
  - Masuk ke Local Setting - System Setting
  - Tap 10x di kiri tengah - atas
2. Cara enable ADB
  - Tap Encryption
  - Kalikan 6 digit serial id dengan 802018
  - Masukkan 6 digit terakhir di kolom password
  - Masukke menu ADB, pilih Open
3. Cara Install apk di HU
  - Enable ADB
  - Koneksikan adb client (windows only) ke HU melalui kabel USB-A
  - Install apk seperti biasa (adb push - pm install)

///// More coding 
1. Disable AEB + DMS
   - moduleid : 327681, cmdid : 37 , payload (1 = ON, 2 = OFF) // AEB
   - moduleid : 327681, cmdid : 195 , payload (1 = ON, 2 = OFF) // DMS
     
2. Auto Seat Vent if AC ON
  - Subs moduleid : 327690, cmdid : 1
  - Turn on Seat Vent :
     - moduleid : 327681, cmdid : 94 , payload (1 = OFF, 2-4 = Speed) // Driver side
     - moduleid : 327681, cmdid : 93 , payload (1 = OFF, 2-4 = Speed) // Pasenger side

       
https://github.com/user-attachments/assets/b54f2e7a-71da-47c0-afd3-124166d21fad





