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

# Backend Geliştirme Temelleri

## Backend Nedir?

Backend, uygulamanın sunucu tarafında çalışan kısmıdır. Veritabanı işlemleri, iş kuralları ve API yönetimi burada yapılır.  
Frontend ise kullanıcının gördüğü arayüz kısmıdır. Backend veri üretir, frontend bu veriyi kullanıcıya gösterir.

---

## Web Sunucusu ve API

**Web sunucusu**, istemciden gelen istekleri karşılayan ve cevap dönen sistemdir.  
**API (Application Programming Interface)**, uygulamaların birbiriyle haberleşmesini sağlayan arayüzdür.

### API Türleri
- REST API
- SOAP API
- GraphQL API

---

## HTTP Nedir?

HTTP (HyperText Transfer Protocol), istemci ile sunucu arasındaki veri iletişim protokolüdür.

### HTTP Metodları

- **GET** → Veri almak için kullanılır.  
- **POST** → Yeni veri eklemek için kullanılır.  
- **PUT** → Var olan veriyi güncellemek için kullanılır.  
- **DELETE** → Veri silmek için kullanılır.  

---

## RESTful Servislerin Çalışma Mantığı

REST, HTTP metodlarını kullanarak kaynak (resource) tabanlı çalışan bir servis mimarisidir.  
Her kaynak bir URL ile temsil edilir ve işlemler HTTP metodları ile yapılır.  
Stateless yapıya sahiptir, yani her istek bağımsızdır.

---

## JSON Veri Formatı

JSON (JavaScript Object Notation), veri taşımak için kullanılan hafif ve okunabilir bir formattır. API’lerde yaygın olarak kullanılır.

### JSON Örneği

```json
{
  "id": 1,
  "name": "Ahmet",
  "email": "ahmet@mail.com"
}
```

JSON, frontend ile backend arasında veri alışverişini kolaylaştırır.

---

## REST vs SOAP vs GraphQL Karşılaştırması

| Özellik | REST | SOAP | GraphQL |
|----------|------|------|----------|
| Veri Formatı | Genellikle JSON | XML | JSON |
| Protokol | HTTP | HTTP, SMTP vb. | HTTP |
| Esneklik | Orta | Düşük | Yüksek |
| Performans | Yüksek | Daha düşük | İhtiyaca göre optimize |

### Temel Farklar

- **REST** → Basit ve hafif yapı, yaygın kullanım.
- **SOAP** → Daha katı kurallı ve güvenlik odaklı.
- **GraphQL** → İstemci sadece ihtiyaç duyduğu veriyi alır.

---

# ASP.NET

## ASP.NET ve ASP.NET Core

**ASP.NET**, Microsoft’un web uygulamaları geliştirmek için oluşturduğu framework’tür ve klasik sürümü .NET Framework’e bağlıdır (Windows bağımlı).

**ASP.NET Core**, açık kaynaklı, yüksek performanslı ve platformlar arası (Windows, Linux, macOS) çalışan modern sürümdür. Günümüzde yeni projelerde ASP.NET Core tercih edilir.

Avantajları:
- Yüksek performans
- Cross-platform destek
- Dahili Dependency Injection desteği
- Middleware mimarisi

---

## MVC Nedir?

MVC (Model-View-Controller), uygulamayı üç ana bölüme ayıran bir tasarım desenidir:

- **Model** → Veri ve iş kuralları
- **View** → Kullanıcı arayüzü
- **Controller** → İstekleri karşılayan ve yöneten yapı

Amaç: Kodun düzenli, sürdürülebilir ve test edilebilir olmasıdır.

---

## Middleware Nedir?

Middleware, HTTP isteği ile response arasında çalışan ara yazılımlardır.  
İstek pipeline mantığıyla sırayla çalışırlar.

### Program.cs İçinde Middleware Sıralaması Örneği

```csharp
var app = builder.Build();

app.UseRouting();
app.UseAuthentication();
app.UseAuthorization();
app.MapControllers();

app.Run();
```

Çalışma sırası yukarıdan aşağıdır. Yanlış sıralama hataya neden olabilir.

---

## Dependency Injection (DI) Nedir?

DI, bir sınıfın bağımlılıklarını dışarıdan alması prensibidir.  
Amaç: Gevşek bağlı (loosely coupled) ve test edilebilir kod yazmaktır.

### DI Örneği

```csharp
builder.Services.AddScoped<IUserService, UserService>();
```

Controller içinde kullanım:

```csharp
public class UsersController : ControllerBase
{
    private readonly IUserService _userService;

    public UsersController(IUserService userService)
    {
        _userService = userService;
    }
}
```

---

# Katmanlı Mimari (Layered Architecture)

Katmanlı mimari uygulamayı sorumluluklarına göre ayırır.

- **Presentation** → API veya UI katmanı
- **Business** → İş kuralları
- **Data Access** → Veritabanı işlemleri

### Service & Repository Pattern

- **Repository** → Veritabanı işlemlerini yönetir.
- **Service** → İş kurallarını içerir ve Repository’yi kullanır.

Akış:
Presentation → Service → Repository → Database

---

# Clean Architecture

Clean Architecture, bağımlılıkların merkeze doğru değil dışa doğru olması prensibine dayanır.

Katmanlar:
- **Domain** → Temel iş kuralları
- **Application** → Use-case ve servisler
- **Infrastructure** → Veritabanı, dış servisler
- **API** → Controller katmanı

Bağımlılık yönü:

API → Application → Domain  
Infrastructure → Application → Domain  

Merkezde Domain bulunur ve en bağımsız katmandır.

# Veritabanı ve ORM

## SQL Nedir?

SQL (Structured Query Language), ilişkisel veritabanlarıyla iletişim kurmak için kullanılan sorgu dilidir. Veri ekleme, silme, güncelleme ve listeleme işlemleri SQL ile yapılır.

---

## İlişkisel ve İlişkisel Olmayan Veritabanları

**İlişkisel veritabanları (RDBMS)** tablo yapısında çalışır ve veriler arasında ilişkiler bulunur.  
Örnek: MSSQL, MySQL, PostgreSQL.

**İlişkisel olmayan (NoSQL)** veritabanları esnek veri yapısına sahiptir (JSON, belge, key-value).  
Örnek: MongoDB.

| Özellik | İlişkisel | NoSQL |
|----------|------------|--------|
| Veri Yapısı | Tablo | Doküman / Key-Value |
| Şema | Sabit | Esnek |
| İlişki | Var | Genelde yok |

---

## ORM ve Entity Framework Core

**ORM (Object Relational Mapping)**, veritabanı tablolarını C# sınıflarına eşleyen yapıdır. SQL yazmadan veri işlemi yapmayı sağlar.

**Entity Framework Core (EF Core)**, .NET için geliştirilmiş modern ORM aracıdır.

---

## DbContext Nedir?

DbContext, veritabanı ile uygulama arasındaki ana bağlantıdır.  
Tablolar DbSet olarak tanımlanır.

```csharp
public class AppDbContext : DbContext
{
    public DbSet<User> Users { get; set; }
}
```

---

## LINQ Nedir?

LINQ (Language Integrated Query), C# içinde veri sorgulamayı sağlayan yapıdır.

### LINQ Örnekleri ve SQL Karşılıkları

**Tüm kullanıcıları listeleme**

LINQ:
```csharp
var users = context.Users.ToList();
```

SQL:
```sql
SELECT * FROM Users;
```

**Şartlı veri çekme**

LINQ:
```csharp
var user = context.Users.Where(u => u.Id == 1).FirstOrDefault();
```

SQL:
```sql
SELECT * FROM Users WHERE Id = 1;
```

**En Çok Kullanılan LINQ İfadeleri**
- Where()
- Select()
- FirstOrDefault()
- ToList()
- OrderBy()

---

## Code-First ve Database-First

**Code-First** yaklaşımında önce C# sınıfları yazılır, veritabanı migration ile oluşturulur.

**Database-First** yaklaşımında önce veritabanı oluşturulur, ardından model sınıfları otomatik üretilir.

| Özellik | Code-First | Database-First |
|----------|------------|----------------|
| Başlangıç | Kod | Veritabanı |
| Kontrol | Geliştiricide | Veritabanında |
| Kullanım | Yeni projeler | Mevcut DB projeleri |

---

## Temel SQL Sorguları

**SELECT** → Veri listeleme  
```sql
SELECT * FROM Users;
```

**INSERT** → Yeni veri ekleme  
```sql
INSERT INTO Users (Name, Email)
VALUES ('Ahmet', 'ahmet@mail.com');
```

**UPDATE** → Veri güncelleme  
```sql
UPDATE Users
SET Name = 'Ahmet Yılmaz'
WHERE Id = 1;
```

**DELETE** → Veri silme  
```sql
DELETE FROM Users
WHERE Id = 1;
```
---
# Güvenlik ve Performans

## Authentication vs Authorization

**Authentication (Kimlik Doğrulama)**, kullanıcının kim olduğunu doğrulama işlemidir.  
Örnek: Kullanıcı adı ve şifre ile giriş yapmak.

**Authorization (Yetkilendirme)**, doğrulanmış kullanıcının hangi işlemleri yapabileceğini belirler.  
Örnek: Admin kullanıcının veri silebilmesi.

---

## JWT (JSON Web Token) Nedir?

JWT, kullanıcı doğrulama ve yetkilendirme için kullanılan token tabanlı güvenlik mekanizmasıdır. Kullanıcı giriş yaptıktan sonra sunucu bir token üretir ve istemci her istekte bu token’ı gönderir.

### JWT Yapısı

JWT üç bölümden oluşur:

- **Header** → Kullanılan algoritma bilgisi
- **Payload** → Kullanıcı bilgileri (claim)
- **Signature** → Güvenlik imzası

Yapı:
Header.Payload.Signature

---

## OAuth, OAuth2.0, OpenID ve OpenIddict

- **OAuth** → Yetkilendirme protokolüdür.
- **OAuth 2.0** → OAuth’un geliştirilmiş sürümüdür.
- **OpenID** → Kimlik doğrulama katmanıdır.
- **OpenIddict** → .NET için OpenID Connect ve OAuth 2.0 implementasyonudur.

İlişki:
OAuth → Yetkilendirme  
OpenID → Kimlik doğrulama  
OAuth 2.0 + OpenID Connect → Modern kimlik sistemleri

---

# Performans Artırma Teknikleri

## 1. AsNoTracking()

Entity Framework’te sadece okuma işlemlerinde kullanılır. Change tracking kapatıldığı için performans artar.

## 2. IAsyncEnumerable

Büyük veri setlerini parça parça asenkron olarak okumayı sağlar. Bellek kullanımını azaltır.

## 3. Caching

Sık kullanılan verilerin geçici olarak bellekte tutulmasıdır. Veritabanı yükünü azaltır.

## 4. Redis

Dağıtık cache sistemidir. Özellikle yüksek trafikli uygulamalarda performansı artırır.

## 5. Profiling

Uygulamanın yavaş çalışan sorgularını ve darboğazlarını analiz etmeyi sağlar.

---

# OWASP Top 10

OWASP, web uygulamalarındaki en yaygın güvenlik açıklarını listeleyen bir güvenlik rehberidir.

## 1. Broken Access Control
Yetkisiz kullanıcıların korumalı verilere erişebilmesi.

## 2. Cryptographic Failures
Şifreleme hataları nedeniyle hassas verilerin açığa çıkması.

## 3. Injection
Kötü amaçlı kod enjeksiyonu. (Örnek: SQL Injection)

## 4. Insecure Design
Güvensiz mimari tasarım hataları.

## 5. Security Misconfiguration
Yanlış yapılandırılmış sunucu veya uygulama ayarları.

## 6. Vulnerable Components
Güncel olmayan veya güvenlik açığı bulunan kütüphaneler.

## 7. Identification and Authentication Failures
Zayıf kimlik doğrulama mekanizmaları (Broken Auth).

## 8. Software and Data Integrity Failures
Veri bütünlüğü ihlalleri.

## 9. Security Logging and Monitoring Failures
Yetersiz loglama ve izleme.

## 10. Server-Side Request Forgery (SSRF)
Sunucunun kötü amaçlı isteklere yönlendirilmesi.

---

## Yaygın Güvenlik Açıkları

**SQL Injection** → Zararlı SQL sorgularının sisteme enjekte edilmesi.  
Önlem: Parametreli sorgular ve EF kullanımı.

**XSS (Cross-Site Scripting)** → Zararlı script kodlarının kullanıcıya çalıştırılması.  
Önlem: Input validation ve output encoding.

**CSRF (Cross-Site Request Forgery)** → Kullanıcının haberi olmadan işlem yapılması.  
Önlem: Anti-forgery token kullanımı.

---

## ASP.NET Core ile Alınabilecek Önlemler

- Model Validation kullanmak  
- Data Annotation ile input kontrolü  
- HTTPS zorunlu kılmak  
- JWT doğrulaması yapmak  
- Role bazlı yetkilendirme uygulamak  
- Input sanitization yapmak  

---
# Logging ve Hata Yönetimi

## Neden Loglama Yapılır?

Loglama, uygulamada gerçekleşen olayların kayıt altına alınmasını sağlar.  
Amaç:

- Hataları tespit etmek
- Sistem davranışını analiz etmek
- Performans sorunlarını incelemek
- Güvenlik olaylarını takip etmek

---

## Log Seviyeleri

ASP.NET Core’da loglar önem derecesine göre seviyelendirilir:

- **Trace** → En detaylı log seviyesi (geliştirme aşaması).
- **Debug** → Hata ayıklama amaçlı bilgiler.
- **Information** → Uygulamanın normal çalışma bilgileri.
- **Warning** → Potansiyel sorunlar.
- **Error** → İşlemin başarısız olduğu hatalar.
- **Critical** → Sistemin durmasına neden olabilecek ciddi hatalar.

---

## ASP.NET Core’da Logging Altyapısı

ASP.NET Core’da logging altyapısı dahili olarak gelir ve `ILogger` arayüzü ile kullanılır.

### ILogger Kullanımı

```csharp
public class UsersController : ControllerBase
{
    private readonly ILogger<UsersController> _logger;

    public UsersController(ILogger<UsersController> logger)
    {
        _logger = logger;
    }

    public IActionResult Get()
    {
        _logger.LogInformation("Kullanıcı listesi getirildi.");
        return Ok();
    }
}
```

---

## Global Exception Handling

Global exception handling, uygulamadaki tüm hataları merkezi bir noktada yakalamayı sağlar. Böylece her controller içinde try-catch yazmak gerekmez.

### UseExceptionHandler Kullanımı

Program.cs içinde:

```csharp
app.UseExceptionHandler("/error");
```

Controller içinde:

```csharp
[Route("/error")]
public IActionResult HandleError()
{
    return Problem("Beklenmeyen bir hata oluştu.");
}
```

---

## Örnek Hata Yönetimi Açıklaması

Bir API endpoint’inde hata oluştuğunda:

- Hata global handler tarafından yakalanır.
- ILogger ile hata loglanır.
- Kullanıcıya detay vermeden standart bir hata mesajı döndürülür.

Bu yaklaşım:
- Güvenliği artırır
- Kod tekrarını azaltır
- Merkezi hata yönetimi sağlar

---
# Yazılım Geliştirme Prensipleri

## SOLID Prensipleri

### 1. Single Responsibility Principle (SRP)
Bir sınıfın yalnızca tek bir sorumluluğu olmalıdır.

Yanlış:
```csharp
class UserService {
    public void SaveUser() {}
    public void SendEmail() {}
}
```

Doğru: Email işlemi ayrı sınıfa taşınmalıdır.

---

### 2. Open/Closed Principle (OCP)
Sınıflar geliştirmeye açık, değişikliğe kapalı olmalıdır.

Örnek: Yeni ödeme türü eklerken mevcut kodu değiştirmek yerine yeni bir sınıf eklemek.

---

### 3. Liskov Substitution Principle (LSP)
Türetilen sınıflar, türediği sınıfın yerine sorunsuz kullanılabilmelidir.

---

### 4. Interface Segregation Principle (ISP)
Sınıflar kullanmadıkları metotlara bağımlı olmamalıdır.

---

### 5. Dependency Inversion Principle (DIP)
Yüksek seviye sınıflar düşük seviyelere değil, soyutlamalara bağımlı olmalıdır.

Örnek:
```csharp
public class OrderService {
    private readonly IPaymentService _payment;
    public OrderService(IPaymentService payment) {
        _payment = payment;
    }
}
```

---

# Design Patterns

## Singleton
Bir sınıftan yalnızca bir nesne oluşturulmasını sağlar.

Kullanım: Logger veya configuration sınıfları.

---

## Repository
Veritabanı işlemlerini soyutlamak için kullanılır.  
Business katmanı doğrudan DB ile iletişime geçmez.

---

## Factory
Nesne oluşturma işlemini merkezi bir yapıya taşır.  
Hangi nesnenin üretileceğini factory belirler.

---

# Clean Code

Clean Code, okunabilir, anlaşılır ve sürdürülebilir kod yazma yaklaşımıdır.

Neden önemlidir?
- Kod bakımı kolaylaşır
- Hata oranı azalır
- Takım çalışması kolaylaşır

### Clean Code Örneği

Kötü:
```csharp
int x;
```

İyi:
```csharp
int userAge;
```

Açıklayıcı değişken isimleri kullanılmalıdır.

---

# Yazılım Mimari Desenleri

| Mimari | Açıklama | Tercih Edilen Senaryo |
|---------|----------|------------------------|
| Layered | Katmanlı yapı (UI, Business, Data) | Küçük/Orta ölçekli projeler |
| Clean Architecture | Bağımlılıklar merkeze doğru | Test edilebilir büyük projeler |
| Microservices | Servislerin bağımsız çalışması | Büyük ve dağıtık sistemler |
| Event-Driven | Olay tabanlı iletişim | Gerçek zamanlı sistemler |
| Hexagonal | Ports & Adapters yapısı | Bağımlılık izolasyonu gereken projeler |

---

## Hangi Mimari Ne Zaman?

- Basit kurumsal uygulama → Layered
- Test odaklı ve sürdürülebilir sistem → Clean Architecture
- Büyük ve ölçeklenebilir sistem → Microservices
- Gerçek zamanlı bildirim sistemi → Event-Driven
- Dış servis bağımlılığı yüksek sistem → Hexagonal
```


