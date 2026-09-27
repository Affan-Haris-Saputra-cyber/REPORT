# Panduan Pemakaian — Template Surat Responsible Disclosure

Template ini dipakai untuk melaporkan temuan kerentanan keamanan pada
aplikasi/sistem milik pihak lain secara **resmi, sopan, dan bertanggung
jawab**, sebelum informasi tersebut dipublikasikan atau jatuh ke tangan
yang salah. Model pelaporan seperti ini dikenal sebagai *Responsible
Disclosure* atau *Coordinated Vulnerability Disclosure (CVD)*.

Cocok dipakai untuk laporan hasil CTF eksternal (bug bounty tidak resmi),
temuan saat riset mandiri, atau saat magang/kerja di bidang keamanan
siber — sejalan dengan arah belajar CTF dan keamanan aplikasi web yang
sedang ditekuni.

---

## 1. Kapan surat ini boleh dikirim?

Hanya kirim laporan **setelah** kondisi berikut terpenuhi:

- [ ] Kerentanan ditemukan **tanpa** merusak, mengubah, menghapus, atau
      menyalin data milik pihak lain
- [ ] Tidak mencoba login/kredensial siapa pun, dan tidak melakukan
      eksploitasi lanjutan di luar yang diperlukan untuk membuktikan bug
- [ ] Anda tahu persis domain/sistem tersebut **milik siapa**, dan
      sebisa mungkin sudah cek apakah ada kebijakan *bug bounty* /
      *security.txt* / kontak resmi keamanan
- [ ] Anda siap dihubungi balik untuk verifikasi

Kalau salah satu poin di atas belum yakin, jangan kirim dulu — cari tahu
kontak resmi dan batasan hukumnya terlebih dahulu (di Indonesia, aktivitas
tanpa izin tetap berisiko terkena UU ITE meskipun niatnya baik).

---

## 2. Cara isi tiap bagian

| Bagian | Isi dengan | Contoh singkat |
|---|---|---|
| **Kepada Yth.** | Nama tim/unit yang menangani keamanan di instansi target | "Tim CSIRT PT XYZ" |
| **I. Informasi Temuan** | Ringkasan cepat — ini yang pertama dibaca tim teknis | Domain, endpoint, tanggal, jenis kerentanan, CVSS |
| **II. Deskripsi Kerentanan** | Ceritakan *apa yang terjadi* dan *kenapa itu salah* | Bukan cuma "ada error", tapi jelaskan penyebabnya |
| **III. Proof of Concept** | Bukti teknis yang bisa direproduksi ulang oleh tim internal | URL, langkah, cuplikan log, screenshot |
| **IV. Mengapa Perlu Diperbaiki** | Alasan urgensi, bukan cuma "ini bug" | Kaitkan ke risiko nyata bagi sistem/pengguna |
| **V. Potensi Dampak** | Skenario terburuk kalau dibiarkan | Kebocoran data, eskalasi ke serangan lain, dst. |
| **VI. Rekomendasi Perbaikan** | Solusi konkret, bukan sekadar "harap diperbaiki" | Contoh konfigurasi/kode kalau memungkinkan |
| **VII. Pernyataan Etika** | Bukti niat baik — bagian ini penting untuk kredibilitas | Jangan dihapus meskipun laporan singkat |

**Tips isi CVSS Score:** kalau belum familiar menghitungnya, pakai
kalkulator resmi di
[first.org/cvss/calculator/3.1](https://www.first.org/cvss/calculator/3.1)
— tinggal jawab beberapa pertanyaan, nanti skor dan *vector string*-nya
otomatis keluar.

---

## 3. Checklist sebelum kirim

- [ ] Semua `[placeholder]` sudah terisi — tidak ada tanda kurung siku
      tersisa
- [ ] Screenshot/lampiran sudah disiapkan dan namanya sesuai yang
      disebut di bagian Lampiran
- [ ] Bahasa sudah dibaca ulang — hindari nada menuduh atau terkesan
      mengancam, tetap sopan walau kerentanannya kritis
- [ ] Kontak yang dicantumkan (email/telepon) aktif dan bisa dihubungi
- [ ] Tidak menyebarkan detail teknis ini ke publik/media sosial dulu
      sebelum ada balasan atau kesepakatan tenggat waktu

---

## 4. Cara mengirim

1. Cari kontak resmi tim keamanan instansi — biasanya lewat:
   - halaman `/.well-known/security.txt` di domain terkait
   - email seperti `security@`, `cert@`, atau `csirt@`
   - jika instansi pemerintah Indonesia, bisa juga ditembuskan ke
     **BSSN** (Badan Siber dan Sandi Negara) via
     [bssn.go.id](https://www.bssn.go.id) sebagai referensi tambahan
2. Kirim surat ini sebagai isi email atau lampiran PDF/Word, dengan
   subjek jelas, misalnya:
   *"Laporan Kerentanan Keamanan — [Jenis Kerentanan] pada [nama
   aplikasi]"*
3. Lampirkan bukti pendukung (screenshot, PoC) secara terpisah, jangan
   digabung jadi satu file besar
4. Beri waktu wajar untuk respons (umumnya 30–90 hari) sebelum
   mempertimbangkan pengungkapan publik

---

## 5. File terkait

- `Template-Surat-Responsible-Disclosure.md` — naskah surat siap isi
