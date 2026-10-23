# Pertemuan 10 - String dan Pengolahan Teks
- Nama: Tantri Widya Solehati
- NIM: 2225250114
- Kelas: 3F 
## Tujuan
Mengolah dan menormalisasi data teks dengan string Python.
## Cara Menjalankan
python3 tugas/normalisasi_data_mahasiswa.py
## Algoritma
- Normalisasi Nama
Fungsi normalisasi_nama(nama) digunakan untuk merapikan nama.
    - strip() menghapus spasi di awal dan akhir teks.
    - split() memisahkan kata-kata dan sekaligus menghilangkan spasi yang berlebihan di antara kata.
    - " ".join(...) menggabungkan kembali kata-kata tersebut dengan satu spasi.
    - title() mengubah huruf pertama setiap kata menjadi huruf kapital.
- Normalisasi Kode Kelas
Fungsi normalisasi_kode(kode) digunakan untuk menyeragamkan format kode kelas.
    - strip() menghapus spasi di awal dan akhir.
    - upper() mengubah semua huruf menjadi huruf kapital.
    - split() memisahkan setiap bagian kode berdasarkan spasi.
    - "-".join(...) menggabungkan bagian-bagian tersebut menggunakan tanda hubung (-).
- Hubungan dengan Inisial
Setelah nama dinormalisasi, fungsi buat_inisial(nama) mengambil huruf pertama dari setiap kata.
## Test Case
| Input Nama            | Input Kode  | Hasil yang Diharapkan                | Hasil Aktual                         | Status |
|-----------------------|-------------|--------------------------------------|--------------------------------------|--------| 
| aan hendrayana        | pmat a 2026 | Aan Hendrayana | PMAT-A-2026 | AH    | Aan Hendrayana | PMAT-A-2026 | AH    | Sesuai |
| fATHIYYAH mUTHMAINNAH | kelas b     | Fathiyyah Muthmainnah | KELAS-B | FM | Fathiyyah Muthmainnah | KELAS-B | FM | Sesuai |
| BUDI                  | pmtk 01     | Budi | PMTK-01 | B                   | Budi | PMTK-01 | B                   | Sesuai |
| siti nur aisyah       | kelas c     | Siti Nur Aisyah | KELAS-C | SNA      | Siti Nur Aisyah | KELAS-C | SNA      | Sesuai |
## Refleksi 
- Permasalahan
Satu masalah teks yang dapat ditemukan adalah adanya spasi berlebih pada nama yang dimasukkan pengguna.
Contoh masalah:
```Python
" ahmad fauzi "
```
Jika tidak diperbaiki, nama menjadi tidak rapi karena terdapat banyak spasi di awal, akhir, dan di antara kata.
- Cara memperbaikinya:
Program menggunakan fungsi normalisasi_nama():
```Python
def normalisasi_nama(nama):
return " ".join(nama.strip().split()).title()
strip() menghapus spasi di awal dan akhir.
split() memisahkan kata dan menghilangkan spasi berlebih.
" ".join() menggabungkan kembali kata-kata dengan satu spasi.
title() membuat huruf pertama setiap kata menjadi kapital.
```
Hasil setelah diperbaiki:
```Python
Input : " ahmad fauzi "
Output : "Ahmad Fauzi"
```
Jadi, masalah teks berupa spasi yang berlebihan dan penulisan nama yang tidak rapi dapat diperbaiki dengan proses normalisasi nama sehingga hasilnya lebih bersih dan konsisten.