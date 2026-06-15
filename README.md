CodeAlpha: Basic Network Sniffer (Task 1)

Sebuah program penganalisis paket jaringan (network packet sniffer) berbasis Python yang tangguh dan interaktif. Aplikasi ini dikembangkan untuk menangkap, mengurai (parsing), dan menganalisis lalu lintas data jaringan lokal secara real-time guna mempelajari arsitektur protokol jaringan.

Proyek ini dibuat untuk memenuhi persyaratan Task 1 pada Program Magang Cyber Security di CodeAlpha.

📋 Prasyarat & Kebutuhan Sistem

Aplikasi ini membutuhkan akses soket mentah (raw socket access), sehingga harus dijalankan dengan hak akses administrator/root.

1. Kebutuhan Perangkat Keras & Lunak

Sistem Operasi: Linux (Sangat direkomendasikan), macOS, Windows, atau Android (menggunakan Termux).

Python: Versi 3.8 atau yang lebih baru.

Hak Akses: Root / Sudo (pada Linux/macOS) atau Administrator (pada Windows).

2. Dependensi Python (Libraries)

Aplikasi ini memanfaatkan pustaka-pustaka berikut:

Scapy: Mesin utama untuk melakukan manipulasi dan penangkapan paket data.

Colorama: Untuk memberikan pewarnaan visual (syntax highlighting) pada terminal konsol agar mudah dibaca.

🛠️ Langkah-Langkah Instalasi

Jalur A: Di PC (Linux / Ubuntu / Debian)

Instalasi Dependensi Sistem:

sudo apt update
sudo apt install python3 python3-pip -y


Instalasi Pustaka Python:

pip3 install scapy colorama


Jalur B: Di Handphone (Android via Termux)

Instalasi Paket Dasar di Termux:

pkg update && pkg upgrade -y
pkg install python python-pip git -y


Instalasi Scapy & Dependensi:

pip install scapy colorama


Catatan: Menjalankan sniffer pada Termux memerlukan perangkat Android yang sudah di-root untuk dapat mengakses kartu jaringan fisik (Wi-Fi/seluler).

🚀 Cara Menjalankan Program

Buka terminal atau CLI di folder tempat file basic_network_sniffer.py disimpan.

Jalankan program dengan perintah hak akses root:

sudo python3 basic_network_sniffer.py


Program akan mulai mendengarkan (listening) pada adapter jaringan aktif Anda.

Tekan tombol Ctrl + C di keyboard untuk menghentikan proses penangkapan. Setelah dihentikan, program akan secara otomatis mengekspor seluruh log paket yang tertangkap ke dalam file biner captured_traffic.pcap yang siap dibuka di Wireshark.

🛡️ Fitur Utama

Multi-Layer Parsing: Mampu membedah protokol Ethernet (Layer 2), IPv4 (Layer 3), serta TCP, UDP, dan ICMP (Layer 4).

Payload Hex-View: Dilengkapi dengan fitur pemindai payload data mentah (raw payload preview) yang aman.

Export PCAP: Otomatis menghasilkan berkas .pcap terstandardisasi setelah selesai merekam untuk analisis lanjutan.

Desain Konsol Interaktif: Menggunakan visualisasi warna interaktif untuk membedakan kategori protokol.

⚠️ Disclaimer (Peringatan Penting)

Aplikasi Network Sniffer ini dikembangkan murni untuk tujuan akademis, pembelajaran, dan edukasi dalam rangka magang di CodeAlpha. Menangkap lalu lintas data jaringan milik orang lain tanpa izin eksplisit adalah tindakan ilegal. Pengembang tidak bertanggung jawab atas segala bentuk penyalahgunaan program ini.
