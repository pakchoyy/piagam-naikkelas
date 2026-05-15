# 🎓 Bantu Guru Yuk | Generator Piagam Naik Kelas SD

Generator piagam kenaikan kelas otomatis untuk guru SD.
Frontend-only, tidak butuh backend, deploy langsung ke Netlify/Vercel/GitHub Pages.

---

## 📁 Struktur Project

```
/
├── index.html          ← SATU FILE INI SAJA (semua logic ada di sini)
├── templates/
│   ├── t1.jpg          ← Template 1 (FREE)
│   ├── t2.jpg          ← Template 2 (PRO)
│   ├── t3.jpg
│   ├── t4.jpg
│   ├── t5.jpg
│   ├── t6.jpg
│   └── t7.jpg
└── README.md
```

---

## 🖼️ Cara Pakai Template Sendiri

1. Desain piagam di Canva (ukuran **A4 Landscape = 2480 x 1754 px**)
2. Export sebagai **JPG** kualitas tinggi
3. Taruh di folder `/templates/` dengan nama `t1.jpg` sampai `t7.jpg`
4. Buka `index.html`, cari bagian `const TEMPLATES = [...]`
5. Sesuaikan `pos` (posisi teks) dan `style` (warna/ukuran) per template

### Panduan `pos` (posisi teks)
Semua nilai adalah **rasio 0.0 – 1.0** dari ukuran canvas:
- `x: 0.5` = tengah horizontal
- `y: 0.44` = 44% dari atas
- `x: 0.68, y: 0.84` = 68% dari kiri, 84% dari atas

### Panduan `style`
```js
judul: { color: '#7a4f0a', size: 0.050, bold: true }
//        warna hex        % tinggi     tebal?
```
- `size: 0.050` artinya 5% dari tinggi canvas ≈ 62px di canvas 1240px

---

## 📊 Format Excel

| Nama | Kategori |
|------|----------|
| Andi Firmansyah | Siswa Terbaik |
| Siti Nurhaliza | Siswa Terajin |

- Baris pertama boleh header (Nama, Kategori) atau langsung data
- Kolom A = Nama siswa
- Kolom B = Kategori/prestasi

---

## 🆓 FREE vs PRO

| Fitur | FREE | PRO |
|-------|------|-----|
| Template | Template 1 saja | Semua 7 template |
| Jumlah siswa | Maks 10 siswa | Unlimited |
| Watermark | Ada | Tidak ada |

Untuk aktifkan PRO, ubah baris ini di `index.html`:
```js
const IS_PRO = false; // ← ganti jadi true
```

---

## 🚀 Deploy

### Netlify (drag & drop)
1. Buka [netlify.com/drop](https://netlify.com/drop)
2. Drag seluruh folder project
3. Selesai — dapat URL otomatis

### Vercel
```bash
npm i -g vercel
vercel --prod
```

### GitHub Pages
1. Push ke GitHub
2. Settings → Pages → Deploy from branch `main` / `root`

---

## 📦 Library yang Digunakan
- [SheetJS](https://sheetjs.com/) — baca file Excel
- [jsPDF](https://github.com/parallax/jsPDF) — export PDF
- [JSZip](https://stuk.github.io/jszip/) — export ZIP
- Google Fonts: Cinzel, Lato, Playfair Display

---

Dibuat dengan ❤️ oleh **Bantu Guru Yuk** | bantuguruyuk.web.id
