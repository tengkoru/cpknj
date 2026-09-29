# SCP dan SFTP untuk mengunduh file via koneksi ssh

---

Cek juga bagian **Info tambahan** pada akhir dokumen ini.

--- 

## Server-PC

#### Install terlebih dahulu openssh ( Debian dan turunannya )
```
$ sudo apt update && apt install openssh-server 
```
#### Cek status ssh ( systemd )
``` 
$ sudo systemctl status ssh
```
Bila muncul **Active: active (running)** artinya service ssh sedang aktif<br>

#### Menjalankan service ssh ( systemd )
```
$ sudo systemctl enable --now ssh
```

#### Cek port 22 ( default port untuk ssh )
```
$ ss -tlnp | grep :22
```
Bila muncul **LISTEN 0 128 0.0.0.0:22** atau **LISTEN 0 128 [::]:22** artinya port 22 siap<br>

#### Cek alamat IP server
```
$ hostname -I
```
contoh : 192.168.9.74<br>

### Cek firewall apakah memblokir port 22 atau tidak

#### Cek firewall
```
$ sudo ufw status
```

#### mengizinkan port 22 untuk dipakai
```
$ sudo ufw allow 22/tcp
```
lalu coba cek kembali statusnya dengan perintah sebelumnya

## Client-PC

#### Install terlebih dahulu openssh ( Debian dan turunannya )
```
$ sudo apt install openssh 
```
#### Install terlebih dahulu openssh ( termux android )
```
$ pkg install openssh 
```

### SCP
Cocok dipakai jika kamu sudah tau persis lokasi file atau folder berada
#### Mengunduh langsung file dari lokasi
```
$ scp tengkoru@192.168.9.74:'~/Documents/koleksi buku/*' ~/Downloads/ 
```
#### Mengunduh langsung folder dari lokasi
```
$ scp -r tengkoru@192.168.9.74:'~/Documents/koleksi buku' ~/Downloads/
```
#### Mengunduh langsung dua atau lebih folder dari lokasi
```
$ scp -r tengkoru@192.168.9.74:'~/Documents/koleksi buku' tengkoru@192.168.9.74:'~/Pictures/screenshot' ~/Downloads/
```

### SFTP
Cocok dipakai bila ingin menjelajahi terlebih dahulu sebelum unduh file

#### Koneksi dengan server
```
$ sftp tengkoru@192.168.9.74
password: 
```

#### Contoh perintah terminal
```
sftp> ls
sftp> cd Documents
sftp>
sftp>
sftp> # perintah unduh file
sftp> get file.pdf
sftp> # perintah unduh semua file didalam lokasi terkini
sftp> get *
sftp> # perintah unduh folder
sftp> get -r 'koleksi buku'
```

### Info tambahan
Jika muncul pertanyaan seperti berikut:
```
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```
ketik **yes** lalu enter, kecuali Anda ingin membatalkan maka ketik **no** lalu enter.









