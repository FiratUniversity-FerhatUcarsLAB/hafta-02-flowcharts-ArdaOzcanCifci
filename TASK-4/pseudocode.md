BAŞLA

&nbsp; İSTE "Öğrenci No ve Şifre giriniz"

&nbsp; OKU ogr\_no, sifre

&nbsp; 

&nbsp; EĞER kimlik\_dogrulama BAŞARILI İSE

&nbsp;   GÖRÜNTÜLE "Açılan Dersler Listesi"

&nbsp;   

&nbsp;   DÖNGÜ (kullanıcı 'kaydı tamamla' diyene kadar)

&nbsp;     İSTE "Eklemek istediğiniz dersin kodunu giriniz"

&nbsp;     OKU ders\_kodu

&nbsp;     

&nbsp;     KONTROL\_1 = Ön koşul dersleri alınmış mı?

&nbsp;     KONTROL\_2 = Derste kontenjan var mı?

&nbsp;     KONTROL\_3 = Ders programında çakışma var mı?

&nbsp;     

&nbsp;     EĞER KONTROL\_1 VE KONTROL\_2 VE KONTROL\_3 DOĞRU İSE

&nbsp;       İŞLEM Dersi geçici listeye ekle

&nbsp;       GÖRÜNTÜLE ders\_kodu, "başarıyla eklendi."

&nbsp;     DEĞİLSE

&nbsp;       GÖRÜNTÜLE "Ders eklenemedi. Sebepler:", KONTROL\_SONUÇLARI

&nbsp;     SON-EĞER

&nbsp;     

&nbsp;     İSTE "Başka ders eklemek istiyor musunuz? (E/H)"

&nbsp;     OKU devam\_mi

&nbsp;     EĞER devam\_mi = 'H' İSE

&nbsp;       DÖNGÜDEN ÇIK

&nbsp;     SON-EĞER

&nbsp;   SON-DÖNGÜ

&nbsp;   

&nbsp;   GÖRÜNTÜLE "Seçilen Dersler:", gecici\_liste

&nbsp;   İŞLEM Kaydı onayla ve veritabanına işle

&nbsp;   GÖRÜNTÜLE "Ders kaydınız başarıyla tamamlandı."

&nbsp;   

&nbsp; DEĞİLSE

&nbsp;   GÖRÜNTÜLE "Hatalı öğrenci no veya şifre."

&nbsp; SON-EĞER

SONLANDIR

