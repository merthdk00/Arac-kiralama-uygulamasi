# arac-kiralama-sistemi

## Proje Amacı

Bu projenin amacı, bir araç kiralama şirketinin temel envanter, müşteri ve kiralama işlemlerini dijital ortamda yönetebilen basit bir araç kiralama otomasyon sistemi geliştirmektir. Sistem sayesinde araç ekleme, müşteri oluşturma, araç kiralama, araç iade etme, dinamik ücret hesaplama ve kiralama geçmişini görüntüleme gibi operasyonel işlemler gerçekleştirilebilmektedir.

### Kullanılan Teknolojiler

#### Python Programlama Dili

* Nesne Yönelimli Programlama (OOP)
* `json` kütüphanesi (verileri dosyaya kaydetmek ve yüklemek için)
* `datetime` kütüphanesi (kiralama ve iade tarihlerini işlemek için)
* Konsol tabanlı kullanıcı arayüzü

---

### Kullanılan OOP Yapıları

#### Sınıf (Class) Yapıları

* `Araç`
* `Otomobil`
* `Motosiklet`
* `Müşteri`
* `KiralamaSistemi` sınıfları kullanılmıştır.

#### Kalıtım (Inheritance)

`Otomobil` ve `Motosiklet` sınıfları, `Araç` sınıfından türetilmiştir. Üst sınıfın ortak özellikleri (plaka, marka, model, yıl, fiyat) miras alınarak kod tekrarı önlenmiştir.

#### Kapsülleme (Encapsulation) & Durum Yönetimi

Araçların müsaitlik durumları (`müsait = True/False`) ve müşterilerin aktif kiralama bilgileri nesne özellikleri (attributes) olarak sınırlandırılmış ve sistem metodları aracılığıyla güvenli bir şekilde güncellenmektedir.

#### Çok Biçimlilik (Polymorphism)

Araç türleri ortak `Araç` yapısını kullansa da, `kiralama_ücretini_hesapla` metodu nesne türüne göre (Otomobil için %10 ek ücret, Motosiklet için %10 indirim) farklı özellikler gösterebilmektedir.

#### Metot Kullanımı

Kiralama, iade, listeleme ve ücret hesaplama gibi tüm operasyonel işlemler sınıf metotları aracılığıyla gerçekleştirilmiştir.

---

## Proje Özellikleri

* Yeni araç ekleme (Otomobil veya Motosiklet seçeneğiyle)
* Yeni müşteri kaydı oluşturma
* Tüm araçları ve sadece o an müsait olan araçları listeleme
* Tarih doğrulamalı araç kiralama işlemleri
* Gün bazlı dinamik ücret hesaplamalı araç iade işlemleri
* Müşteri bazlı kiralama geçmişini listeleme
* Kiralama ücretini simüle etme (bilgi amaçlı hesaplama)
* Verileri JSON formatında dosyaya kaydetme ve tekrar yükleme
