# OmodaE5Mod
Omoda E5 Mod

/////// OBD monitoring khusus Omoda E5
- Kodingan asal, ada proteksi untuk sleep ketika aki < 13 V
  https://github.com/aguscah/OmodaE5Mod/blob/main/E5OBD.apk

/////// Install apk di HU Omoda E5
1. Cara masuk ke hidden menu
  - Masuk ke Local Setting
  - Tap 10x di kiri tengah - atas
2. Cara enable ADB
  - Tap Encryption
  - Kalikan 6 digit serial id dengan 802018
  - Masukkan 6 digit terakhir di kolom password
3. Cara Install apk di HU
  - Enable ADB
  - Koneksikan adb client (windows only) ke HU melalui kabel USB-A
  - Install apk seperti biasa (adb push - pm install)

///// More coding 
1. Disable AEB + DMS
   - moduleid : 327681, cmdid : 37 , payload (1 = ON, 2 = OFF) // AEB
   - moduleid : 327681, cmdid : 195 , payload (1 = ON, 2 = OFF) // DMS
