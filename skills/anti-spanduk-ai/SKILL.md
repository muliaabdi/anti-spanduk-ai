---
name: anti-spanduk-ai
description: "Senior design critique and production guidelines for print banners and social media promo without generic AI slop. Evaluates banner images/screenshots or briefs against a 10-dimension craft rubric with ranked findings (blocking -> important -> polish), provides concrete fixes, and generates/revises high-impact, authentic banner designs."
---

# anti-spanduk-ai

Kritik desain tingkat senior dan panduan pembuatan spanduk cetak & banner promosi bebas estetika generik AI.

Memiliki dua mode operasi:
1. **Mode Desain (Generasi Baru)**: Membuat artwork desain spanduk lengkap dengan teks dari brief pengguna, langsung ke kanvas murni tanpa slop AI.
2. **Mode Review / Kritik (Design Critique)**: Membedah dan mengaudit gambar/screenshot spanduk yang diunggah pengguna atau hasil rancangan, memberikan temuan berperingkat (🔴 Blocking → 🟠 Important → 🟡 Polish) dengan perbaikan konkret.

---

## 1. Dapatkan Artefak & Tentukan Mode

- **Jika input berupa Gambar / Tangkapan Layar (Screenshot)** → Jalankan **Mode Review / Kritik Desain**:
  - Periksa hierarki, tipografi, warna, tekstur produk, artefak AI, dan margin aman.
- **Jika input berupa Teks Brief** → Jalankan **Mode Desain**:
  - Langsung rancang artwork lengkap dengan teks di kanvas datar murni (100% flat artwork).
- **Jika input meminta "Review lalu Perbaiki / Revisi"** → Jalankan Mode Review terlebih dahulu untuk membedah masalah, lalu hasilkan prompt revisi presisi atau buat gambar revisinya langsung.

---

## 2. Rubrik Evaluasi 10 Dimensi

Evaluasi artefak terhadap panduan lengkap di `checklist.md`:

1. **Hierarki Visual & Scan Path Jarak Jauh**: 1 focal point jelas, keterbacaan 3–5 detik dari kejauhan.
2. **Tipografi & Keterbacaan**: Font display/sans-serif tebal komersial; Dilarang teks stiker kartun ber-outline ganda.
3. **Ruang Negatif & Tata Letak**: Whitespace fungsional sebagai struktur, tidak padat sesak, margin tepi aman.
4. **Warna & Kontras**: Kontras teks-latar tajam (WCAG AA), palet merek 2–3 warna, larangan gradien biru-ungu neon AI.
5. **Otentisitas Foto Produk**: Fotografi riil autentik (35mm camera, natural daylight); larangan keras tekstur lilin/plastik 3D CGI makanan dan properti klise (karung goni, meja rustic lapuk).
6. **Higienitas Anti-Slop**: Bebas gelombang vektor Canva (*vector waves/blobs*), bebas flare/confetti/partikel cahaya acak, bebas ornamen etnik tempelan.
7. **Ketepatan Konten & Ejaan**: Ejaan nama, angka, kontak, dan tanggal 100% akurat; nol halusinasi slogan fiktif.
8. **Kebutuhan Teknis Cetak Fisik**: Kanvas 100% artwork datar murni; Dilarang menggambar panah dimensi fisik ("3 m"), tali pengikat, atau mata ayam tiruan pada gambar.
9. **Kebutuhan Media Sosial**: Pesan terbaca di layar ponsel, elemen penting aman dari potongan antarmuka aplikasi.
10. **Konsistensi & Karakter Merek**: Relevan dengan karakter bisnis riil, tidak generik.

---

## 3. Format Laporan Kritik (Senior Craft Critique)

Kelompokkan temuan berdasarkan tingkat keparahan. **Fokus pada masalah nyata yang berdampak, bukan sekadar basa-basi.**

### Tingkat Keparahan (Severity Tiers):
- 🔴 **Blocking** — Masalah fatal: teks typo/salah eja, render makanan 3D sintetis/plastik, teks bertabrakan dengan gambar hingga tidak terbaca, elemen penting terkena batas potong/keliman, ada panah ukuran/tali tiruan di kanvas.
- 🟠 **Important** — Masalah yang merusak hierarki, estetika, atau keterbacaan: tipografi gaya stiker kartun ber-outline ganda, terlalu banyak ornamen/gelombang canva, palet warna bertabrakan, ketiadaan titik fokus.
- 🟡 **Polish** — Penyempurnaan detail mikro: penyesuaian kerning/spasi huruf, penyelarasan grid tepi, penyesuaian saturasi aksen.

### Format Setiap Temuan:
- **Apa**: Elemen spesifik dan posisinya pada kanvas.
- **Kenapa**: Alasan fungsional atau keterbacaan (1 kalimat tegas).
- **Solusi**: Perbaikan konkret dengan instruksi/nilai presisi (bukan saran mengambang).

### Struktur Akhir Laporan Review:
1. **Daftar Temuan (🔴 Blocking → 🟠 Important → 🟡 Polish)**
2. **Kelebihan (Strengths)**: 2–3 hal yang sudah dieksekusi dengan baik (kritik yang konstruktif berpijak pada fondasi yang berhasil).
3. **Perubahan Paling Berdampak (Highest-Leverage Change)**: Satu tindakan tunggal paling krusial yang harus dieksekusi pertama kali untuk mendongkrak kualitas desain secara drastis.
4. **Prompt / Instruksi Revisi**: Susunan prompt regenerasi gambar lengkap siap pakai atau instruksi inpaint presisi untuk mewujudkan perbaikan.

---

## 4. Mode Desain: Eksekusi Gambar Bebas Slop

Jika menjalankan pembuatan gambar baru:
1. Hasilkan desain datar yang memenuhi kanvas (100% pure flat artwork).
2. Dilarang menyertakan mockup ruangan, panah ukuran dimensi ("3 m"), tali tambang, atau ring paku mata ayam.
3. Gunakan tipografi komersial tebal tanpa outline ganda kartun.
4. Gunakan fotografi produk nyata beralas natural atau latar solid datar.
5. Jalankan self-critique internal terhadap kriteria 🔴 Blocking sebelum menyerahkan gambar ke pengguna.
