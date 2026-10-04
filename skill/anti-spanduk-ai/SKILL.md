---
name: anti-spanduk-ai
description: "Menyusun prompt image generator untuk spanduk cetak dan banner media sosial tanpa estetika generik AI. Gunakan saat diminta membuat prompt untuk spanduk, banner, poster promosi, feed/Story Instagram, dan desain promosi lain yang dihasilkan penuh lewat image generator (teks termasuk)."
---

# anti-spanduk-ai

> Skill prompt spanduk cetak & media sosial. Semua elemen, termasuk teks, dihasilkan image generator dalam satu gambar.

## Kapan dipakai

Permintaan membuat prompt untuk spanduk cetak, banner, poster promosi, feed atau Story media sosial, thumbnail, dan sejenisnya, yang hasil akhirnya satu gambar dari image generator.

Tidak untuk: desain UI, hero section website, atau layout yang teksnya ditulis terpisah di editor (Canva/Figma/Illustrator).

## Prinsip

1. **Pesan spesifik, bukan slogan kosong.** "Diskon 20% semua roti sampai 12 Oktober" bekerja. "Solusi Terbaik untuk Kebutuhan Anda" tidak.
2. **Satu pesan utama.** Spanduk dibaca 3-5 detik. Judul, penawaran, satu informasi pendukung. Sisanya kehilangan.
3. **Hierarki jarak baca.** Ukuran teks mengikuti jarak baca: judul terlihat dari jauh, detail terbaca dari dekat.
4. **Ornamen punya fungsi.** Dekorasi hanya jika memperkuat pesan atau identitas merek. Tanpa alasan, hapus.
5. **Identitas dari merek, bukan dari model.** Warna, font, dan mood mengikuti identitas yang disebut pengguna. Tidak ada identitas? Tanya dulu, jangan pakai default.

## Larangan estetika generik AI

Prompt WAJIB menghindari pola berikut, kecuali pengguna meminta eksplisit:

| Pola | Kenapa dihindari | Pengganti |
|---|---|---|
| Gradien biru-ungu / biru-cyan | Tanda tangan visual model paling umum, terbaca "buatan AI" seketika | Palet warna merek; maksimal 2-3 warna |
| Glow / cahaya memancar di semua objek | Amplifikasi tanpa hierarki; semua menonjol berarti tidak ada yang menonjol | Glow hanya pada satu titik fokus, atau tidak sama sekali |
| Wajah generik stok tersenyum | Tidak berkaitan dengan pesan, mengganti informasi dengan dekorasi | Produk, hasil nyata, atau ilustrasi yang mewakili penawaran |
| Latar oranye-biru "cinematic" dengan partikel cahaya | Komposisi template paling sering muncul | Latar sederhana kontras dengan pesan |
| Robot, otak neon, lingkaran digital | Simbol klise untuk "teknologi" | Objek nyata dari produk/layanan |
| Tipografi 3D metalik chrome | Sulit dibaca, cepat usang, sering terdistorsi | Font tebal bersih dengan kontras kuat |
| Komposisi simetris sempurna dengan logo di tengah | Terasa sertifikat, bukan spanduk | Hierarki asimetris: pesan utama dominan, logo kecil di sudut atau bawah |
| Ornamen memenuhi tepi (confetti, gelembung, garis abstrak) | Mengurangi ruang pesan dan keterbacaan | Ruang kosong sebagai bagian dari desain |

## Aturan teks (dibuat image generator)

Karena teks dirender model, salah eja dan distorsi adalah risiko utama.

1. **Teks sesedikit mungkin.** Setiap kata menambah risiko cacat. Target maksimal: judul + penawaran + satu baris informasi + nama merek.
2. **Pesan dalam prompt ditulis eksplisit, kata per kata, dalam tanda kutip.** Jangan biarkan model meringkas atau menerjemahkan.
3. **Tetapkan peran tiap teks:** judul utama, subjudul, informasi, nama merek. Sebut ukuran relatifnya ("teks judul terbesar, ±30% tinggi kanvas").
4. **Gunakan model yang andal untuk teks.** Jika ragu, sarankan model generasi gambar dengan kemampuan teks terbaik saat ini (misal seri terbaru Gemini/Nano Banana, GPT-image, Ideogram). Sebutkan di saran penggunaan.
5. **Kata pendek > kata panjang.** "GRATIS ONGKIR" lebih tahan distorsi daripada kalimat.
6. **Nama merek dan angka rentan salah.** Perintahkan ejaan eksak: `"Roti Pagi"` huruf R kapital, P kapital, satu kata masing-masing. Angka ditulis angka, bukan kata.
6. **Wajib checklist verifikasi teks** setelah gambar jadi (lihat bawah). Salah satu huruf rusak = generate ulang bagian itu atau seluruh gambar.

## Cetak vs media sosial

### Spanduk / banner cetak

- Tanyakan atau cari tahu ukuran fisik dan unit (meter/cm) dan rasio.
- Rasio tidak standar? Sarankan generate di rasio terdekat yang didukung model lalu crop, ATAU generate dalam segmen. Sebutkan konsekuensinya.
- Area aman: pentingkan pesan di tengah 80%; tepi berisiko terpotong pemasangan.
- Detail jarak baca: judul dominan (minimal ±20-25% tinggi kanvas), informasi pendukung tetap besar.
- Latar belakang lebih pekat dari tampilan layar; cetak menggelap 5-15%.
- Ingatkan pengguna: hasil generator perlu diperiksa resolusi (target minimal 72-150 DPI pada ukuran cetak untuk spanduk jarak jauh) dan profil warna percetakan. Skill tidak menghasilkan file siap cetak.

### Media sosial

- Rasio bawaan: feed persegi 1:1, portrait 4:5; Story/Reels 9:16; header X/LinkedIn sesuai ukuran terkini.
- Cek area terpotong: atas-bawah Story tertutup UI; jangan taruh teks di sana.
- Teks lebih kecil dari spanduk cetak, tapi tetap terbaca di layar ponsel: uji dengan pratinjau diperkecil.
- Satu gambar satu tujuan: penawaran, pengumuman, ATAU brand reminder. Jangan semua.

## Format prompt

Susun prompt dengan struktur berikut, adaptif bahasa Indonesia/Inggris sesuai model yang dipakai:

```text
[Jenis desain] [ukuran/rasio] untuk [tujuan promosi].
Gaya: [identitas merek: warna, mood, referensi].
Pesan utama: "[teks eksak]" — [peran: judul, ukuran relatif].
Teks pendukung: "[teks eksak]" — [peran, ukuran relatif].
Nama merek: "[ejaan eksak]" — posisi.
Komposisi: [hierarki, titik fokus, arah baca].
Latar: [deskripsi sederhana, kontras dengan teks].
Hindari: [daftar dari tabel larangan yang relevan].
```

Contoh:

```text
Spanduk cetak 3:1 untuk pembukaan toko roti.
Gaya: hangat dan bersih, palet krem dan cokelat tua, tanpa gradien.
Pesan utama: "DISKON 20% SEMUA ROTI" — judul, teks terbesar, ±25% tinggi kanvas, font tebal bersih.
Teks pendukung: "S/D 12 OKTOBER" — ±10% tinggi kanvas.
Nama merek: "Roti Pagi" — pojok kiri atas, kecil.
Komposisi: pesan utama di tengah-kiri, foto roti hangat di kanan, ruang kosong cukup di tepi.
Latar: krem polos dengan kontras cokelat tua untuk teks.
Hindari: gradien biru-ungu, glow, wajah stok tersenyum, ornamen memenuhi tepi, font 3D chrome.
```

## Informasi yang wajib ada sebelum menyusun prompt

Tanya satu per satu hanya yang belum disebut pengguna:

1. Tujuan spanduk (penawaran? pengumuman? branding?)
2. Ukuran atau rasio dan media (cetak/media sosial/platform mana)
3. Pesan utama, kata per kata
4. Teks pendukung dan nama merek
5. Identitas visual: warna, font kesukaan, mood, referensi
6. Model image generator yang dipakai (untuk kalibrasi kekuatan teks)

## Checklist verifikasi hasil (wajib setelah gambar jadi)

Jalankan bersama pengguna pada gambar hasil:

- [ ] Semua teks persis seperti diminta, tanpa salah eja, tanpa huruf rusak
- [ ] Angka dan nama merek benar
- [ ] Pesan utama terbaca pada ukuran/jarak target (kecilkan pratinjau untuk simulasi)
- [ ] Tidak ada pola larangan dari tabel di atas (kecuali diminta eksplisit)
- [ ] Rasio benar, pesan tidak di zona berisiko terpotong
- [ ] Komposisi: satu titik fokus, hierarki jelas

Gagal satu butir teks = generate ulang dengan penekanan ejaan pada bagian yang rusak. Gagal butir komposisi = perbaiki prompt, bukan terima.

## Batasan

- Skill menghasilkan prompt dan verifikasi, bukan file siap cetak. Konversi resolusi, bleed, dan profil warna tetap tugas percetakan/editor.
- Kualitas teks tergantung model. Bila model tidak andal untuk teks dan pengguna tetap ingin semua via generator, catat risiko secara eksplisit dan sarankan generasi ulang bertahap.
- Jangan gunakan nama merek/orang nyata tanpa izin, dan jangan tiru karya seniman spesifik. Buat gaya dari deskripsi, bukan dari nama seniman.
