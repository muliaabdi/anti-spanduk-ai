# anti-spanduk-ai

Skill untuk menghasilkan prompt image generator yang membuat spanduk cetak dan media sosial tanpa estetika generik AI.

## Tujuan

- Pesan spesifik, bukan slogan kosong
- Hierarki informasi jelas
- Ornamen punya fungsi, bukan dekorasi bawaan model
- Teks terbaca dan akurat
- Siap disesuaikan untuk cetak atau media sosial

## Instalasi

Salin folder `skill/anti-spanduk-ai` ke direktori skill agent Anda.

Contoh OpenCode:

```bash
cp -r skill/anti-spanduk-ai ~/.agents/skills/
```

## Penggunaan

Minta agent membuat prompt untuk spanduk, banner, atau materi promosi. Sebutkan tujuan, ukuran, pesan utama, dan identitas visual. Skill akan menanyakan informasi yang kurang, lalu menyusun prompt beserta checklist verifikasi.

Contoh:

> Buat prompt banner cetak 3 × 1 meter untuk pembukaan toko roti. Nama: Roti Pagi. Tanggal: 12 Oktober 2026. Pesan: Diskon 20% semua roti. Warna merek: krem dan cokelat. Semua teks harus dibuat image generator.

## Batasan

Image generator tidak menjamin teks benar atau file siap cetak. Hasil wajib diperiksa untuk ejaan, resolusi aktual, bleed, dan profil warna sebelum masuk percetakan.

## Struktur

```text
skill/anti-spanduk-ai/SKILL.md
```
