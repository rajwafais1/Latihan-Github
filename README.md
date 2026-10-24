# Praktikum 3 - Access Modifier `protected` dan CRUD Mahasiswa

Implementasi modul praktikum Java menggunakan **tiga package**:

- `induk/Mahasiswa.java`: superclass, penyimpanan `ArrayList`, dan operasi Create, Read, Update, Delete.
- `anak/MahasiswaApp.java`: subclass dengan menu console.
- `gui/MahasiswaGUI.java`: subclass dengan tampilan Swing (`JFrame`, `JTextField`, `JButton`, `JTable`).

Kedua subclass memanggil method `protected` milik superclass dari package yang berbeda. GUI menggunakan komposisi `JFrame`, karena Java hanya mendukung single inheritance.

## Menjalankan dengan terminal (JDK 8 atau lebih baru)

Jalankan perintah berikut dari folder utama repository:

```bash
javac induk/Mahasiswa.java anak/MahasiswaApp.java gui/MahasiswaGUI.java
java anak.MahasiswaApp
```

Untuk menjalankan versi GUI, gunakan:

```bash
java gui.MahasiswaGUI
```

GUI membutuhkan komputer dengan lingkungan desktop (tidak dapat ditampilkan melalui terminal GitHub di iPhone).

## Menjalankan di NetBeans

1. Buat project Java Application baru.
2. Di dalam Source Packages, buat package `induk`, `anak`, dan `gui`.
3. Masukkan masing-masing file Java ke package yang sesuai.
4. Klik kanan `MahasiswaApp.java` lalu **Run File** untuk versi console, atau `MahasiswaGUI.java` lalu **Run File** untuk versi GUI.

## Cara pakai

- **Tambah**: masukkan nama lalu klik Tambah / pilih menu 1.
- **Lihat**: data ditampilkan dalam tabel GUI / menu 2.
- **Ubah**: pilih baris, ganti nama, lalu klik Ubah / menu 3.
- **Hapus**: pilih baris lalu klik Hapus / menu 4. Pada GUI akan muncul konfirmasi.

**Catatan:** data tersimpan sementara di `ArrayList`; data akan hilang saat aplikasi ditutup. Versi console dan GUI masing-masing punya daftar data di memori sendiri.
