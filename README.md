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

#### Manuel Kurulum

Eğer Swift Package Manager veya CocoaPods kullanmak istemiyorsanız, FMDB kütüphanesini manuel olarak projenize ekleyebilirsiniz.

#### Adımlar:

1. **FMDB Dosyalarını İndirin**  
   FMDB'nin kaynak kodlarını [FMDB GitHub Repository](https://github.com/ccgus/fmdb)'sinden indirin veya bu projede yer alan `FMDB` klasörünü kullanabilirsiniz.

2. **FMDB Dosyalarını Projenize Ekleyin**  
   `FMDatabase.h`, `FMDatabase.m`, ve FMDB'ye ait diğer dosyaları projenizin klasörüne taşıyın.  
   - Xcode'da `File > Add Files to "ProjeAdı"` menüsünden dosyaları projeye ekleyin.

3. **Objective-C Bridging Header Oluşturma**  
   Eğer projeniz yalnızca Swift içeriyorsa, bir `Bridging Header` dosyası oluşturmanız gerekir. Bunu şu şekilde yapabilirsiniz:
   
   - Xcode'da `File > New > File > Header File` yolunu izleyin ve dosyanızı **ProjeAdı-Bridging-Header.h** olarak adlandırın.
   - Daha sonra proje ayarlarına gidin:
     - `Build Settings > Swift Compiler - General > Objective-C Bridging Header` kısmına **ProjeAdı-Bridging-Header.h** dosyasının yolunu ekleyin (örneğin: `ProjeAdı/ProjeAdı-Bridging-Header.h`).

4. **FMDB'yi Bridging Header'a Ekleyin**  
   `ProjeAdı-Bridging-Header.h` dosyasına şu satırı ekleyin:
   ```objective-c
   #import "FMDB.h"
