# SwiftUISQLiteBridgeWithFMDB

SwiftUI projelerinde **SQLite** kullanımı için köprü görevi gören bir çözüm. Bu proje, **FMDB** (Objective-C tabanlı SQLite kütüphanesi) ile SwiftUI arasında bağlantı kurmayı kolaylaştırır ve veritabanı işlemlerini daha hızlı bir şekilde gerçekleştirmenizi sağlar.

---

## Özellikler

- **FMDB Entegrasyonu**: SQLite işlemleri için güçlü ve güvenilir bir yapı.
- **CRUD Desteği**: Veri ekleme, okuma, güncelleme ve silme işlemleri.
- **SwiftUI Uyumlu**: Modern SwiftUI projelerinde kolay entegrasyon.
- **Esnek Tasarım**: Kolay özelleştirilebilir yapı.
- **Veritabanı Yönetimi**: SQLite veritabanlarının oluşturulması ve yönetimi için araçlar.

---

## Kurulum

### 1. **FMDB'yi Projeye Ekleme**

FMDB'yi kullanmak için Swift Package Manager (SPM) veya CocoaPods kullanabilirsiniz:

#### Swift Package Manager (SPM)
1. Xcode'da `File > Add Packages` menüsüne gidin.
2. Şu URL'yi ekleyin:
     ```
     https://github.com/ccgus/fmdb
     ```
3. `FMDB` paketini ekleyin.

#### CocoaPods
1. Projenizin `Podfile` dosyasına aşağıdaki satırı ekleyin:
     ```
     pod 'FMDB'
     ```

2. Terminalde aşağıdaki komutla kurun:
     ```
     pod install
     ```
