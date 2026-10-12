# kodasistanim
Proje Yazarı: Hayrettin ÇELİK

# Projenin Adı: Kod-Asistan v0.1

## Projenin Amacı: 
Kullanıcılara günlük işlerinde (hesaplama, selamlama vb.) yardımcı olacak bir dijital asistan tasarlamak.

## Projenin Hedefleri:
* **v1.0 Akıllı Menü:** Kullanıcının seçim yapmasını kolaylaştıran, dinamik ve gelişmiş bir kullanıcı arayüzü menüsü eklenecek.
* **v2.0 Veri Saklama:** Kullanıcı ayarlarını, girilen bilgileri ve geçmiş işlemleri hafızada tutacak bir veri tabanı entegrasyonu yapılacak.
* **v3.0 Gelişmiş Karar Mekanizması:** Yapay zekâ destekli hata ayıklama ve daha karmaşık mantıksal sorguların çözümü sağlanacak.

## Projenin Kapsamı:
Bu proje kapsamında, sistemin karar alma yeteneğini test etmek amacıyla tasarlanan **KRİTİK EŞİK** sözde kod mantığı şu şekildedir:

BAŞLA
GİRDİ bakiye
GİRDİ secilenUrun

urunFiyati = urunListesi(secilenUrun).fiyat
urunStogu = urunListesi(secilenUrun).stok

EĞER (urunStogu == 0) İSE
    ÇIKTI "Ürün tükendi! Paranız iade ediliyor."
    ÇIKTI bakiye
    
EĞER DEĞİLSE (bakiye >= urunFiyati) İSE
    paraUstu = bakiye - urunFiyati
    urunStogu = urunStogu - 1
    
    ÇIKTI secilenUrun + " Veriliyor."
    ÇIKTI paraUstu + " Para Üstü Veriliyor."
    ÇIKTI "Afiyet olsun!"
    
DEĞİLSE
    eksikTutar = urunFiyati - bakiye
    ÇIKTI "Yetersiz bakiye. Lütfen " + eksikTutar + " TL daha ekleyin."
    
BİTTİ
