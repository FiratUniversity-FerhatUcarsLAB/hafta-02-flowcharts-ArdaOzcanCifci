BAŞLA

&nbsp; TANIMLA sepet = boş liste

&nbsp; TANIMLA toplam\_tutar = 0

&nbsp; 

&nbsp; DÖNGÜ (kullanıcı 'ödeme' seçene kadar)

&nbsp;   GÖRÜNTÜLE "1. Ürün Ekle\\n2. Sepeti Göster\\n3. Ödeme Yap"

&nbsp;   OKU kullanici\_secimi

&nbsp;   

&nbsp;   EĞER kullanici\_secimi = 1 İSE

&nbsp;     İSTE "Eklenecek ürün adı ve fiyatını giriniz"

&nbsp;     OKU urun\_adi, urun\_fiyati

&nbsp;     EKLE {urun\_adi, urun\_fiyati} listesine EKLE

&nbsp;     GÖRÜNTÜLE urun\_adi, "sepete eklendi."

&nbsp;   DEĞİLSE EĞER kullanici\_secimi = 2 İSE

&nbsp;     GÖRÜNTÜLE "Sepetinizdeki Ürünler:", sepet

&nbsp;   DEĞİLSE EĞER kullanici\_secimi = 3 İSE

&nbsp;     DÖNGÜDEN ÇIK

&nbsp;   SON-EĞER

&nbsp; SON-DÖNGÜ

&nbsp; 

&nbsp; HER urun İÇİN sepet İÇİNDE

&nbsp;   toplam\_tutar = toplam\_tutar + urun.fiyati

&nbsp; SON-DÖNGÜ

&nbsp; 

&nbsp; EĞER toplam\_tutar >= 500 İSE

&nbsp;   kargo\_ucreti = 0

&nbsp;   GÖRÜNTÜLE "Kargonuz ücretsiz!"

&nbsp; DEĞİLSE

&nbsp;   kargo\_ucreti = 30

&nbsp; SON-EĞER

&nbsp; 

&nbsp; genel\_toplam = toplam\_tutar + kargo\_ucreti

&nbsp; GÖRÜNTÜLE "Sepet Toplamı:", toplam\_tutar

&nbsp; GÖRÜNTÜLE "Kargo Ücreti:", kargo\_ucreti

&nbsp; GÖRÜNTÜLE "Ödenecek Tutar:", genel\_toplam

SONLANDIR

