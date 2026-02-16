# trex_research-

# Modern Yazılım Geliştirme Teknikleri

## Git ve GitHub

### Git Nedir?

Git, dağıtık bir versiyon kontrol sistemidir.  
Ekip çalışmalarında kod karmaşasını önleyen en temel araçtır.

### GitHub Nedir?

GitHub, Git repository’lerini internet üzerinde barındıran bir platformdur.

---

## Temel Git Komutları

- `git init` → Yeni repository oluşturur
- `git clone` → Uzak repo’yu bilgisayara kopyalar
- `git add` → Değişiklikleri stage alanına alır
- `git commit` → Değişiklikleri kaydeder
- `git push` → Değişiklikleri remote’a gönderir
- `git pull` → Remote’daki değişiklikleri çeker
- `git branch` → Yeni branch oluşturur
- `git merge` → Branch’leri birleştirir

---

## Merge Conflict Nedir?

Merge conflict, iki farklı branch'te aynı dosyanın aynı satırları değiştirildiğinde ve Git bunları otomatik birleştiremediğinde oluşur.

### Çözüm Yolları

1. Manuel düzenleme
2. IDE/Editor araçları kullanma
3. `git merge --abort` ile işlemi iptal etme

---

## CI/CD

CI/CD, kodun otomatik olarak build edilmesi, test edilmesi ve deploy edilmesi sürecidir.  
Bu süreç insan hatasını azaltır ve yazılımın sürekli çalışabilir durumda kalmasını sağlar.

### .NET Projesinde CI/CD Uygulaması

Bir .NET Web API projesinde tipik pipeline adımları:

1. Kod push edilir
2. `dotnet restore`
3. `dotnet build`
4. Testler çalıştırılır
5. `dotnet publish`
6. Sunucuya deploy edilir

---

## Software Development Life Cycle (SDLC)

SDLC, yazılım geliştirme sürecinin planlı ve sistematik şekilde yürütülmesidir.

### SDLC Aşamaları

1. **Planlama** – Proje kapsamı ve gereksinimler belirlenir.
2. **Analiz** – Teknik ve iş gereksinimleri detaylandırılır.
3. **Geliştirme** – Kod yazımı yapılır.
4. **Test** – Hatalar kontrol edilir.
5. **Dağıtım (Deployment)** – Uygulama canlı ortama alınır.
6. **Bakım** – Hata düzeltmeleri ve iyileştirmeler yapılır.

---

## Agile, Scrum ve Kanban

### Agile

Esnek ve iteratif geliştirme yaklaşımıdır.

### Scrum

Sprint mantığıyla çalışan Agile metodolojisidir.  
Günlük toplantılar ve sprint planlaması içerir.

### Kanban

Görevlerin görsel bir tahta üzerinde yönetildiği sistemdir.

---

# .NET Platformu

## .NET Nedir?

.NET, Microsoft tarafından geliştirilen açık kaynaklı bir yazılım geliştirme platformudur. Web, masaüstü, mobil, oyun ve bulut tabanlı uygulamalar geliştirmek için kullanılır.

### Tarihçesi

- 2002 yılında .NET Framework olarak yayınlandı.
- 2016 yılında .NET Core ile platform bağımsız hale geldi.
- .NET 5 ile Framework ve Core yapıları birleştirildi.
- Günümüzde .NET 7/8+ modern ve birleşik sürümler olarak devam etmektedir.

### Amacı

- Farklı platformlarda çalışabilen uygulamalar geliştirmek  
- Yüksek performans ve güvenlik sağlamak  
- Modern yazılım geliştirme standartlarını desteklemek  

### Neden Kullanılır?

- Kurumsal projelerde yaygın olması  
- Güçlü C# dili desteği  
- Geniş kütüphane ve araç ekosistemi  
- Performanslı Web API geliştirme imkanı  

---

## .NET Framework, .NET Core ve .NET 7/8+ Farkları

| Özellik | .NET Framework | .NET Core | .NET 7/8+ |
|----------|----------------|------------|------------|
| Çıkış Yılı | 2002 | 2016 | 2022+ |
| Platform | Sadece Windows | Windows, Linux, macOS | Windows, Linux, macOS |
| Açık Kaynak | Hayır | Evet | Evet |
| Performans | Orta | Yüksek | Daha yüksek |
| Güncellik | Eski | Aktif | En güncel |

---

## Platformlar Arası Çalışabilir mi?

Evet. Modern .NET sürümleri aşağıdaki işletim sistemlerinde çalışabilir:

- Windows  
- Linux  
- macOS  

Bu özellik sayesinde aynı proje farklı işletim sistemlerinde yeniden yazılmadan çalıştırılabilir.

## Senkron ve Asenkron Programlama

**Senkron programlama**, işlemlerin sırayla ve birbirini bekleyerek çalıştığı yapıdır. Bir işlem bitmeden diğeri başlamaz. Uzun süren işlemlerde uygulamanın yavaşlamasına neden olabilir.

**Asenkron programlama**, uzun süren işlemleri beklemeden diğer işlemlerin çalışmasına devam edilmesini sağlar. Özellikle veritabanı ve API çağrılarında performans avantajı sağlar.

### Temel Kavramlar

- **async** → Metodun asenkron çalışacağını belirtir.
- **await** → Asenkron işlemin tamamlanmasını bekler ancak thread’i bloklamaz.
- **Task** → Asenkron işlemi temsil eder.
- **ConfigureAwait(false)** → Mevcut context’e dönmeyi engelleyerek performans iyileştirmesi sağlar.

### Arrow Function (=>) C#’taki Yeri

C#’ta `=>` ifadesi lambda expression ve expression-bodied member tanımlamak için kullanılır. Daha kısa ve okunabilir kod yazmayı sağlar.

```csharp
int Topla(int a, int b) => a + b;

## dotnet --info Çıktısı Örneği ve Yorumlama

Aşağıda örnek bir `dotnet --info` çıktısı bulunmaktadır:

```bash
.NET SDK:
 Version:   8.0.100
 Commit:    abcdef123

Runtime Environment:
 OS Name:     Windows
 OS Version:  10.0.19045
 OS Platform: Windows
 RID:         win-x64
 Base Path:   C:\Program Files\dotnet\sdk\8.0.100\

Host:
  Version:      8.0.0
  Architecture: x64

.NET SDKs installed:
  7.0.400 [C:\Program Files\dotnet\sdk]
  8.0.100 [C:\Program Files\dotnet\sdk]

.NET runtimes installed:
  Microsoft.NETCore.App 7.0.10
  Microsoft.NETCore.App 8.0.0
```

### Yorumlama

- **SDK Version** → Yüklü olan .NET SDK sürümünü gösterir (proje geliştirmek için kullanılır).
- **Runtime** → Uygulamayı çalıştırmak için gereken ortamdır.
- **OS Platform** → İşletim sistemini belirtir.
- **SDKs installed** → Bilgisayarda yüklü tüm SDK sürümleri.
- **Runtimes installed** → Yüklü olan çalışma zamanı sürümleri.

---


