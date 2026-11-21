# Project 01 — Network Reconnaissance Menggunakan Nmap

## 1. Deskripsi Proyek
Proyek ini merupakan praktik Network Reconnaissance menggunakan Nmap untuk mengidentifikasi port terbuka dan layanan jaringan pada sistem lokal.

Pengujian dilakukan terhadap komputer sendiri menggunakan alamat IP `127.0.0.1` sebagai target.

## 2. Tujuan
- Memahami konsep network reconnaissance.
- Mengidentifikasi port yang terbuka.
- Mendeteksi layanan yang berjalan pada port tertentu.
- Memahami penggunaan Nmap untuk analisis keamanan jaringan.

## 3. Tools yang Digunakan
- Kali Linux
- Nmap
- Python 3
- VirtualBox

## 4. Lingkungan Pengujian
| Komponen | Keterangan |
|---|---|
| Sistem Operasi | Kali Linux |
| Target | 127.0.0.1 |
| Port Pengujian | 8000 |
| Layanan | HTTP |
| Tools | Nmap |

## 5. Tahapan Pengujian

### A. Menjalankan Server Lokal
Menjalankan server HTTP sederhana menggunakan Python:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

### B. Melakukan Pemindaian
Menjalankan Nmap untuk memeriksa port 8000:

```bash
nmap -sV -p 8000 127.0.0.1 -oN scan-result.txt
```

### C. Memeriksa Hasil
Hasil pemindaian disimpan dalam file `scan-result.txt`.

## 6. Hasil Pengujian
Tuliskan hasil aktual dari pemindaian di sini, termasuk status port dan layanan yang terdeteksi.

Contoh:
- Port: 8000/tcp
- Status: open
- Layanan: HTTP

*Catatan: Sesuaikan hasil dengan output Nmap yang sebenarnya.*

## 7. Analisis Keamanan
Port yang terbuka menunjukkan adanya layanan yang menerima koneksi pada port tersebut.

Dalam konteks keamanan jaringan, port terbuka perlu dianalisis untuk memastikan layanan yang berjalan memang diperlukan dan dikonfigurasi dengan aman.

Pemindaian ini merupakan langkah awal dalam proses network reconnaissance yang dapat membantu analis keamanan memahami permukaan serangan suatu sistem.

## 8. Bukti Pengujian
Screenshot hasil pemindaian tersedia pada folder `screenshots/`.

## 9. Kesimpulan
Pengujian ini menunjukkan bagaimana Nmap dapat digunakan untuk mengidentifikasi port terbuka dan mendeteksi layanan pada sistem lokal. Praktik ini memberikan pemahaman dasar mengenai network reconnaissance yang merupakan salah satu keterampilan penting bagi seorang SOC Analyst.

## 10. Batasan Pengujian
Pengujian hanya dilakukan pada sistem lokal milik sendiri (`127.0.0.1`) untuk tujuan pembelajaran.

## Author
Cybersecurity Learning Portfolio — SOC Analyst Preparation 

-------------------------- ARWAN --------------------------
