Kegunaan:

Kode ini dibuat untuk menghasilkan daftar alamat IP secara masal (massive IP range generation) berdasarkan input daftar IP dasar (3 oktet pertama). Biasanya ini digunakan untuk keperluan seperti:

🔎 Network scanning: Misalnya, kamu ingin memindai (scan) seluruh IP dalam subnet tertentu untuk mencari perangkat aktif, layanan terbuka, atau potensi celah keamanan.

🗺️ Pemetaan jaringan (network mapping): Membantu membuat daftar IP lengkap dari beberapa subnet.

🧪 Pengujian otomatis: Misalnya untuk simulasi, testing aplikasi jaringan, atau monitoring.

⚙️ Otomatisasi proses IT/networking: Memudahkan pembuatan list IP tanpa harus mengetik satu per satu.

Fungsi Utama Kode:

1. Membaca file input berisi daftar IP dasar (contoh: 192.168.1, 10.0.0).
2. Membuat rentang IP lengkap dengan oktet terakhir dari 0 sampai 255 untuk setiap IP dasar tersebut, sehingga membentuk subnet lengkap.
3. Menyimpan hasil rentang IP ke dalam file Results/ip_range.txt.
4. Memproses pembuatan rentang IP secara paralel menggunakan multiple thread, sehingga mempercepat eksekusi ketika ada banyak IP dasar.

📌 Ciri Khas Tool Ini (apa yang membuatnya unik)

Input sederhana berbasis 3‑oktet → fokus pada subnet /24.

Mode append: menambahkan ke Results/ip_range.txt, sehingga hati‑hati kalau menjalankan berulang (bisa duplikat).

Threaded: melakukan pekerjaan paralel (lebih cepat), cocok untuk I/O-bound tasks.

Tidak melakukan probing: script hanya membuat daftar IP — alat lain yang melakukan scanning. Itu membuatnya aman (lebih ringan) tapi berguna sebagai komponen pipeline.

Tampilannya ramah: banner dan warna (colorama) membuat interaksi lebih enak.

Tanpa validasi ketat: cepat, tapi silent fail kalau input salah — sulit dimonitor kalau ada error.

