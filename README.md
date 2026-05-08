# Clothing.co — Situs Statis HTML

Situs peragaan **Clothing.co** untuk mata kuliah Pemrograman Web: halaman produk fashion *ready-to-wear* dengan layout berbasis **HTML** (tabel, navigasi, dan *frames*). Tidak memakai framework atau build step; cukup dibuka sebagai file statis atau di-hosting misalnya **GitHub Pages**.

## Isi situs

- **Beranda** — ringkasan brand dan tautan cepat  
- **Profil toko** — cerita brand  
- **Galeri produk** — kumpulan gambar koleksi  
- **Daftar harga** — referensi harga  
- **Kontak** — informasi kontak  
- **Kategori** — Atasan, Bawahan, Luaran, Aksesoris (`categories/`)  
- **Halaman produk** — detail per item (`products/`)

## Struktur folder

| Path | Keterangan |
|------|------------|
| `index.html` | Entry point: `frameset` (header, menu, konten, footer) |
| `header.html`, `menu.html`, `footer.html` | Bagian layout yang dimuat di frame |
| `home.html`, `profil.html`, `gallery.html`, `price.html`, `kontak.html` | Halaman konten utama |
| `categories/` | Halaman per kategori |
| `products/` | Halaman detail produk |
| `assets/image/` | Logo, banner, galeri, thumbnail |

## Menjalankan di komputer lokal

1. Clone atau unduh folder proyek ini.  
2. Buka `index.html` di browser (double-click), **atau** jalankan server sederhana di root proyek agar semua path dan frame berperilaku konsisten:

   ```bash
   cd "/path/ke/UTS"
   python3 -m http.server 8080
   ```

   Lalu buka `http://localhost:8080/`.

## GitHub Pages (GitHub Actions)

Repo ini menyertakan workflow **Deploy to GitHub Pages** (`.github/workflows/deploy-github-pages.yml`), yang jalan pada push ke branch `main` atau manual lewat tab **Actions**.

**Sekali setelan di GitHub:**

1. **Settings** → **Pages**  
2. **Build and deployment** → **Source**: pilih **GitHub Actions** (bukan *None*).  
3. Setelah workflow sukses, URL umumnya: `https://<username>.github.io/<nama-repo>/`

Jika deploy gagal dengan error **404** pada step *Creating Pages deployment*, biasanya Pages belum diset ke sumber **GitHub Actions**; pastikan langkah di atas sudah disimpan.

**Alternatif tanpa Actions:** di **Pages**, pilih **Deploy from a branch** → branch `main`, folder `/ (root)` — lalu nonaktifkan atau hapus workflow supaya tidak bentrok.

## Teknologi

- HTML (termasuk `<frameset>` / `<frame>` untuk layout multipanel)  
- Aset gambar (misalnya WebP/PNG) di `assets/`

---

*Proyek akademik — Clothing.co & branding pada konten merupakan contoh untuk keperluan pembelajaran.*
