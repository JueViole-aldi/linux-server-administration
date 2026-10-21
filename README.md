# 🐧 Linux (Ubuntu Server) Administration — Lab Documentation

Repositori ini mendokumentasikan praktik administrasi sistem operasi **Linux** berbasis baris perintah (*Command Line Interface* / CLI) yang mencakup pengelolaan *user/permissions*, pemantauan penyimpanan, analisis *log*, pencadangan data (*backup*), hingga pengamanan akses server.

---

## 1. Manajemen Pengguna, Grup & Hak Akses File (Users & Permissions)
* **Skenario Industri:** Mengatur otorisasi akun staf per divisi dan mengamankan direktori kerja di server agar hanya dapat diakses atau dimodifikasi oleh pengguna yang berwenang.
* **Perintah CLI Utama:**
  * Pembuatan User & Grup: `sudo adduser`, `sudo groupadd`, `sudo usermod -aG`
  * Pengaturan Izin Akses & Kepemilikan: `chmod` (Octal/Symbolic) dan `chown`

<!-- Besok setelah upload gambar bernama linux-permissions.png, hapus tanda panah komentar di baris bawah ini: -->
<!-- ![Manajemen User dan Permissions Linux](linux-permissions.png) -->

---

## 2. Manajemen Paket Aplikasi & Pemantauan Kapasitas Penyimpanan (Disk Monitoring)
* **Skenario Industri:** Memelihara pembaruan perangkat lunak server melalui repositori resmi serta memantau ketersediaan ruang penyimpanan (*disk space*) dan struktur partisi untuk mencegah server berhenti beroperasi akibat penyimpanan penuh.
* **Perintah CLI Utama:**
  * Manajemen Paket: `sudo apt update && sudo apt upgrade`, `sudo apt install`
  * Cek Penyimpanan & Partisi: `df -h`, `du -sh`, `lsblk`

<!-- Besok setelah upload gambar bernama linux-apt-disk.png, hapus tanda panah komentar di baris bawah ini: -->
<!-- ![Manajemen Paket dan Disk Linux](linux-apt-disk.png) -->

---

## 3. Investigasi Masalah Sistem Melalui System Logs (`syslog` & Process Management)
* **Skenario Industri:** Melakukan *troubleshooting* layanan server yang mengalami kendala dengan memeriksa catatan sistem (*log files*) secara langsung serta memantau penggunaan sumber daya CPU/RAM.
* **Perintah CLI Utama:**
  * Analisis Log: `cat /var/log/syslog`, `tail -f /var/log/syslog`, `journalctl -xe`, `grep`
  * Manajemen Proses: `top`, `ps aux`, `kill`

<!-- Besok setelah upload gambar bernama linux-syslog.png, hapus tanda panah komentar di baris bawah ini: -->
<!-- ![Analisis Syslog dan Proses Linux](linux-syslog.png) -->

---

## 4. Prosedur Backup Data, Remote Access (SSH) & Konfigurasi Firewall (UFW)
* **Skenario Industri:** Mengamankan operasional server melalui kendali jarak jauh terenkripsi (**OpenSSH**), membatasi port jaringan yang terbuka menggunakan **Uncomplicated Firewall (UFW)**, serta menjalankan pencadangan (*backup*) direktori penting secara terkompresi.
* **Perintah CLI Utama:**
  * Pengamanan Jaringan & SSH: `sudo ufw allow ssh`, `sudo ufw enable`, `sudo ufw status verbose`, `/etc/ssh/sshd_config`
  * Arsip & Backup Data: `tar -czvf`, `rsync`

<!-- Besok setelah upload gambar bernama linux-ssh-ufw-backup.png, hapus tanda panah komentar di baris bawah ini: -->
<!-- ![SSH Firewall UFW dan Backup Linux](linux-ssh-ufw-backup.png) -->
