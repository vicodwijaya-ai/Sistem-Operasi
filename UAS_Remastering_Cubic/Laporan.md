# UAS REMASTERING CUBIC 

<h4>Nama : Vico Dwi Wijaya<h4>
<h4>NIM  : 254107020259<h4>
<h4>Kelas: TI-1H<h4>
<h4>Absen: 28<h4>

## Tugas Proyek:
1. Persiapan Sistem Dasar

    * Siapkan file ISO Ubuntu versi LTS (Long Term Support) terbaru.
    * Gunakan tool remastering pilihan Anda (sangat disarankan menggunakan Cubic).

2. Kustomisasi dan Instalasi Aplikasi
    Pasang beberapa aplikasi berikut ke dalam sistem yang sedang di-remaster:

    * VLC Media Player (Pemutar multimedia)
    * GIMP (Editor gambar)
    * Apache2 + PHP (Web server lokal)
    ```
    apt update
    ```
    ![alt text](<image/Screenshot 2026-06-13 103101.png>)

    ```
    apt install vlc gimp apache2 php -y
    ```
    ![alt text](<image/Screenshot 2026-06-13 102834.png>)
    ![alt text](<image/Screenshot 2026-06-13 102253.png>)
    
    * Visual Studio Code (Code editor)
    ```
    wget -O vscode.deb 'https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64'
    ```
    ![alt text](image/image-1.png)
    
    ```
    apt install ./vscode.deb -y
    ```
    ![alt text](image/image-2.png)

    ```
    rm vscode.deb
    ```
    ![alt text](image/image-3.png)
    
    * Aplikasi Kustom Buatan Sendiri: Buat sebuah program sederhana berbasis Bash Script yang berfungsi untuk menampilkan informasi dasar perangkat keras komputer, meliputi:

        * Informasi Prosesor (CPU)
        * Kapasitas dan Penggunaan Memori (RAM)
        * Kapasitas Ruang Penyimpanan (Storage)
    
    ## Membuat Aplikasi Kustom (Bash Script) Info Hardware.

    1. Buat dan buka file programnya:
    ```
    nano /usr/local/bin/info-hardware
    ```
    2. Kode Bash Script-nya:
    ```
    #!/bin/bash
    echo "====================================="
    echo "      INFORMASI HARDWARE SISTEM      "
    echo "====================================="
    echo ""
    echo "[1] Informasi Prosesor (CPU):"
    lscpu | grep "Model name"
    echo ""
    echo "[2] Kapasitas dan Penggunaan Memori (RAM):"
    free -h
    echo ""
    echo "[3] Kapasitas Ruang Penyimpanan (Storage):"
    df -h /
    echo "====================================="
    ```
    ![alt text](image/image-4.png)

    3. Berikan izin eksekusi
    ```
    chmod +x /usr/local/bin/info-hardware
    ```
    ![alt text](image/image-5.png)

    4. Cara cek berhasil atau tidak
    ```
    info-hardware
    ```
    ![alt text](image/image-6.png)


3. Kustomisasi Tampilan (Antarmuka)

    Ubah visual atau estetika pada Desktop Environment bawaan, yang mencakup perubahan pada:
    * Wallpaper (Latar belakang desktop)
    ```
    wget -O /usr/share/backgrounds/wallpaper-kustom.jpg 'https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=1920&auto=format&fit=crop'
    ```
    ![alt text](image/image-8.png)

    * Tema sistem (Theme) -> UNTUK MELAKUKAN KUSTOMISASI TAMPILAN  SEBAIKNYA INSTALL TEMA DAN PAKET DULU AGAR BERHASIL
    * Paket ikon (Icons pack)
    Ini install tema dan paket ikon perintah seperti ini
    ```
    apt install arc-theme papirus-icon-theme -y
    ```
    ![alt text](image/image-7.png)

    #### Untuk cek Keberhasilan:
    ```
    ls /usr/share/backgrounds/
    ```
    ![alt text](image/image-9.png)




    ![alt text](image/image-10.png)

    

    #### Setelah selesai klik next dan tunggu loading
    ![alt text](image/image-11.png)
    ![alt text](image/image-12.png)
    ![alt text](image/image-13.png)
    ![alt text](image/image-14.png)

4. Pembuatan File ISO Baru
    Lakukan proses build atau generate untuk menghasilkan file ISO baru hasil modifikasi Anda, lalu beri nama dengan format: Ubuntu-Custom-[NIM].iso (Ganti [NIM] dengan Nomor Induk Mahasiswa Anda).
    ![alt text](image/image.png)
    ![alt text](image/image-15.png)

5. Pengujian dan Dokumentasi
    * Uji coba file ISO kustom yang telah jadi menggunakan emulator/perangkat virtual seperti VirtualBox atau QEMU.
    * Ambil tangkapan layar (screenshot) yang menunjukkan:
    1. Tampilan utama desktop yang telah diubah visualnya.
    2. Hasil eksekusi dari Bash script (aplikasi kustom informasi perangkat keras) yang telah Anda buat di dalam terminal.


    #### Sebelum Wallpaper

    ![alt text](image/image-19.png)
    ![alt text](image/image-24.png)

    #### Sesudah
    ![alt text](image/image-23.png)
    ![alt text](image/image-25.png)
    ![alt text](image/image-16.png)
    

    #### Sebelum
    ![alt text](image/image-20.png)

    #### Sesudah
    ![alt text](image/image-17.png)
    ![alt text](image/image-22.png)


    # CEK HASIL INSTALASI DARI PROJECT REMASTERING
    
    #### Visual Studio Code (Code editor)
    ![alt text](image/image-26.png)

    #### VLC Media Player (Pemutar multimedia)
    ![alt text](image/image-27.png)

    #### GIMP (Editor gambar)
    ![alt text](image/image31.png)

    #### Apache2 + PHP (Web server lokal)
    ![alt text](image/image-29.png)

    #### Tes Aplikasi Berbasis Bashscript
    ![alt text](image/image-30.png)

