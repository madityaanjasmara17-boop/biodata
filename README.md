# Portfolio Website

Website portofolio modern dan responsif yang dibuat dengan HTML, CSS, dan JavaScript vanilla.

## Fitur

- ✨ Desain modern dan menarik
- 📱 Responsif untuk semua perangkat (mobile, tablet, desktop)
- 🎨 Animasi smooth dan transisi yang halus
- 🧭 Navigasi yang mudah digunakan
- 📧 Form kontak yang fungsional
- ⚡ Cepat dan ringan (tanpa framework)

## Struktur File

```
proyek_test/
├── index.html      # Halaman utama
├── styles.css      # Styling dan desain
├── script.js       # Interaktivitas dan animasi
└── README.md       # Dokumentasi
```

## Cara Menggunakan

1. Buka file `index.html` di browser web Anda
2. Atau gunakan live server untuk development:
   ```bash
   # Jika menggunakan VS Code, install extension "Live Server"
   # Klik kanan pada index.html dan pilih "Open with Live Server"
   ```

## Kustomisasi

### Mengubah Informasi Pribadi

1. **Nama dan Profesi**: Edit di bagian Hero Section (`index.html` baris 30-35)
2. **Tentang Saya**: Edit di bagian About Section (`index.html` baris 60-75)
3. **Keahlian**: Edit di bagian Skills Section (`index.html` baris 85-110)
4. **Proyek**: Edit di bagian Projects Section (`index.html` baris 120-170)
5. **Kontak**: Edit di bagian Contact Section (`index.html` baris 180-220)

### Mengubah Warna

Edit variabel CSS di file `styles.css` (baris 4-12):

```css
:root {
    --primary-color: #6366f1;    /* Warna utama */
    --primary-dark: #4f46e5;     /* Warna utama gelap */
    --secondary-color: #8b5cf6;  /* Warna sekunder */
    /* ... */
}
```

### Menambahkan Gambar

1. Buat folder `images` di direktori proyek
2. Tambahkan gambar Anda
3. Ganti placeholder di HTML dengan tag `<img>`:
   ```html
   <img src="images/foto-anda.jpg" alt="Foto Profil">
   ```

## Mengelola Proyek

Untuk menambah atau menghapus proyek, Anda perlu mengedit file `index.html` secara manual.

### Lokasi File yang Perlu Diedit

**File**: `index.html`  
**Bagian**: Section dengan id `projects` (sekitar baris 129-200)

### Cara Menambah Proyek Baru

1. Buka file `index.html` dengan text editor
2. Cari bagian berikut:
   ```html
   <section id="projects" class="projects">
       <div class="container">
           <h2 class="section-title">Proyek Saya</h2>
           <div class="projects-grid" id="projects-grid">
   ```
3. Di dalam `<div class="projects-grid">`, tambahkan card proyek baru **sebelum** tag penutup `</div>` (sebelum baris `</div></div></section>`)
4. Gunakan struktur berikut sebagai template:
   ```html
   <div class="project-card" data-project-id="4">
       <div class="project-image">
           <div class="project-placeholder">Nama Proyek</div>
       </div>
       <div class="project-content">
           <h3 class="project-title">Judul Proyek Anda</h3>
           <p class="project-description">
               Deskripsi lengkap tentang proyek Anda. Jelaskan fitur-fitur utama, 
               teknologi yang digunakan, dan hasil yang dicapai.
           </p>
           <div class="project-tags">
               <span class="tag">React</span>
               <span class="tag">Node.js</span>
               <span class="tag">MongoDB</span>
               <span class="tag">Express</span>
           </div>
           <a href="https://github.com/username/project" class="project-link" target="_blank">Lihat Proyek →</a>
       </div>
   </div>
   ```
5. **Ganti bagian-bagian berikut**:
   - `data-project-id="4"` → Ganti dengan ID unik (4, 5, 6, dst.)
   - `Nama Proyek` → Nama singkat proyek (akan muncul di placeholder)
   - `Judul Proyek Anda` → Judul lengkap proyek
   - `Deskripsi lengkap...` → Deskripsi proyek Anda
   - `<span class="tag">React</span>` → Ganti dengan teknologi yang digunakan (tambah/hapus tag sesuai kebutuhan)
   - `https://github.com/username/project` → URL proyek atau repository GitHub Anda

**Contoh Proyek Lengkap**:
```html
<div class="project-card" data-project-id="4">
    <div class="project-image">
        <div class="project-placeholder">Blog Platform</div>
    </div>
    <div class="project-content">
        <h3 class="project-title">Personal Blog Platform</h3>
        <p class="project-description">
            Platform blog pribadi dengan fitur rich text editor, komentar, 
            dan sistem autentikasi. Dibangun dengan Next.js dan menggunakan 
            Markdown untuk konten.
        </p>
        <div class="project-tags">
            <span class="tag">Next.js</span>
            <span class="tag">TypeScript</span>
            <span class="tag">Prisma</span>
            <span class="tag">PostgreSQL</span>
        </div>
        <a href="https://github.com/ahmadrizki/blog-platform" class="project-link" target="_blank">Lihat Proyek →</a>
    </div>
</div>
```

### Cara Menghapus Proyek

1. Buka file `index.html` dengan text editor
2. Cari bagian `<section id="projects" class="projects">`
3. Di dalam `<div class="projects-grid">`, cari card proyek yang ingin dihapus
4. Hapus **seluruh blok** mulai dari `<div class="project-card" data-project-id="X">` sampai `</div>` yang menutup card tersebut
5. Pastikan tidak menghapus tag penutup `</div>` dari `projects-grid` atau `container`

**Contoh**: Untuk menghapus proyek dengan ID 2, hapus seluruh blok berikut:
```html
<div class="project-card" data-project-id="2">
    <div class="project-image">
        <div class="project-placeholder">Analytics Dashboard</div>
    </div>
    <div class="project-content">
        <!-- ... semua konten di dalamnya ... -->
    </div>
</div>
```

### Tips

- ✅ **ID Proyek**: Pastikan setiap proyek memiliki `data-project-id` yang unik (1, 2, 3, 4, dst.)
- ✅ **Urutan Proyek**: Proyek akan ditampilkan sesuai urutan di HTML (dari atas ke bawah)
- ✅ **Tags**: Anda bisa menambah atau mengurangi tag sesuai teknologi yang digunakan
- ✅ **Link Proyek**: Jika tidak ada URL, ganti `<a href="...">` dengan `<span class="project-link">Lihat Proyek →</span>`
- ✅ **Placeholder**: Teks di `project-placeholder` akan muncul di bagian gambar proyek

## Mempublikasikan Website (Agar Bisa Dilihat Orang Lain)

**Status Saat Ini**: Website hanya bisa dilihat di komputer Anda sendiri (lokal).

Untuk membuat website bisa diakses oleh orang lain di internet, Anda perlu **deploy/hosting** website ini. Berikut beberapa opsi **gratis** yang mudah digunakan:

### Opsi 1: Netlify (Paling Mudah - Direkomendasikan)

1. **Persiapan**:
   - Buat akun di [netlify.com](https://www.netlify.com) (gratis)
   - Atau hubungkan dengan GitHub/GitLab

2. **Cara Deploy**:
   - **Drag & Drop**: Buka [app.netlify.com/drop](https://app.netlify.com/drop)
   - Drag folder `proyek_test` ke halaman tersebut
   - Website akan langsung online dengan URL seperti: `https://random-name-123.netlify.app`
   - Anda bisa ubah nama di Settings → Site details → Change site name

3. **Keuntungan**:
   - ✅ Gratis selamanya
   - ✅ URL custom (bisa ubah nama)
   - ✅ HTTPS otomatis
   - ✅ Deploy ulang cukup drag & drop lagi

### Opsi 2: Vercel

1. **Persiapan**:
   - Buat akun di [vercel.com](https://vercel.com) (gratis)

2. **Cara Deploy**:
   - Install Vercel CLI: `npm i -g vercel`
   - Atau gunakan website: Upload folder melalui dashboard
   - Website akan online dengan URL: `https://your-project.vercel.app`

3. **Keuntungan**:
   - ✅ Gratis
   - ✅ Cepat dan modern
   - ✅ Integrasi dengan GitHub

### Opsi 3: GitHub Pages (Jika Punya GitHub)

1. **Persiapan**:
   - Buat akun GitHub di [github.com](https://github.com)
   - Install Git di komputer Anda

2. **Cara Deploy**:
   ```bash
   # Di terminal, masuk ke folder proyek
   cd /home/koko/proyek_test
   
   # Inisialisasi Git
   git init
   git add .
   git commit -m "Portfolio website"
   
   # Buat repository baru di GitHub, lalu:
   git remote add origin https://github.com/username/portfolio.git
   git branch -M main
   git push -u origin main
   ```
   
   - Di GitHub, masuk ke Settings → Pages
   - Pilih branch `main` dan folder `/ (root)`
   - Website akan online di: `https://username.github.io/portfolio`

3. **Keuntungan**:
   - ✅ Gratis
   - ✅ URL: `username.github.io/nama-repo`
   - ✅ Update mudah (tinggal push ke GitHub)

### Opsi 4: Surge.sh (Sangat Cepat)

1. **Persiapan**:
   ```bash
   npm install -g surge
   ```

2. **Cara Deploy**:
   ```bash
   cd /home/koko/proyek_test
   surge
   # Ikuti instruksi di terminal
   # Website akan online di: https://nama-pilihan.surge.sh
   ```

3. **Keuntungan**:
   - ✅ Gratis
   - ✅ Deploy dari terminal (sangat cepat)
   - ✅ URL custom

### Opsi 5: Firebase Hosting

1. **Persiapan**:
   - Buat akun di [firebase.google.com](https://firebase.google.com)
   - Install Firebase CLI: `npm install -g firebase-tools`

2. **Cara Deploy**:
   ```bash
   firebase login
   firebase init hosting
   firebase deploy
   ```

### Rekomendasi untuk Pemula

**Paling Mudah**: **Netlify** dengan drag & drop
- Tidak perlu install apapun
- Tidak perlu coding
- Langsung online dalam hitungan detik

**Jika Sudah Kenal Git**: **GitHub Pages**
- Gratis dan terpercaya
- URL profesional
- Mudah update

### Catatan Penting

- ⚠️ **Form Kontak**: Form kontak di website ini hanya menampilkan alert. Untuk benar-benar mengirim email, Anda perlu:
  - Menggunakan service seperti [Formspree](https://formspree.io) (gratis)
  - Atau setup backend sendiri
  
- ✅ **Update Website**: Setelah deploy, setiap kali Anda update file, deploy ulang dengan cara yang sama

- ✅ **URL Custom**: Semua platform di atas menyediakan URL gratis, dan beberapa juga mendukung custom domain (bayar)

## Browser Support

Website ini kompatibel dengan semua browser modern:
- Chrome/Edge (terbaru)
- Firefox (terbaru)
- Safari (terbaru)
- Opera (terbaru)

## Tips

- Pastikan semua gambar dioptimalkan untuk web
- Uji website di berbagai ukuran layar
- Periksa form kontak berfungsi dengan baik
- Update link sosial media dengan URL yang benar

## Lisensi

Bebas digunakan untuk keperluan pribadi atau komersial.

