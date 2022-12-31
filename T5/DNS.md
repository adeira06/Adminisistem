# DNS

1. Buka akun debian pada virtualbox, lalu masukkan su untuk memasuki akun root dan masukkan sandi. ![Image](1.png)

2. Kemudian tulis nano /etc/network/interface untuk konfigurasi Network Interface yang saya gunakan pada Debian Server. ![Image](2.png)
  
3. Lalu atur juga file resolv.conf. ![Image](3.png)
![Image](31.png)
4. Setelah itu kita bias menginstall dns server di Debian, dengan cara “apt install bind9 dnsutils” dan tunggu selasai. ![Image](4.png)

5. Setelah terinstall kita bisa mengkonfigurasi sdn server dengan menuliskan “cd /etc/bind” lalu masukkan “nano named.conf.local”. ![Image](5.png)

6. Lalu edit dan tambahkan forward zone dan reverse zone pada file name.conf.local. ![Image](6.png)

7. Selanjutnya buat file db.aiaaja lalu edit file. ![Image](7.png)
![Image](71.png)

8. Langkah selanjutnya buat file db.192 lalu edit file. ![Image](8.png)
![Image](81.png)

9. Langkah selanjutnya buat file name.local.options lalu edit file. ![Image](9.png)

10. Edit file name.local.options lalu tambahkan IP DNS Server di bagian forwarders dan saya menggunakan IP Gateway dan IP DNS Public 8.8.8.8. ![Image](10.png)

11. Simpan konfigurasi file tersebut, lalu restart service DNS Server. ![Image](11.png)

12. Cek status DNS Server dan pastikan status service dalam keadaan active dan running. ![Image](12.png)

13. Selanjutnya jalankan perintah Nslookup untuk pengetesan ke nama domain pastikan hasilnya nama domain mengarah ke IP Address Server. ![Image](13.png)
  
14. Setelah tahapan installasi dan konfigurasi DNS Server selesai. Selanjutnya setting masuk pada bagian Network, lalu pada settingan DNS isi dengan IP Address Server. ![Image](14.png)

15. Selanjutnya lakukan test ping ke nama domain yang sebelumnya kita buat. Jika berhasil maka nama domain akan di terjemahkan ke IP Address Server yaitu 36.86.36.183 dan Lakukan juga test ping ke Internet, sebagai contoh disini saya ping ke facebook.com. ![Image](15.png)
![Image](151.png)

16. Konfigurasi Web Server dengan install Web Server, untuk aplikasi Web Server kita menggunakan Apache2. ![Image](16.png)
