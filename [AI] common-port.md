# Common Ports — CompTIA A+ 220-1201 (2.1)

## Abstrak
Dokumen ini membahas port TCP dan UDP yang umum digunakan dalam komunikasi
jaringan. Memahami port-port ini penting untuk troubleshooting masalah
komunikasi jaringan dan konfigurasi firewall, karena firewall sering
menggunakan nomor port sebagai kriteria mengizinkan atau memblokir lalu lintas.

## Tabel Port Penting

| Protokol | Port | Keterangan |
|---|---|---|
| FTP | TCP 20, 21 | 20 = transfer data aktif, 21 = kontrol/administrasi |
| SSH | TCP 22 | Komunikasi terenkripsi (pengganti Telnet) |
| Telnet | TCP 23 | Komunikasi tanpa enkripsi (tidak direkomendasikan) |
| SMTP | TCP 25 | Mengirim email antar server |
| DNS | UDP 53 | Menerjemahkan nama domain ke alamat IP |
| DHCP | UDP 67, 68 | Pemberian alamat IP otomatis |
| HTTP | TCP 80 | Web tanpa enkripsi |
| HTTPS | TCP 443 | Web terenkripsi |
| POP3 | TCP 110 | Menerima email |
| IMAP4 | TCP 143 | Menerima email dengan sinkronisasi folder |
| NetBIOS | UDP 137, TCP 139 | Penamaan dan sesi transfer file (Windows lama) |
| SMB / CIFS | TCP 445 | Berbagi file dan printer (Windows modern) |
| LDAP | TCP 389 | Akses layanan direktori |
| RDP | TCP 3389 | Remote desktop (terutama Windows) |

## Poin-Poin Penting
- FTP menggunakan TCP 20 untuk transfer data aktif dan TCP 21 untuk administrasi/kontrol.
- SSH menyediakan koneksi terenkripsi melalui TCP 22, sedangkan Telnet (TCP 23) tidak terenkripsi.
- SMTP menggunakan TCP 25 untuk mengirim pesan email antar server.
- DNS menggunakan UDP 53 untuk menerjemahkan FQDN menjadi alamat IP.
- DHCP menggunakan UDP 67 dan 68 untuk memberikan konfigurasi IP secara otomatis.
- HTTP (TCP 80) tidak terenkripsi, sementara HTTPS (TCP 443) terenkripsi.
- POP3 (TCP 110) menerima email; IMAP4 (TCP 143) menambahkan sinkronisasi folder antar klien.
- SMB (TCP 445) untuk transfer data Windows modern; versi lama memakai NetBIOS (UDP 137, TCP 139).
- LDAP (TCP 389) mengakses layanan direktori; LDAPS adalah versi amannya.
- RDP (TCP 3389) untuk akses dan kontrol desktop jarak jauh, terutama Windows.
