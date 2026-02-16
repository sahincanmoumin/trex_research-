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

