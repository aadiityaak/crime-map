# 🗺️ Crime Map - Sistem Pemetaan Kejahatan Indonesia

<div align="center">

![Crime Map Dashboard](https://img.shields.io/badge/Crime%20Map-Dashboard-red?style=for-the-badge)
![Laravel](https://img.shields.io/badge/Laravel-11.x-red?style=for-the-badge&logo=laravel)
![Vue.js](https://img.shields.io/badge/Vue.js-3.x-green?style=for-the-badge&logo=vue.js)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=for-the-badge&logo=typescript)
![PHP](https://img.shields.io/badge/PHP-8.3-purple?style=for-the-badge&logo=php)

_Sistem informasi pemetaan dan monitoring kejahatan berbasis web dengan visualisasi interaktif untuk seluruh Indonesia_

[Demo](#-demo) • [Fitur](#-fitur) • [Instalasi](#-instalasi) • [Dokumentasi](#-dokumentasi) • [Contributing](#-contributing)

</div>

---

## 📋 Deskripsi

**Crime Map** adalah aplikasi web modern untuk pemetaan dan monitoring data kejahatan di Indonesia. Aplikasi ini menyediakan visualisasi interaktif menggunakan peta Leaflet, dashboard statistik komprehensif, dan sistem manajemen data yang user-friendly.

### 🎯 Tujuan Aplikasi

- **Visualisasi Data Kejahatan**: Menampilkan data kejahatan secara visual pada peta interaktif
- **Monitoring Real-time**: Dashboard statistik untuk monitoring tren kejahatan
- **Manajemen Data**: Interface admin untuk mengelola data wilayah dan kejahatan
- **Analisis Geografis**: Analisis sebaran kejahatan berdasarkan wilayah administratif

---

## ✨ Fitur Unggulan

### 🗺️ **Interactive Crime Mapping**

- Peta Indonesia interaktif dengan Leaflet.js
- 16+ ikon kejahatan berbeda per jenis crime
- Click & drag untuk lokasi coordinates
- Auto-center berdasarkan provinsi
- Responsive design untuk mobile & desktop

### 📊 **Advanced Dashboard**

- Statistik real-time dengan cards modern
- Grafik dan visualisasi data
- Filter berdasarkan wilayah
- Export data capabilities

### 🔍 **Smart Search & Filtering**

- Real-time search dengan debouncing
- Pagination 50 items per halaman
- Advanced filtering berdasarkan:
    - Provinsi, Kabupaten/Kota, Kecamatan
    - Jenis kejahatan
    - Koordinat geografis

### 🏛️ **Comprehensive Data Management**

- **Provinsi**: 38 provinsi Indonesia lengkap
- **Kabupaten/Kota**: 514+ kabupaten/kota
- **Kecamatan**: 7,288+ kecamatan
- **Data Kejahatan**: CRUD lengkap dengan coordinate mapping

### 🎨 **Modern UI/UX**

- Dark mode support
- Responsive design
- Loading states & animations
- Error handling yang user-friendly
- Beautiful card layouts & statistics

---

## 🛠️ Tech Stack

### **Backend**

- **Laravel 11.x** - PHP Framework
- **PHP 8.3+** - Server-side language
- **MySQL** - Database
- **Inertia.js** - Modern SPA experience

### **Frontend**

- **Vue.js 3** - Progressive JavaScript framework
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **Vite** - Fast build tool
- **Leaflet.js** - Interactive maps

### **UI Components**

- **Radix Vue** - Headless UI components
- **Lucide Icons** - Beautiful icon library
- **Class Variance Authority** - Component variants

---

## 🚀 Demo

### Dashboard Preview

```
🎯 Total Kejahatan: 18 kasus
🗺️ Provinsi Terdampak: 6 provinsi
🏢 Kab/Kota Terdampak: 12 kab/kota
📍 Kecamatan Terdampak: 18 kecamatan
🏷️ Jenis Kejahatan: 8 kategori
```

### Crime Types Supported

- 🔴 Pencurian
- 🟠 Perampokan
- 🟣 Pembunuhan
- 🩷 Pemerkosaan
- 🟡 Penipuan
- 🟢 Narkoba
- 🔵 Kekerasan
- ⚫ Vandalisme

---

## 📦 Instalasi

### Prerequisites

- PHP 8.3+
- Composer
- Node.js 18+
- MySQL 8.0+
- Web server (Apache/Nginx)

### Quick Start

1. **Clone Repository**

    ```bash
    git clone https://github.com/aadiityaak/crime-map.git
    cd crime-map
    ```

2. **Install Dependencies**

    ```bash
    # Backend dependencies
    composer install

    # Frontend dependencies
    npm install
    ```

3. **Environment Setup**

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

4. **Database Configuration**

    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=crime_map
    DB_USERNAME=your_username
    DB_PASSWORD=your_password
    ```

5. **Database Migration & Seeding**

    ```bash
    php artisan migrate
    php artisan db:seed
    ```

6. **Build Assets**

    ```bash
    npm run build
    # atau untuk development
    npm run dev
    ```

7. **Run Application**

    ```bash
    php artisan serve
    ```

    Akses aplikasi di: `http://localhost:8000`

### Default Login

```
Email: admin@example.com
Password: password
```

---

## 🗂️ Struktur Project

```
crime-map/
├── 📁 app/
│   ├── 📁 Http/Controllers/     # API & Web Controllers
│   ├── 📁 Models/              # Eloquent Models
│   └── 📁 Providers/           # Service Providers
├── 📁 database/
│   ├── 📁 migrations/          # Database migrations
│   ├── 📁 seeders/             # Data seeders
│   └── 📁 data/               # Indonesian region data
├── 📁 resources/
│   ├── 📁 js/
│   │   ├── 📁 components/      # Vue components
│   │   ├── 📁 pages/          # Inertia pages
│   │   ├── 📁 layouts/        # Page layouts
│   │   └── 📁 types/          # TypeScript types
│   └── 📁 css/                # Stylesheets
├── 📁 routes/
│   ├── web.php                # Web routes
│   └── auth.php               # Auth routes
└── 📁 public/
    └── 📁 build/              # Compiled assets
```

---

## 🔧 Development

### Development Commands

```bash
# Start development server
npm run dev
php artisan serve

# Build for production
npm run build

# Clear caches
php artisan optimize:clear

# Run tests
php artisan test

# Code formatting
npm run lint
```

### Database Seeding

```bash
# Seed Indonesian regions
php artisan db:seed --class=ProvinsiSeeder
php artisan db:seed --class=KabupatenKotaSeeder
php artisan db:seed --class=KecamatanSeeder

# Seed sample crime data
php artisan db:seed --class=CrimeDataSeeder
```

---

## 🌐 API Endpoints

### Public APIs

```
GET /api/provinsi              # Get all provinces
GET /api/kabupaten-kota/{id}   # Get regencies by province
GET /api/kecamatan/{id}        # Get districts by regency
```

### Web Routes

```
GET /dashboard                 # Main dashboard
GET /crime-data               # Crime data management
GET /crime-data/create        # Add new crime data
GET /crime-data/{id}/edit     # Edit crime data
GET /provinsi                 # Province management
GET /kabupaten-kota           # Regency management
GET /kecamatan                # District management
```

---

## 🚀 Deployment

### Shared Hosting Deployment

Ikuti panduan lengkap di [DEPLOYMENT.md](./DEPLOYMENT.md)

### Quick Deployment Checklist

- [ ] Build assets: `npm run build`
- [ ] Cache configs: `php artisan optimize`
- [ ] Upload files sesuai struktur
- [ ] Configure database
- [ ] Set file permissions
- [ ] Run migrations
- [ ] Test functionality

---

## 📊 Database Schema

### Main Tables

- **provinces** - 38 provinsi Indonesia
- **regencies** - 514+ kabupaten/kota
- **districts** - 7,288+ kecamatan
- **crime_data** - Data kejahatan dengan koordinat
- **users** - User management

### Relationships

```
provinces (1) → (n) regencies (1) → (n) districts (1) → (n) crime_data
```

---

## 🤝 Contributing

Kontribusi sangat diterima! Silakan:

1. Fork repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

### Development Guidelines

- Follow PSR-12 coding standards
- Use TypeScript untuk type safety
- Write meaningful commit messages
- Add tests untuk fitur baru
- Update documentation

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

## 👥 Authors & Contributors

- **Aditya AK** - _Initial work_ - [@aadiityaak](https://github.com/aadiityaak)

---

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/aadiityaak/crime-map/issues)
- **Discussions**: [GitHub Discussions](https://github.com/aadiityaak/crime-map/discussions)
- **Email**: aadiityaak@gmail.com

---

## 🙏 Acknowledgments

- Data wilayah Indonesia dari [kemendagri.go.id](https://kemendagri.go.id)
- Icons by [Lucide](https://lucide.dev)
- Maps by [OpenStreetMap](https://openstreetmap.org)
- UI components by [shadcn/ui](https://ui.shadcn.com)

---

<div align="center">

**⭐ Jika project ini membantu, berikan star di GitHub! ⭐**

Made with ❤️ for Indonesia

</div>
