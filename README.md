<div align="center">

# 🔄 Loopa

### İkinci El ve Ücretsiz Paylaşım Platformu

[![Live Demo](https://img.shields.io/badge/🌐_Canlı_Demo-Ziyaret_Et-success?style=for-the-badge)](https://hsd-proje-front.vercel.app/)
[![API Docs](https://img.shields.io/badge/📚_API_Docs-Swagger-blue?style=for-the-badge)](https://hsd-proje.onrender.com/docs)

[![Next.js](https://img.shields.io/badge/Next.js-16.1-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.127-009688?style=flat-square&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Latest-FFCA28?style=flat-square&logo=firebase)](https://firebase.google.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=flat-square&logo=python)](https://www.python.org/)

**Sürdürülebilir tüketimi teşvik eden, kullanıcıların ikinci el eşyalarını paylaşabileceği, bağışlayabileceği veya satın alabileceği modern bir sosyal paylaşım platformu.**

[🌐 Canlı Demo](https://hsd-proje-front.vercel.app/) • [📚 API Dokümantasyonu](https://hsd-proje.onrender.com/docs) • [🎨 Tasarım](https://stitch.withgoogle.com/projects/9756006167165370596)

</div>

---

## 📖 Proje Hakkında

Loopa, çevre dostu bir yaklaşımla ikinci el eşya paylaşımını kolaylaştıran bir platformdur. Kullanıcılar eşyalarını bağışlayabilir, satabilir veya destek talebinde bulunabilir. Platform, karbon ayak izini azaltmayı ve topluluk dayanışmasını güçlendirmeyi hedefler.

### ✨ Temel Özellikler

- 🔐 **Güvenli Kimlik Doğrulama**: Firebase Authentication
- 📝 **İlan Yönetimi**: Bağış, satış ve destek talepleri
- 🗺️ **Konum Tabanlı Arama**: Yakınındaki ilanları keşfet
- 💬 **Gerçek Zamanlı Mesajlaşma**: Kullanıcılar arası iletişim
- 📊 **Karbon Ayak İzi Takibi**: Çevresel etki ölçümü
- 🎨 **Modern Arayüz**: Responsive ve kullanıcı dostu tasarım

---

## 🛠️ Teknolojiler

### Frontend
- **Next.js 16.1** - React framework
- **React 19** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Leaflet** - Harita entegrasyonu

### Backend
- **FastAPI** - Python web framework
- **Python 3.13** - Backend language
- **Firebase Firestore** - NoSQL database
- **Firebase Auth** - Kimlik doğrulama
- **Pydantic** - Data validation

---

## 🚀 Kurulum ve Çalıştırma

### Gereksinimler

- Node.js 20+
- Python 3.13+
- Firebase projesi

### 1. Projeyi Klonlayın

```bash
git clone https://github.com/AlbayEmre/Loopa.git
cd Loopa
```

### 2. Backend Kurulumu

```bash
cd backend

# Virtual environment oluştur
python -m venv venv

# Aktifleştir (Windows)
venv\Scripts\activate

# Bağımlılıkları yükle
pip install -r requirements.txt

# .env dosyası oluştur
cp .env.example .env
# .env dosyasını düzenleyip Firebase credentials'larınızı ekleyin

# Sunucuyu başlat
uvicorn app.main:app --reload
```

Backend: `http://localhost:8000`

### 3. Frontend Kurulumu

```bash
cd ../frontend

# Bağımlılıkları yükle
npm install

# .env.local dosyası oluştur
cp env.example .env.local
# .env.local dosyasını düzenleyip Firebase config'inizi ekleyin

# Geliştirme sunucusunu başlat
npm run dev
```

Frontend: `http://localhost:3000`

---

## 🔧 Yapılandırma

### Backend (.env)

Firebase Console'dan aldığınız credentials'ları ekleyin:

```env
FIREBASE_PROJECT_ID=your-project-id
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n"
FIREBASE_CLIENT_EMAIL=firebase-adminsdk@your-project.iam.gserviceaccount.com
SECRET_KEY=your-secret-key
```

### Frontend (.env.local)

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_FIREBASE_API_KEY=your-api-key
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your-project-id
```

> **Not**: Firebase credentials almak için [Firebase Console](https://console.firebase.google.com/) > Project Settings > Service Accounts

---

## 📱 Kullanım

1. **Kayıt Ol / Giriş Yap**: Firebase Authentication ile güvenli giriş
2. **İlan Oluştur**: Bağışlamak veya satmak istediğiniz eşyayı ekleyin
3. **Keşfet**: Harita üzerinde yakınındaki ilanları görün
4. **Mesajlaş**: İlan sahipleriyle iletişime geçin
5. **İstatistikler**: Karbon tasarrufunuzu takip edin

---

## 🌐 Canlı Uygulama

- **Frontend**: [https://hsd-proje-front.vercel.app/](https://hsd-proje-front.vercel.app/)
- **Backend API**: [https://hsd-proje.onrender.com/](https://hsd-proje.onrender.com/)
- **API Docs**: [https://hsd-proje.onrender.com/docs](https://hsd-proje.onrender.com/docs)

---

## 📂 Proje Yapısı

```
Loopa/
├── backend/              # FastAPI backend
│   ├── app/
│   │   ├── main.py      # Ana uygulama
│   │   ├── routers/     # API endpoints
│   │   ├── models/      # Pydantic modeller
│   │   └── services/    # Business logic
│   ├── .env.example     # Environment template
│   └── requirements.txt # Python dependencies
│
├── frontend/            # Next.js frontend
│   ├── src/
│   │   ├── app/        # Pages (App Router)
│   │   ├── components/ # React components
│   │   └── lib/        # Utilities & API
│   ├── env.example     # Environment template
│   └── package.json    # Node dependencies
│
└── README.md
```

---

## 🔒 Güvenlik

> **⚠️ ÖNEMLİ**: `.env` ve `.env.local` dosyalarını asla Git'e commit etmeyin!

- JWT token authentication
- Firebase security rules
- Password hashing (bcrypt)
- Input validation
- CORS policy

---

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

---

<div align="center">

### 🌱 Sürdürülebilir bir gelecek için!

**Projeyi beğendiyseniz ⭐ vermeyi unutmayın!**

Made with ❤️ by [Emre Albay](https://github.com/AlbayEmre)

</div>
