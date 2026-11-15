# TestGen Agent

AI Agent pembuat test case otomatis dari requirement dan user story, dikembangkan dengan **IBM Bob**.
Capstone Project IBM x Hacktiv8 (IT Track, AI Agent).

## Ringkasan

TestGen Agent menerima requirement atau user story, lalu menghasilkan test case
terstruktur (positive, negative, boundary, edge case) dalam bentuk tabel yang siap dieksekusi.

## Problem Statement

Pembuatan test case manual lambat, formatnya tidak konsisten, dan skenario penting
seperti nilai batas dan input tidak valid mudah terlewat. Akibatnya bug lolos ke produksi.

## Target Users

QA engineer junior, developer yang merangkap penguji, dan mahasiswa Teknik Informatika.

## Arsitektur Prompt (5 Layer)

1. **Role**: QA Engineer senior berstandar ISTQB.
2. **Tujuan & Konteks**: mengubah requirement menjadi test case.
3. **Cara Kerja**: analisis requirement, terapkan EP/BVA/Decision Table, tangani ambiguitas.
4. **Format Output**: tabel dengan kolom ID, Kategori, Skenario, Precondition, Langkah,
   Data Uji, Expected Result, Prioritas.
5. **Batasan**: tidak menambah fitur atau mengarang aturan, fokus pada test case.

Prompt lengkap ada di file [`prompt.md`](prompt.md).

## Contoh Penggunaan

Input: requirement fitur Login (password 8-20 karakter, akun terkunci 15 menit
setelah 3x gagal login, ada checkbox Remember me).

Screenshot prompt dan hasil pengujian ada di folder [`screenshots/`](screenshots/).

## Cara Menjalankan

[Isi sesuai hasilnya. Contoh: buka `index.html` di browser. Kalau hanya prompt di IBM Bob,
tulis "Tempel prompt di prompt.md ke IBM Bob lalu masukkan requirement".]

## Iterasi Prompt

- **v1**: [prompt sederhana dan hasilnya]
- **v2**: [perubahan dan dampaknya]
- **v3**: [perubahan dan dampaknya]

## Pengembangan Lanjutan

Ekspor ke CSV atau Excel, integrasi dengan Jira atau TestRail, dukungan input dokumen PRD.

## Tim / Penulis

[Nama kamu]