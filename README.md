# Lab2Web - Praktikum 2: HTML Lanjutan

Repositori ini dibuat untuk memenuhi tugas mata kuliah **Pemrograman Web** pada **Praktikum 2: HTML Lanjutan**.

---

## 👤 Data Mahasiswa
- **Nama** : Satrio Erlangga
- **NIM** : 312510006
- **Kelas** : I253C
- **Program Studi** : Teknik Informatika
- **Fakultas** : Teknik
- **Instansi** : Universitas Pelita Bangsa

---

## Struktur Folder

```text
Lab2Web/
├── index.html
├── biodata.html
├── README.md
└── media/
    ├── audio.mp3
    └── video.mp4
```

Langkah-Langkah Praktikum & Hasil Tampilan Web
1. Membuat Tabel Data Mahasiswa & Struktur Tabel
Membuat tabel sederhana serta mengembangkan tabel menggunakan struktur <thead>, <tbody>, <tfoot>, dan gabungan sel colspan.

 Kode (index.html):
<h3>Tabel Terstruktur (thead, tbody, tfoot)</h3>
<table border="1" cellpadding="5" cellspacing="0">
    <caption>Nilai Praktikum Web</caption>
    <thead>
        <tr>
            <th>No</th>
            <th>Nama</th>
            <th>Nilai</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Satrio Erlangga</td>
            <td>95</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Andi</td>
            <td>85</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2" align="center"><b>Rata-rata</b></td>
            <td><b>90</b></td>
        </tr>
    </tfoot>
</table>
Hasil Tampilan Web Browser:
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 182715" src="https://github.com/user-attachments/assets/09b3b8d3-06cf-4d09-927d-548ab187bb69" />

2. Membuat Form Registrasi & Jenis Input
Mengimplementasikan elemen <form> dengan berbagai jenis input (text, email, password, date), tombol radio button, checkbox, select dropdown, dan textarea.

 Kode (index.html):
<h2>2. Form Registrasi & Jenis Input</h2>
    
    <form action="#" method="POST">
        <!-- Input Text, Email, Password, Date -->
        <label for="nama">Nama Lengkap:</label><br>
        <input type="text" id="nama" name="nama"><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email"><br><br>

        <label for="password">Password:</label><br>
        <input type="password" id="password" name="password"><br><br>

        <label for="tanggal">Tanggal Lahir:</label><br>
        <input type="date" id="tanggal" name="tanggal"><br><br>

        <!-- Radio Button -->
        <label><b>Jenis Kelamin:</b></label><br>
        <input type="radio" id="laki" name="jk" value="L">
        <label for="laki">Laki-laki</label>
        <input type="radio" id="perempuan" name="jk" value="P">
        <label for="perempuan">Perempuan</label><br><br>

        <!-- Checkbox -->
        <label><b>Keahlian:</b></label><br>
        <input type="checkbox" id="html" name="skill" value="HTML">
        <label for="html">HTML</label>
        <input type="checkbox" id="css" name="skill" value="CSS">
        <label for="css">CSS</label>
        <input type="checkbox" id="js" name="skill" value="JavaScript">
        <label for="js">JavaScript</label><br><br>

        <!-- Select & Textarea -->
        <label for="prodi">Program Studi:</label><br>
        <select id="prodi" name="prodi">
            <option value="">-- Pilih Prodi --</option>
            <option value="ti">Teknik Informatika</option>
            <option value="si">Sistem Informasi</option>
        </select><br><br>

        <label for="alamat">Alamat:</label><br>
        <textarea id="alamat" name="alamat" rows="4" cols="40"></textarea><br><br>

        <button type="submit">Daftar</button>
        <button type="reset">Reset</button>
    </form>
Hasil Tampilan Web Browser:
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 183024" src="https://github.com/user-attachments/assets/59f94a43-777c-4431-ac97-5a2c1a95befb" />

3. Validasi Form Dasar
Menerapkan validasi form bawaan HTML menggunakan atribut required, minlength, min, dan max pada elemen input.

 Kode (index.html):
<h2>3. Latihan Validasi Form</h2>
    
    <form action="#" method="POST">
        <label for="val_nama">Nama (Min 3 Karakter):</label><br>
        <input type="text" id="val_nama" name="nama" required minlength="3"><br><br>

        <label for="val_email">Email (Wajib Format Email):</label><br>
        <input type="email" id="val_email" name="email" required><br><br>

        <label for="val_umur">Umur (17 - 60 Tahun):</label><br>
        <input type="number" id="val_umur" name="umur" min="17" max="60" required><br><br>

        <button type="submit">Kirim Form</button>
    </form>
Hasil Tampilan Web Browser (Pesan Validasi):
<img width="957" height="506" alt="Cuplikan layar 2026-10-03 183905" src="https://github.com/user-attachments/assets/400f1cf4-01c9-4703-bb61-4890b6aca8dd" />

4. Semantic HTML & Elemen Multimedia
Menggunakan struktur elemen semantic (<header>, <nav>, <main>, <section>, <aside>, <footer>) serta menambahkan media pemutar audio <audio> dan video <video>.

 Kode (index.html):
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Portal Mahasiswa - Semantic & Multimedia</title>
</head>
<body>

    <!-- Semantic Header & Nav -->
    <header>
        <h1>Portal Mahasiswa - Praktikum 2</h1>
    </header>
    
    <nav>
        <a href="index.html">Beranda</a> |
        <a href="biodata.html">Biodata (Proyek Mini)</a>
    </nav>
    <hr>

    <!-- Semantic Main -->
    <main>
        <section id="multimedia">
            <h2>Elemen Multimedia</h2>
            
            <h3>Audio</h3>
            <audio controls>
                <source src="media/audio.mp3" type="audio/mpeg">
                Browser tidak mendukung audio.
            </audio>

            <h3>Video</h3>
            <video controls width="480">
                <source src="media/video.mp4" type="video/mp4">
                Browser tidak mendukung video.
            </video>
        </section>
    </main>

    <!-- Semantic Aside -->
    <aside>
        <p><b>Informasi:</b> Praktikum 2 difokuskan pada Semantic HTML dan Multimedia.</p>
    </aside>

    <!-- Semantic Footer -->
    <footer>
        <p>&copy; 2026 Teknik Informatika - Universitas Pelita Bangsa</p>
    </footer>

</body>
</html>
Hasil Tampilan Web Browser:
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 185334" src="https://github.com/user-attachments/assets/9d7b90c6-d547-4247-9db9-452f846e421d" />
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 185814" src="https://github.com/user-attachments/assets/96859f65-d2a1-4bfc-8368-0269180b91a8" />

5. Proyek Mini - Form Biodata Mahasiswa (biodata.html)
Menggabungkan seluruh elemen (Tabel, Form, Validasi, Semantic HTML, dan Multimedia) ke dalam satu proyek halaman Biodata Mahasiswa.

 Kode  (biodata.html):
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Proyek Mini - Biodata Mahasiswa</title>
</head>
<body>

    <header>
        <h1>Biodata Mahasiswa</h1>
    </header>

    <nav>
        <a href="index.html">Beranda</a> |
        <a href="#biodata">Biodata</a> |
        <a href="#form">Form Edit</a>
    </nav>
    <hr>

    <main>
        <!-- Section Tabel Data -->
        <section id="biodata">
            <h2>Data Mahasiswa</h2>
            <table border="1" cellpadding="8" cellspacing="0">
                <tr>
                    <th>Data</th>
                    <th>Keterangan</th>
                </tr>
                <tr>
                    <td>NIM</td>
                    <td>312510006</td>
                </tr>
                <tr>
                    <td>Nama</td>
                    <td>Satrio Erlangga</td>
                </tr>
                <tr>
                    <td>Program Studi</td>
                    <td>Teknik Informatika</td>
                </tr>
                <tr>
                    <td>Kelas</td>
                    <td>TI.25.C.1</td>
                </tr>
            </table>
        </section>

        <br>

        <!-- Section Form -->
        <section id="form">
            <h2>Form Update Biodata</h2>
            <form action="#" method="POST">
                <label for="nama">Nama Lengkap:</label><br>
                <input type="text" id="nama" name="nama" required minlength="3"><br><br>

                <label for="email">Email:</label><br>
                <input type="email" id="email" name="email" required><br><br>

                <label for="prodi">Program Studi:</label><br>
                <select id="prodi" name="prodi" required>
                    <option value="">-- Pilih --</option>
                    <option value="ti">Teknik Informatika</option>
                    <option value="si">Sistem Informasi</option>
                </select><br><br>

                <label for="alamat">Alamat:</label><br>
                <textarea id="alamat" name="alamat" rows="4" cols="40" required></textarea><br><br>

                <button type="submit">Simpan</button>
                <button type="reset">Reset</button>
            </form>
        </section>

        <br>

        <!-- Section Audio -->
        <section id="media-biodata">
            <h2>Media Perkenalan</h2>
            <audio controls>
                <source src="media/audio.mp3" type="audio/mpeg">
                Browser Anda tidak mendukung elemen audio.
            </audio>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Teknik Informatika - Universitas Pelita Bangsa</p>
    </footer>

</body>
</html>
Hasil Tampilan Web Browser (biodata.html):
<img width="957" height="504" alt="Cuplikan layar 2026-10-03 191101" src="https://github.com/user-attachments/assets/397ea8c0-6385-4074-9a90-badc37dbd42a" />


Jawaban Pertanyaan Modul
Apa fungsi <table>, <tr>, <th>, dan <td>?

<table>: Elemen pembungkus utama untuk membuat tabel.

<tr> (Table Row): Membuat baris pada tabel.

<th> (Table Header): Membuat sel judul/header kolom (teks dicetak tebal dan rata tengah).

<td> (Table Data): Membuat sel untuk menampung data pada baris tabel.

Apa perbedaan <th> dan <td>?

<th> ditujukan untuk judul/header kolom, sehingga teksnya secara otomatis dicetak tebal (bold) dan diposisikan di tengah (center).

<td> ditujukan untuk isi data tabel biasa, sehingga teksnya ditampilkan dengan bobot normal dan rata kiri (left).

Apa fungsi colspan pada tabel?

Atribut colspan (column span) berfungsi untuk menggabungkan dua atau lebih kolom horizontal menjadi satu sel tabel.

Apa fungsi <form> dalam HTML?

Tag <form> berfungsi sebagai kontainer atau wadah untuk menampung berbagai komponen elemen input yang digunakan untuk menerima masukan data dari pengguna dan mengirimkannya ke server.

Apa perbedaan radio button dan checkbox?

Radio Button (type="radio"): Hanya memungkinkan pengguna memilih satu pilihan saja dari sebuah kelompok opsi.

Checkbox (type="checkbox"): Memungkinkan pengguna memilih satu, beberapa, atau seluruh pilihan sekaligus.

Mengapa <label> sebaiknya terhubung dengan id input melalui atribut for?

Menghubungkan atribut for pada label dengan id pada input bertujuan untuk meningkatkan aksesibilitas dan kemudahan navigasi. Pengguna cukup mengklik teks label untuk langsung mengaktifkan/mengarahkan kursor ke kotak input yang bersangkutan.

Apa perbedaan <textarea> dengan input type="text"?

input type="text" digunakan untuk menerima masukan teks pendek dalam satu baris tunggal (single line).

<textarea> digunakan untuk menerima masukan teks panjang yang terdiri dari beberapa baris (multi-line), seperti alamat atau catatan.

Apa fungsi semantic HTML seperti <header>, <nav>, <main>, <section>, <article>, <aside>, dan <footer>?

Memberikan struktur dan makna yang jelas pada halaman web, memudahkan mesin pencari (Search Engine) memahami konten, serta membantu pembaca layar (screen reader) dalam menavigasi halaman.

Apa fungsi required, min, max, dan minlength?

required: Menandai bahwa kolom input wajib diisi sebelum form dapat dikirim.

min: Menentukan nilai angka/tanggal terkecil yang diizinkan.

max: Menentukan nilai angka/tanggal terbesar yang diizinkan.

minlength: Menentukan jumlah karakter teks minimum yang wajib dimasukkan pengguna.

Apa perbedaan elemen <audio> dan <video>?

Tag <audio> digunakan untuk menyematkan dan memutar berkas suara/musik (contoh: .mp3).

Tag <video> digunakan untuk menyematkan dan memutar berkas video/visual bergerak beserta suaranya (contoh: .mp4).
