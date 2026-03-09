# MERN Stack Katmanlı Mimari Projesi

Bu proje, **MERN Stack (MongoDB, Express.js, React, Node.js)** kullanılarak geliştirilmiş, profesyonel bir katmanlı mimari (Layered Architecture) örneğidir. Projenin temel amacı, ölçeklenebilir ve sürdürülebilir bir yazılım yapısı kurarak güvenli bir kullanıcı yönetim sistemi sunmaktır.

## 🚀 Özellikler

- **Katmanlı Mimari:** Logic, veri erişimi ve sunum katmanlarının birbirinden ayrıldığı modüler yapı.
- **Güvenli Kimlik Doğrulama:** JWT (JSON Web Token) tabanlı oturum yönetimi.
- **Şifre Güvenliği:** `bcrypt` ile şifrelerin güvenli bir şekilde hashlenmesi.
- **Girdi Doğrulama:** `express-validator` ile API isteklerinin doğrulanması.
- **Mimari Görselleştirme:** Uygulama içindeki `/architecture` rotasında projenin teknik yapısını görsel olarak sunan özel bir sayfa.
- **Güvenlik Katmanları:** Helmet, CORS ve Rate Limiting entegrasyonu.

## 🛠️ Kullanılan Teknolojiler

### Backend
- **Node.js & Express.js:** Sunucu ortamı ve API yönetimi.
- **MongoDB & Mongoose:** NoSQL veri tabanı ve nesne modelleme.
- **JWT & bcrypt:** Kimlik doğrulama ve veri güvenliği.
- **express-validator:** Middleware tabanlı doğrulama.
- **Helmet & Rate Limit:** Güvenlik sıkılaştırmaları.

### Frontend
- **React:** Kullanıcı arayüzü kütüphanesi.
- **React Router:** SPA (Single Page Application) yönlendirme.
- **Axios:** HTTP istemcisi.
- **CSS3:** Modern ve kullanıcı dostu arayüz tasarımı.

## 🏗️ Mimari Yapı

Proje şu akış üzerine inşa edilmiştir:
`Client → Controller → Service → Repository → Database`

### Klasör Yapısı
```text
.
├── backend                 # Sunucu tarafı kodları
│   ├── src
│   │   ├── controllers     # İstekleri karşılayan ve yanıt veren katman
│   │   ├── services        # İş mantığının (Business Logic) bulunduğu katman
│   │   ├── repositories    # Veri tabanı işlemlerinin yapıldığı katman
│   │   ├── models          # Mongoose şemaları
│   │   ├── routes          # API uç noktaları (Endpoints)
│   │   ├── middleware      # Ara yazılımlar (Auth, vb.)
│   │   ├── validators      # Veri doğrulama şemaları
│   │   ├── config          # Veri tabanı ve çevre ayarları
│   │   └── utils           # Yardımcı araçlar
├── frontend                # İstemci tarafı kodları
│   ├── src
│   │   ├── pages           # Sayfa bileşenleri (Home, Architecture, Users, vb.)
│   │   ├── components      # Tekrar kullanılabilir arayüz öğeleri
│   │   ├── services        # API çağrılarını yöneten servisler
│   │   ├── hooks           # Özel React hookları
│   │   └── utils           # Yardımcı fonksiyonlar
```

## ⚙️ Kurulum ve Çalıştırma

### Gereksinimler
- Node.js (v14 veya üzeri)
- MongoDB (Yerel veya Atlas)

### 1. Projeyi Klonlayın veya İndirin
```bash
git clone <proje-url>
cd mern-architecture-project
```

### 2. Backend Kurulumu
```bash
cd backend
npm install
```
`.env` dosyasını oluşturun ve şu değişkenleri tanımlayın:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_super_secret_key
```
Backend'i çalıştırın:
```bash
npm run dev
```

### 3. Frontend Kurulumu
```bash
cd ../frontend
npm install
npm start
```

## 📊 Mimari Görselleştirme
Uygulama çalıştıktan sonra tarayıcınızda `http://localhost:3000/architecture` adresine giderek projenin katmanlı yapısını ve veri akış diyagramını inceleyebilirsiniz.

---
Bu proje bir web programlama ödevi kapsamında, en iyi yazılım pratikleri gözetilerek hazırlanmıştır.
