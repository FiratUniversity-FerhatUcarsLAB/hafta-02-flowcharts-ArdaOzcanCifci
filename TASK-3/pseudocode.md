BAŞLA

&nbsp; GÖRÜNTÜLE "Hastane Randevu Sistemine Hoş Geldiniz"

&nbsp; GÖRÜNTÜLE "Lütfen bir poliklinik seçiniz:"

&nbsp; // Poliklinikler listelenir

&nbsp; OKU secilen\_poliklinik

&nbsp; 

&nbsp; GÖRÜNTÜLE "Lütfen bir doktor seçiniz:"

&nbsp; // Seçilen poliklinikteki doktorlar listelenir

&nbsp; OKU secilen\_doktor

&nbsp; 

&nbsp; GÖRÜNTÜLE "Uygun randevu saatleri:"

&nbsp; // Seçilen doktorun takvimi gösterilir

&nbsp; OKU secilen\_saat

&nbsp; 

&nbsp; EĞER secilen\_saat MÜSAİT İSE

&nbsp;   İSTE "Adınızı ve TC Kimlik Numaranızı giriniz"

&nbsp;   OKU hasta\_adi, hasta\_tc

&nbsp;   

&nbsp;   İŞLEM Randevuyu kaydet (hasta\_adi, secilen\_doktor, secilen\_saat)

&nbsp;   İŞLEM secilen\_saat'i DOLU olarak işaretle

&nbsp;   GÖRÜNTÜLE "Randevunuz başarıyla oluşturulmuştur."

&nbsp;   GÖRÜNTÜLE "Tarih:", GÜNCEL\_TARİH, "Saat:", secilen\_saat

&nbsp; DEĞİLSE

&nbsp;   GÖRÜNTÜLE "Üzgünüz, seçtiğiniz saat dolu."

&nbsp;   GÖRÜNTÜLE "Lütfen başka bir saat seçiniz."

&nbsp; SON-EĞER

SONLANDIR

