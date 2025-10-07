> 📌 **YOUTUTUBE AÇIKLAMA VİDEOUSU LİNKİ:**
 https://youtu.be/ISII0y09R2E

# 🧩 NTP Homework 2 - Key Logging and E-mail Notification System

Bu proje, **Windows Form (C#)** kullanılarak geliştirilmiş bir uygulamadır.  
Amaç, klavyeden girilen tuşları dinleyerek bunları bir log hâlinde toplamak ve belirli bir sayıya ulaştığında bu veriyi e-posta olarak göndermektir.

> ⚠️ Bu proje tamamen **eğitim amaçlı**dır. Gerçek ortamlarda izinsiz tuş kaydı veya veri aktarımı yapmak **yasal değildir.**  
> Buradaki amaç, *keyboard hook*, *Windows API (user32.dll)* ve *e-posta API entegrasyonu* konularını öğrenmektir.

---
## 🚀 Proje Özeti

- **Kullanılan Diller / Teknolojiler**
  - C#
  - Windows Forms
  - .NET Framework
  - `DllImport` (user32.dll ile düşük seviye klavye yakalama)
  - [Brevo API (eski adıyla Sendinblue)](https://www.brevo.com) üzerinden e-posta gönderimi

- **Başlıca Özellikler**
  - Klavyedeki tüm karakterleri yakalama (Türkçe karakter desteği dahil)
  - Büyük/küçük harf algılama (`CapsLock` takibi)
  - Log biriktirme ve belirli uzunluğa ulaşınca e-posta gönderme
  - JSON formatında API isteği oluşturma (manuel olarak)
  - Hataları kullanıcıya `MessageBox` üzerinden bildirme

---

## ⚙️ Kurulum ve Çalıştırma

1. Proje klasörünü Visual Studio'da aç.
2. Gereken NuGet paketleri otomatik olarak yüklenecektir (örneğin `System.Net.Http`).
3. **API anahtarını** bir environment variable olarak ekle:
   - Windows arama çubuğuna “Environment Variables” yaz → aç
   - “User variables” kısmına yeni bir değişken ekle:
     ```
     Variable name: BREVO_API_KEY
     Variable value: senin_brevo_api_anahtarın
     ```
4. Programı başlat.
5. Tuşlara bastıkça log tutulur. Yaklaşık 50 karakterden sonra log içeriği e-posta olarak gönderilir.

---

## 📬 E-posta Yapısı

Gönderilen e-postada şu bilgiler bulunur:
- **Konu (Subject):** NTP Ödev outputu  
- **İçerik:** Klavyeden alınan karakterlerin sırası (örnek: `"Betül test yazdı -enter- 123"`)

---


## 👩‍💻 Geliştirici

**Betül Bilhan**  
Yazılım Mühendisliği Öğrencisi  


---

## ⚠️ Yasal Uyarı
Bu proje yalnızca **akademik / ödev** amaçlıdır.  
İzinsiz sistemlerde veya başka kullanıcıların bilgisayarlarında çalıştırılması **suç teşkil eder.**



