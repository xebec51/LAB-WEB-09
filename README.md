# Laboratorium Pemrograman Web (LAB-WEB-09) - Ganjil 2025
## Repositori Resmi Kelompok Asistensi Web-09

---

### 📋 Prasyarat

Sebelum memulai, pastikan Anda sudah:
1.  Memiliki akun **GitHub** ([github.com](https://github.com)).
2.  Menginstal **Git** di komputer Anda ([git-scm.com](https://git-scm.com/)).

### ⚙️ Konsep Alur Kerja (Fork & One-Branch-Per-Student)

Kita akan menggunakan alur kerja standar industri dengan sedikit penyesuaian untuk lab ini. Setiap praktikan akan memiliki "ruang kerja" sendiri yang terisolasi menggunakan **satu branch permanen** bernama NIM Anda.

* **Fork:** Anda membuat "salinan" pribadi dari repositori utama ini ke akun GitHub Anda.
* **Clone:** Anda mengunduh salinan (fork) tersebut ke komputer Anda.
* **Branch:** Anda membuat **satu branch saja** dengan nama **NIM Anda**. Branch ini akan digunakan untuk semua tugas selama satu semester.
* **Push:** Setiap minggu, Anda akan mengunggah tugas baru ke branch NIM Anda di repositori fork.
* **Pull Request (PR):** Anda akan membuat **satu Pull Request saja** di awal. Tugas-tugas mingguan berikutnya akan otomatis ditambahkan ke PR yang sudah ada tersebut setiap kali Anda melakukan `push`.

---

### 🚀 Alur Pengumpulan Tugas

Ikuti langkah-langkah berikut. Perhatikan mana yang hanya dilakukan sekali dan mana yang dilakukan setiap minggu.

#### Langkah 1: Pengaturan Awal (Hanya Dilakukan Sekali)

1.  **Fork Repositori:** Klik tombol **Fork** di pojok kanan atas halaman repositori utama: [https://github.com/xebec51/LAB-WEB-09](https://github.com/xebec51/LAB-WEB-09). Ini akan membuat salinan repositori ke akun GitHub Anda. 
2.  **Clone Repositori Fork Anda:** Buka terminal/Git Bash, lalu jalankan perintah `clone`. Ganti `YOUR_USERNAME` dengan username GitHub Anda.
    ```sh
    git clone https://github.com/YOUR_USERNAME/LAB-WEB-09.git
    ```
3.  **Masuk ke Folder Proyek:**
    ```sh
    cd LAB-WEB-09
    ```
4.  **Buat Branch Permanen Anda:** Buat dan langsung pindah ke branch baru dengan nama NIM Anda. Anda bisa menggunakan salah satu dari dua opsi di bawah ini.

    <details>
    <summary><strong>Opsi 1: Perintah Singkat (Direkomendasikan)</strong></summary>

    Gunakan perintah `git checkout -b <nama-branch>`. Flag `-b` adalah singkatan dari `--branch`, yang merupakan perintah untuk **membuat branch baru dan langsung berpindah** ke branch tersebut dalam satu langkah.
    ```sh
    # Contoh menggunakan NIM
    git checkout -b H071241001
    ```
    </details>

    <details>
    <summary><strong>Opsi 2: Perintah Dua Langkah (Untuk Pemahaman)</strong></summary>

    Jika Anda ingin memahami prosesnya secara terpisah, Anda bisa menggunakan dua perintah:
    
    1.  **`git branch <nama-branch>`** untuk **membuat** branch baru.
        ```sh
        # Contoh menggunakan NIM
        git branch H071241001
        ```
    2.  **`git checkout <nama-branch>`** untuk **berpindah** ke branch yang sudah dibuat.
        ```sh
        # Contoh menggunakan NIM
        git checkout H071241001
        ```
    </details>
    
    > **Catatan:** Kedua opsi di atas menghasilkan hal yang sama. Anda hanya perlu memilih salah satu. Anda akan selalu bekerja di branch ini selama sisa semester.

#### Langkah 2: Alur Kerja Mingguan (Dilakukan Setiap Praktikum)

1.  **Pastikan Anda di Branch yang Benar:** Sebelum mulai, pastikan Anda sudah berada di branch NIM Anda.
    ```sh
    # Contoh menggunakan NIM Anda
    git checkout H071241001
    ```
2.  **Buat Folder Pribadi & Tugas:**
    * Buat folder dengan format **`NIM_NamaLengkap`** jika belum ada.
    
        > **PENTING: Aturan Penamaan Folder Nama**
        > Untuk `NamaLengkap`, hilangkan semua spasi dan gunakan huruf kapital di awal setiap kata. Teknik penamaan ini disebut **PascalCase** (atau *UpperCamelCase*). Ini adalah praktik umum dalam pemrograman untuk memastikan nama folder dan file mudah dibaca oleh sistem dan tidak menyebabkan eror.
        >
        > **Contoh yang Benar:** `H071241001_MuhRinaldiRuslan`
        > **Contoh yang Salah:** `H071241001_Muh Rinaldi Ruslan` (menggunakan spasi)

    * Di dalam folder pribadi Anda (`NIM_NamaLengkap`), buat folder tugas baru untuk minggu ini dengan format **`Tugas_XX`** (contoh: `Tugas_01`, `Tugas_02`, dst.).

    Struktur folder Anda akan terus bertambah setiap minggunya:
    ```
    .
    ├── H071231074_MuhRinaldiRuslan/
    │   ├── Tugas_01/
    │   │   ├── index.html
    │   │   └── style.css
    │   ├── Tugas_02/
    │   │   └── ... (file tugas minggu kedua)
    │   └── Tugas_03/
    │       └── ... (dan seterusnya)
    │
    └── README.md
    ```
3.  **Kerjakan Tugas Anda** di dalam folder yang baru dibuat.

#### Langkah 3: Proses Mengumpulkan Tugas (Dilakukan Setiap Minggu)

1.  **Simpan & Commit Perubahan:**
    ```sh
    # Tambahkan semua file yang baru atau berubah
    git add .

    # Commit dengan pesan yang jelas sesuai tugas minggu ini
    git commit -m "[NIM_ANDA] Mengumpulkan Tugas 02"
    ```
2.  **Push ke Branch Anda di Fork:**
    ```sh
    # Contoh menggunakan NIM
    git push origin H071241001
    ```
3.  **Buat atau Perbarui Pull Request:**
    * **Jika ini adalah pengumpulan PERTAMA Anda:** Buka halaman fork Anda di GitHub. Klik **"Compare & pull request"**, beri judul `Pengumpulan Tugas - NIM_Nama Lengkap`, lalu buat Pull Request.
    * **Untuk minggu-minggu BERIKUTNYA:** Anda **TIDAK PERLU** membuat Pull Request baru. Cukup lakukan `push` seperti pada langkah 3.2, dan commit terbaru Anda akan otomatis ditambahkan ke Pull Request yang sudah ada.

---

### ⚠️ Aturan Penting & Praktik Terbaik

* **Satu Praktikan, Satu Branch.** Seluruh pekerjaan selama satu semester dilakukan di dalam branch NIM Anda.
* **Satu Praktikan, Satu Pull Request.** Jangan pernah menutup PR Anda sampai akhir semester, kecuali diinstruksikan.
* **Gunakan Penamaan PascalCase** untuk folder nama Anda.
* **Commit Message Jelas:** Gunakan format `[NIM] Aksi yang dilakukan` agar mudah dilacak.

<details>
<summary>👉 <strong>Klik di sini jika butuh bantuan tentang Personal Access Token (PAT)</strong></summary>

Jika Git meminta *password* saat Anda melakukan `push`, Anda harus menggunakan **Personal Access Token (PAT)**, bukan password akun GitHub Anda.

**Cara Membuat PAT:**
1.  Buka **Settings** di profil GitHub Anda (pojok kanan atas).
2.  Scroll ke bawah, pilih **Developer settings** di menu kiri.
3.  Pilih **Personal access tokens** -> **Tokens (classic)**.
4.  Klik **Generate new token** -> **Generate new token (classic)**.
5.  **Note:** Beri nama token, misal: `Akses untuk Lab Web Unhas`.
6.  **Expiration:** Pilih durasi token (misal: 90 hari atau sampai akhir semester).
7.  **Select scopes:** Centang kotak **`repo`**. Ini memberikan izin penuh untuk repositori.
8.  Klik **Generate token**.
9.  **SIMPAN TOKEN!** Salin token yang muncul dan simpan di tempat yang aman. Token ini hanya akan muncul sekali. Jika hilang, Anda harus membuat yang baru.

</details>

<br>

Jika ada kendala, jangan ragu bertanya kepada Asisten kalian. Selamat mengerjakan!😇

Salam, <br><br>
**Naldi**<br>
Asisten Praktikum Web-09 Tahun 2025
