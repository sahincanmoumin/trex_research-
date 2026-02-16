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
