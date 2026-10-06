# anti-spanduk-ai

Instruksi siap pakai dan skill untuk **membuat** serta **mengaudit (critique)** desain spanduk cetak dan banner media sosial tanpa estetika generik AI. Terinspirasi oleh metodologi kritik desain senior [Superfuture/design-review](https://github.com/Superfuture/design-review).

Dapat diunggah langsung ke **ChatGPT / Gemini**, atau dipasang sebagai skill di **Claude Code / Antigravity IDE**.

---

## 2 Mode Operasi

1. **Mode Desain (Generasi Baru)**: AI langsung menghasilkan artwork lengkap dengan teks di atas kanvas datar murni (100% flat artwork) dari brief singkat, bebas dari render plastik 3D dan ornamen klise AI.
2. **Mode Review / Kritik (Design Critique)**: AI membedah gambar atau screenshot spanduk yang Anda unggah menggunakan **Rubrik 10 Dimensi Spanduk**, memberikan temuan berperingkat (**🔴 Blocking → 🟠 Important → 🟡 Polish**), kelebihan (**Strengths**), satu perubahan paling krusial (**Highest-Leverage Change**), dan prompt revisi siap pakai.

---

## Cara Pakai

### Opsi A: Di ChatGPT / Gemini Web
1. Unggah file `anti-spanduk-ai.md` (atau pasang di **Custom GPT**).
2. **Untuk membuat desain:** Berikan brief singkat:
   > Buat sesuai anti-spanduk-ai.md: Banner cetak 3 × 1 meter untuk pembukaan toko roti. Nama: Roti Pagi. Tanggal: 12 Oktober 2026. Pesan: Diskon 20% semua roti. Warna: krem dan cokelat.
3. **Untuk membedah / me-review desain:** Unggah gambar/screenshot spanduk Anda:
   > Review spanduk ini sesuai anti-spanduk-ai.md. Apa yang kurang sebelum dicetak?

### Opsi B: Sebagai Skill (Claude Code / Antigravity IDE)
Salin folder `skills/anti-spanduk-ai` ke direktori skill agent Anda:
```bash
# Untuk Claude Code
cp -r skills/anti-spanduk-ai ~/.claude/skills/anti-spanduk-ai

# Untuk Antigravity IDE (.agents/skills)
mkdir -p .agents/skills && cp -r skills/anti-spanduk-ai .agents/skills/
```

---

## Format Laporan Kritik (Design Critique)

Saat mengaudit gambar spanduk, temuan disajikan berperingkat:
- 🔴 **Blocking** — Kesalahan fatal: salah eja nama/angka, render makanan 3D sintetis/plastik, teks menabrak batas potong/keliman cetak, panah ukuran "3 m" tergambar di kanvas.
- 🟠 **Important** — Merusak hierarki & estetika: font stiker kartun ber-outline ganda, ornamen gelombang canva klise, warna tidak harmonis, ketiadaan titik fokus.
- 🟡 **Polish** — Penyempurnaan mikro: kerning huruf, margin visual mikro, penyelarasan tepi.
- **Strengths** — 2–3 poin elemen yang sudah berhasil dieksekusi dengan baik.
- **Highest-Leverage Change** — 1 perubahan tunggal paling berdampak yang harus diperbaiki duluan.
- **Prompt Revisi Siap Pakai** — Prompt generasi ulang gambar yang presisi jika ingin memperbaiki langsung.

---

## Isi & Standar Craft

- **10 Dimensi Rubrik Spanduk**: Hierarki Visual, Tipografi, Ruang Negatif, Warna & Kontras, Otentisitas Foto Produk, Higienitas Anti-Slop, Ketepatan Konten, Kebutuhan Teknis Cetak, Kebutuhan Media Sosial, dan Karakter Merek.
- **19 Pola AI Generik yang Dilarang**: Dari render makanan CGI lilin/plastik hingga font outline stiker kartun.
- **Aturan Cetak Fisik Murni**: Kanvas 100% artwork datar tanpa panah dimensi ("3 m"), tali tambang, atau ring paku mata ayam tiruan.
- **Self-Critique Otomatis**: Audit berjenjang sebelum gambar diserahkan.

---

## Sebelum & Sesudah

### Sebelum (Prompt Biasa / Estetika AI Generik)

![Sebelum](assets/before.png)

- Terlalu ramai dengan ornamen dekoratif dan bingkai klise
- Hierarki teks hilang dan bertumpuk
- Sulit dibaca dari kejauhan

### Sesudah (Dengan anti-spanduk-ai)

![Sesudah](assets/after.png)

- Tipografi tebal, kontras kuat, dan langsung terbaca
- Hierarki jelas: penawaran utama dan tanggal langsung terlihat
- Visual produk nyata dengan ruang negatif yang lega

---

## Batasan

Image generator tidak menjamin teks benar atau file siap cetak. Hasil wajib diperiksa untuk ejaan, resolusi aktual, bleed, dan profil warna sebelum masuk percetakan.

---

## Struktur Repositori

```text
anti-spanduk-ai/
├── anti-spanduk-ai.md        <- Panduan utama (unggah ke ChatGPT/Gemini / Custom GPT)
├── README.md
├── assets/
│   ├── before.png
│   └── after.png
└── skills/
    └── anti-spanduk-ai/
        ├── SKILL.md          <- Agent skill (Claude Code / Antigravity)
        └── checklist.md      <- 10 dimensi rubrik craft spanduk & banner
```
