# Lab2Web - Praktikum 2: HTML Lanjutan

Repositori ini dibuat untuk memenuhi tugas mata kuliah **Pemrograman Web** pada **Praktikum 2: HTML Lanjutan**.

---

## 👤 Data Mahasiswa
- **Nama** : Satrio Erlangga
- **NIM** : 312510006
- **Kelas** : TI.25.C.1
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
HTML
<form action="#" method="POST">
    <label for="nama_reg">Nama Lengkap:</label><br>
    <input type="text" id="nama_reg" name="nama"><br><br>

    <label for="email_reg">Email:</label><br>
    <input type="email" id="email_reg" name="email"><br><br>

    <label><b>Jenis Kelamin:</b></label><br>
    <input type="radio" id="laki" name="jk" value="L"> <label for="laki">Laki-laki</label>
    <input type="radio" id="perempuan" name="jk" value="P"> <label for="perempuan">Perempuan</label><br><br>

    <label><b>Keahlian:</b></label><br>
    <input type="checkbox" id="html" name="skill" value="HTML"> <label for="html">HTML</label>
    <input type="checkbox" id="css" name="skill" value="CSS"> <label for="css">CSS</label><br><br>

    <label for="prodi_reg">Program Studi:</label><br>
    <select id="prodi_reg" name="prodi">
        <option value="">-- Pilih Prodi --</option>
        <option value="ti">Teknik Informatika</option>
    </select><br><br>

    <label for="alamat_reg">Alamat:</label><br>
    <textarea id="alamat_reg" name="alamat" rows="4" cols="40"></textarea><br><br>

    <button type="submit">Daftar</button>
</form>
Hasil Tampilan Web Browser:
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 183024" src="https://github.com/user-attachments/assets/59f94a43-777c-4431-ac97-5a2c1a95befb" />

3. Validasi Form Dasar
Menerapkan validasi form bawaan HTML menggunakan atribut required, minlength, min, dan max pada elemen input.

 Kode (index.html):
HTML
<form action="#" method="POST">
    <label for="val_nama">Nama (Min 3 Karakter):</label><br>
    <input type="text" id="val_nama" name="nama" required minlength="3"><br><br>

    <label for="val_email">Email (Wajib Diisi):</label><br>
    <input type="email" id="val_email" name="email" required><br><br>

    <label for="val_umur">Umur (17 - 60 Tahun):</label><br>
    <input type="number" id="val_umur" name="umur" min="17" max="60" required><br><br>

    <button type="submit">Kirim Form (Uji Validasi)</button>
</form>
Hasil Tampilan Web Browser (Pesan Validasi):
<img width="957" height="506" alt="Cuplikan layar 2026-10-03 183905" src="https://github.com/user-attachments/assets/400f1cf4-01c9-4703-bb61-4890b6aca8dd" />

4. Semantic HTML & Elemen Multimedia
Menggunakan struktur elemen semantic (<header>, <nav>, <main>, <section>, <aside>, <footer>) serta menambahkan media pemutar audio <audio> dan video <video>.

 Kode (index.html):
HTML
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
Hasil Tampilan Web Browser:
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 185334" src="https://github.com/user-attachments/assets/9d7b90c6-d547-4247-9db9-452f846e421d" />
<img width="959" height="503" alt="Cuplikan layar 2026-10-03 185814" src="https://github.com/user-attachments/assets/96859f65-d2a1-4bfc-8368-0269180b91a8" />

5. Proyek Mini - Form Biodata Mahasiswa (biodata.html)
Menggabungkan seluruh elemen (Tabel, Form, Validasi, Semantic HTML, dan Multimedia) ke dalam satu proyek halaman Biodata Mahasiswa.

 Kode  (biodata.html):
HTML
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
        <section id="biodata">
            <h2>Data Mahasiswa</h2>
            <table border="1" cellpadding="8" cellspacing="0">
                <tr><th>Data</th><th>Keterangan</th></tr>
                <tr><td>NIM</td><td>312510006</td></tr>
                <tr><td>Nama</td><td>Satrio Erlangga</td></tr>
                <tr><td>Program Studi</td><td>Teknik Informatika</td></tr>
            </table>
        </section>

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
            </form>
        </section>

        <section id="media-biodata">
            <h2>Media Perkenalan</h2>
            <audio controls>
                <source src="media/audio.mp3" type="audio/mpeg">
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
