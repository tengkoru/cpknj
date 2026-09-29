# Aturan kepenulisan didalam file .gitignore
---
### Buat file nya terlebih dahulu dengan perintah
```
touch .gitignore
```

### Kemudian edit file menggunakan perintah nano
```
nano .gitignore
```
---

Git akan membaca file .gitignore baris per baris. Berikut ini simbol dan aturan yang bisa digunakan

### Tanda bintang (*) sebagai wildcard
Mengabaikan semua file yang memiliki akhiran atau pola tertentu, di folder mana pun mereka berada.

contoh:
```
*.log
*.exe
*.o
*.pyc
```

### Garis Miring (/) di akhir nama
Mengabaikan folder (direktori) beserta semua isi file di dalamnya

contoh:
```
node_modules/
__pycache__/
.godot/
```

### Garis Miring (/) di awal nama
Mengabaikan file yang hanya berada tepat di folder utama (root) proyek, bukan yang didalam subfolder.

contoh: 
```
/config.json
```

###  Tanda Seru (!) sebagai pengecualian
Memaksa git tetap menyertakan file tertentu meskipun pada bagian sebelumnya terdapat pengecualian tertentu.

contoh:
```
*.log
!public.log
```

### Tanda Pagar (#) untuk komentar
Memberikan catatan/keterangan didalam .gitignore yang akan diabaikan oleh Git.

contoh:
```
# ini folder tempat menyimpan berbagai kebutuhan tambahan untuk aplikasi
.env/
```