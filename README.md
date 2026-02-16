# trex_research-


1. Modern Yazılım Geliştirme Teknikleri
1.1 Git ve GitHub


1.1.1 Git Nedir?

Git, dağıtık bir versiyon kontrol sistemidir. Ekip çalışmalarında kod karmaşasını önleyen en temel araçtır.


1.1.2. GitHub Nedir?

GitHub, Git repository’lerini internet üzerinde barındıran bir platformdur.


1.2 Temel Git komutları

git init → Yeni repository oluşturur
  
git clone → Uzak repo’yu bilgisayara kopyalar
  
git add → Değişiklikleri stage alanına alır
  
git commit → Değişiklikleri kaydeder
  
git push → Değişiklikleri remote’a gönderir
  
git pull → Remote’daki değişiklikleri çeker
  
git branch → Yeni branch oluşturur
  
git merge → Branch’leri birleştirir


1.3 Merge Conflict Nedir?

Merge conflict iki farklı branch'te aynı dosyanın aynı satırları değiştirildiğinde ve Git bunları otomatik birleştiremediğinde oluşur.

Çözüm yolları:

1.Manuel düzenleme
2.IDE/Editor araçları kullanmak
3.Abort etme

1.4 CI/CD 

CI/CD, kodun otomatik olarak build edilmesi, test edilmesi ve deploy edilmesi sürecidir. CI/CD süreçleri, insan hatasını azaltır ve yazılımın sürekli çalışabilir durumda kalmasını sağlar.

.NET Projesinde CI/CD Uygulaması

Bir .NET Web API projesinde pipeline adımları:

1.Kod push edilir

2.dotnet restore çalışır

3.dotnet build yapılır

4.Testler çalıştırılır

5.dotnet publish ile çıktı alınır

6.Sunucuya deploy edilir

