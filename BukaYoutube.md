## Cara Buka Youtube di HU tanpa alat tambahan

1. Pastikan mengerti dan paham apa itu ADB
2. Pastikan [ADB enable + WIFI connected](https://github.com/sl3per/OmodaE5Mod/blob/main/enableadbwifi.md) di HU 
3. Pastikan sudah install platform-tools (adb client) di laptop
4. Koneksikan HU dengan laptop (windows only) melalui kabel USB-A yang ada di console HU (bukan yang USB-C)
5. Download Firefox Lite, bisa dari apkcombo / apkpure atau semacamnya
6. adb push ke /data/local/tmp/ 
7. adb shell
8. pm install /data/local/tmp/[file apknya]
9. di homescreen HU akan muncul aplikasi Firefox, buka dan klik shortcut untuk youtube nya
![image](https://github.com/user-attachments/assets/cda63682-43cb-4569-a533-e17fbb144586)
