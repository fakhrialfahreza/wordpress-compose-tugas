docker compose bertujuan untuk mempermudah menjalankan dan mengatur beberapa container sekaligus menggunakan satu file konfigurasi, yaitu compose.yaml. WordPress membutuhkan database terpisah karena database digunakan untuk menyimpan data website
service db untuk menjalankan mariadb sebagai database,, sedangkan service wordpress menjalankan aplikasi wordpress dan mengelola website
image: untuk menentukan image docker yang digunakan, container_name: untuk memberi nama khusus pada container, ports: untuk menghubungkan port komputer dengan port container, environment: untuk menentukan variabel konfigurasi, depends_on: untuk mengatur ketergantungan antar service, volumes: untuk menyimpan data agar tidak hilang ketika conatiner dihentikan
Karena wordpress dan mariadb berjalan di container yang berbeda
env: untuk menyimpan konfigurasi asli, env.example: untuk menyediakan contoh format konfigurasi agar kita dapat mengetahui apa saja yang harus diisi, gitignore: menentukan file yang tidak perlu atau tidak boleh diunggah ke github
dalam percobaan tersebut membuktikan bahwa data pada wordpress tetap tersimpan meskipun container dihentikan dan dijalankan lagi
sedikit masalah yang saya temui adalah ketika saya mengatur file file tersebut dan harus ada file apa saja yang isinya diperlukan yang membuat saya sedikit bingung
tidak ada modifikasi yang saya tambahkan