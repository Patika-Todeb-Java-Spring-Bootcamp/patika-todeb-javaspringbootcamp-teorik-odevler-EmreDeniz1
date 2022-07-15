# patika-todeb-javaspringbootcamp-teorik-odevler-EmreDeniz1
patika-todeb-javaspringbootcamp-teorik-odevler-EmreDeniz1 created by GitHub Classroom

## **IOC ve DI nedir**
Inversion of control, bir programın nesnelerinin veya bölümlerinin kontrolünü conteinerlara veya framework'e aktaran yazılım mühendisliği ilkesidir. Bu ilke çoğunlukla nesneye yönelik programlamada kullanılır. 
Kodumuzun istenilen kitaplığa çağrı yaptığı geleneksel programlamanın aksine, IoC, bir programın akışının kontrolünü framework'e teslim eder ve projeniz deki bağımlılıkların oluşturulmasını ve yönetilmesini geliştiricinin yerine, framework’ün yapması sağlar.

Dependecy Injection, IoC'yi uygulamak için kullanabileceğimiz bir şemadır.Nesneleri diğer nesnelerle bağlamak veya nesneleri diğer nesnelere "enjekte etmek", nesnelerin kendileri tarafından değil, bir assembler tarafından yapılır. Böylece bağımlılık azalır.

## **Spring Bean Scopes**

Beanlerimizin bir yaşam döngüsü vardır. Bu yaşam döngüsü çerçevesinde istediğimiz işlemleri yapması için Beanimizin kapsamını yani scope’unu belirlememiz gerekmektedir. Spring Beanlerimizdeki scopeleri Spring IoC containerı tarafından yönetilir ve beanlerimizdeki nesnelerin ne zaman ve nasıl oluşturulacağını belirler.

Scope Çeşitleri

singleton

Varsayılan olarak her bean Singleton’dur. Bu Bean’den sadece bir tane üretilir.

prototype

Bean’e istek geldiğinde oluşturulur. Her istekte farklı bir instance oluşturulur.

request

Web uygulamaları için kullanılır. Her HTTP isteği geldiğinde instance oluşturulur.

session

Web uygulamaları için kullanılır. Her HTTP session oluştuğunda instance oluşturulur.

globalSession

Web uygulamaları için kullanılır. Her HTTP isteği geldiğinde sadece bir tane instance oluşturulur.

## **What does @SpringBootAplication do**

@SpringBootApplication, sınıfın bir yapılandırma sınıfı olduğunu ve @EnableAutoConfiguration ve bileşende @ComponentScan açıklaması aracılığıyla tarama yoluyla otomatik yapılandırmayı tetiklediğini belirtir. Spring Uygulama Bağlamının otomatik yapılandırmasını sağlar. Birçok Spring Boot geliştiricisi main classına hep  @Configuration, @EnableAutoConfiguration ve @ComponentScan annotationu eklemesi sonucu, Spring Boot yukarıdaki annotationların hepsini ekleyen  @SpringBootApplication'ı sunmuştur.

## **Why Spring Boot over Spring?**

Kısaca, Spring Boot geliştirmeyi, test etmeyi ve canlıya geçmeyi daha kolay hale getiren Spring'in bir uzantısıdır. Alt sorularda daha detaylı açıklanacaktır.

## **What is Singleton and where to use it**

İsminden de anlaşılacağı üzere singleton tasarım deseni,  hazırlayacağımız sınıftan sadece bir örneğinin oluşturulmasını sağlar. Bu sayede nesnenin kopyalanmasını yada yeni bir tane oluşturmasını engeller ve nesneye ihtiyaç duyulduğunda o nesnenin daha önceden oluşturulan örneği çağırır.

Ne zaman kullanırız?

Veritabanı bağlantılarında, port bağlantılarında, yada dosya işlemleri gibi tek bir nesneye ihtiyaç duyduğumuz zamanlarda kullanırız.

Explain @RestController annotation in Spring Boot

Bu anotasyon ilgili sınıftaki bütün metodların birer REST servis noktası olmasını sağlar. Bu anotasyon aslında @Controller ve @ResponseBody anotasyonlarının bileşimi. 

@Controller annotationu, bildiğiniz gibi ilgili sınıfın bir controller sınıfı olduğunu belirtir.

@ResponseBody annotationu ise, isteğin cevaplandırılacağı methodun başına yazılır. Böylece nasıl mapping işlemi yapılmışsa, o adres parametreleri ile çağırıldığında ilgili methoda yönlendirilir ve method çalıştırılır.

RestController Sınıfın Metodlarında Kullanılan Anotasyonlar Nelerdir?
1. Get isteği için  @GetMapping 
2. Post isteği için @PostMapping 
3. Delete isteği için @DeleteMapping 

## **What is the primary difference between Spring and Spring Boot**

| SPRING | SPRING BOOT |
|--------|-------------|
| To run the Spring application, needed to set the server explicitly. | Spring Boot provides embedded servers such as Tomcat and Jetty etc. |
| To run the Spring application, a deployment descriptor is needed. | There is no requirement for a deployment descriptor. |
| To create a Spring application, needed to write boilerplate code. | It eliminates most of the boilerplate code. |
| It doesn’t provide support for the in-memory database. | It provides support for the in-memory database, such as H2. |
| It creates a loosely coupled application. | It creates a stand-alone application. |

## **Why to use VCS**

Sürüm Kontrolü, kaynak koddaki değişiklikleri izlemek ve kontrol etmek için kullanılır.  Sürüm Kontrol Sistemi (VCS) olmadan karmaşık kod geliştirme neredeyse imkansızdır.  Projelerde VCS kullanmanın çeşitli avantajları vardır:

-Ekip ile işbirliği

-Kim, Ne, Ne Zaman, Neden cevaplarıyla yapılan değişiklikler

-Sürümleri doğru şekilde depolamak

-Önceki sürümleri kolayca geri yükleme

-Kısa açıklamalarla ve hatta içindeki metin dosyalarıyla daha önce ne olduğunu anlama

-Destek olmak

-Eşzamanlı Geliştirme

-Otomasyon

## **What are SOLID principles? Give samples using Java**

S — Single-responsibility principle

ÖZET: Bir sınıf (nesne) yalnızca bir amaç uğruna değiştirilebilir, o da o sınıfa yüklenen sorumluluktur, yani bir sınıfın(fonksiyona da indirgenebilir) yapması gereken yalnızca bir işi olması gerekir.

O — Open-closed principle

ÖZET: Bir sınıf ya da fonksiyon halihazırda var olan özellikleri korumalı ve değişikliğe izin vermemelidir. Yani davranışını değiştirmiyor olmalı ve yeni özellikler kazanabiliyor olmalıdır.

L — Liskov substitution principle

ÖZET: Kodlarımızda herhangi bir değişiklik yapmaya gerek duymadan alt sınıfları, türedikleri(üst) sınıfların yerine kullanabilmeliyiz.

I — Interface segregation principle

ÖZET: Sorumlulukların hepsini tek bir arayüze toplamak yerine daha özelleştirilmiş birden fazla arayüz oluşturmalıyız.

D — Dependency Inversion Principle

ÖZET: Sınıflar arası bağımlılıklar olabildiğince az olmalıdır özellikle üst seviye sınıflar alt seviye sınıflara bağımlı olmamalıdır.


## **What is RAD model**

Hızlı uygulama geliştirme olarak türkçeye çevirebileceğimiz Rapid Application Development(RAD), yazılım geliştirme süreçlerine ilişkin uygulanan ve bu süreçlerin mümkün olduğunca hızlı bir şekilde gerçekleştirilmesini destekleyen yöntemler bütünüdür. Süreçlerin hızlı bir şekilde tamamlanmasını destekler nitelikteki bu metodun ana hedefleri; yüksek hız, yüksek kalite ve düşük maliyet olarak açıklanabilir. Yazılım geliştirme süreçlerinin kalitesinin yükseltilmesine ve maliyetlerin azaltılmasına yönelik bu metodoloji zamandan da büyük tasarruf sağlaması itibariyle güncel bir yöntem durumundadır.

What is Spring Boot Starter. How is it used.

Starterlar kısaca uygulamanıza ekleyebileceğiniz bir dizi bağımlılık tanımlayıcısıdır. Sizi kullanmak istediğiniz teknolojilerin her biri için arama yapıp teker teker bağımlılık olarak ekleme zahmetinden kurtarır. Starterlar sayesinde ihtiyacınız olan Spring ve ilgili teknolojileri kolayca uygulamanıza ekleyebilirsiniz. 

Örnek olarak Spring ve JPA kullanmak istiyorsanız spring-boot-starter-data-jpa bağımlılığını projenize eklemeniz yeterli olacaktır.

## **What are the Spring Boot annotations**


Temel Spring Boot Anotasyonları

•  @Bean - Bir metodun Spring tarafından yönetilen bir Bean ürettiğini belirtir

• @Service - Belirtilen sınıfın bir servis sınıfı olduğunu belirtir.

• @Repository - Veritabanı işlemlerini gerçekleştirme yeteneği olan yapıldığı repository sınıfını belirtir.

• @Configuration - Bean tanımlamaları gibi tanımlamalar için bir Bean sınıfı olduğunu belirtir

• @Controller - Requestleri yakalayabilme yeteneği olan bir web controller sınıfını belirtir.

• @RequestMapping - controller sınıfının handle ettiği HTTP Requestlerin path eşleştirmesini yapar

• @Autowired - Constructor, Değişken yada setter metodlar için dependency injection işlemi gerçekleştirir

• @SpringBootApplication - Spring Boot autoconfiguration ve component taramasını aktif eder.


## **What is Spring Boot dependecy management**

Bağımlılık Yönetiminin Önemi

 İlgili Spring-Boot sürümüne göre gerekli tüm bağımlılıkları tek bir yerde belirlemeye izin verir.

 Spring-Boot sürümünü belirtebilir veya değiştirebilirsiniz.  Spring-Boot sürümlerini değiştirdiğinizde, bahsedilen (eklenen) bağımlılıkların tüm sürümleri otomatik olarak güncellenecektir.

 'Multi-Module' projeleri için faydalı olan farklı Spring-Boot kitaplıkları sürümlerinin çakışmalarını önleyebilirsiniz.

Spring-Boot'ta Bağımlılık Yönetiminin Çalışması

 Bağımlılık, uygulamamızda kullanabileceğimiz belirli işlevler sağlayan bir 'Kütüphane'den başka bir şey değildir.

 Spring-Boot'ta Bağımlılık Yönetimi ve Otomatik Yapılandırma aynı anda çalışır.

 Bağımlılıkları yönetmeyi bizim için son derece kolaylaştıran bu otomatik yapılandırmadır.

## **What is Spring Boot actuator**

Spring Boot Actuator, Spring Boot Framework'ün bir alt projesidir.  Çalışan herhangi bir uygulama hakkında operasyonel bilgileri ortaya çıkarmak için HTTP uç noktalarını kullanır.

 Bu kitaplığı kullanmanın temel yararı, üretime hazır uygulamalardan sistem durumu ve izleme ölçümleri almamızdır.  Ayrıca, metriklerin toplanması, trafiğin anlaşılması veya veritabanının durumunun bilinmesi Actuator ile son derece kolay hale gelir.






