# Tugas Rumah Minggu 11 - CI untuk Repo Compose

**Nama:** [IMAM MAHDI JATIM]  
**NIM:** [202557201038]  
**Mata Kuliah:** [TEKNOLOGI OPEN SOURCE]

## Deskripsi Proyek
Proyek ini merupakan tugas praktik penerapan Continuous Integration (CI) menggunakan GitHub Actions untuk memvalidasi konfigurasi Docker Compose.

## Workflow CI
Workflow menggunakan GitHub Actions dengan tahapan:
1. Checkout repository.
2. Menyalin `.env.example` menjadi `.env`.
3. Menjalankan `docker compose config -q` untuk memvalidasi konfigurasi Compose.

Workflow berjalan ketika ada push ke branch `main` atau pull request.

## Status CI
![Compose Check](https://github.com/madi505/tugas-minggu11-ci-compose/actions/workflows/compose-check.yml/badge.svg)

## Bukti Praktik

### 1. Hasil CI Berhasil
![Run Hijau](bukti/1-run-hijau.png)

### 2. Pull Request dengan CI Gagal
![PR Merah](bukti/2-pr-merah.png)

### 3. Badge CI pada README
![Badge CI](bukti/3-badge.png)

## Link Pull Request
[Klik di sini untuk melihat Pull Request](ISI_LINK_PR_KAMU)

## Kendala dan Perbaikan
Kendala yang ditemukan adalah kesalahan indentasi pada file `docker-compose.yml` sehingga proses validasi CI gagal.

Perbaikan dilakukan dengan mengembalikan indentasi ke posisi yang benar. Setelah perubahan dikirim, proses CI berhasil berjalan kembali.

## Refleksi
Dari praktik ini, saya memahami cara membuat workflow GitHub Actions, melakukan validasi konfigurasi Docker Compose, serta mengetahui bagaimana CI mendeteksi kesalahan konfigurasi melalui Pull Request.
