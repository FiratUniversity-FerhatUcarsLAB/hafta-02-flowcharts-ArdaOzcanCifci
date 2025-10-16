BAŞLA

&nbsp; GÖRÜNTÜLE "Hoş Geldiniz"

&nbsp; İSTE "Kartınızı takınız"

&nbsp; OKU kart\_bilgisi

&nbsp; 

&nbsp; İSTE "Lütfen 4 haneli PIN kodunuzu giriniz"

&nbsp; OKU girilen\_pin

&nbsp; 

&nbsp; EĞER girilen\_pin DOĞRU İSE

&nbsp;   GÖRÜNTÜLE "1. Para Çekme\\n2. Bakiye Sorgulama\\n3. Çıkış"

&nbsp;   OKU secim

&nbsp;   

&nbsp;   EĞER secim = 1 İSE

&nbsp;     İSTE "Çekmek istediğiniz tutarı giriniz"

&nbsp;     OKU cekilecek\_tutar

&nbsp;     

&nbsp;     EĞER hesap\_bakiyesi >= cekilecek\_tutar İSE

&nbsp;       İŞLEM Parayı ver

&nbsp;       hesap\_bakiyesi = hesap\_bakiyesi - cekilecek\_tutar

&nbsp;       GÖRÜNTÜLE "İşlem başarılı. Kartınızı alabilirsiniz."

&nbsp;     DEĞİLSE

&nbsp;       GÖRÜNTÜLE "Yetersiz bakiye."

&nbsp;     SON-EĞER

&nbsp;     

&nbsp;   DEĞİLSE EĞER secim = 2 İSE

&nbsp;     GÖRÜNTÜLE "Hesap Bakiyeniz: ", hesap\_bakiyesi

&nbsp;   DEĞİLSE

&nbsp;     GÖRÜNTÜLE "Çıkış yapılıyor."

&nbsp;   SON-EĞER

&nbsp;   

&nbsp; DEĞİLSE

&nbsp;   GÖRÜNTÜLE "Hatalı PIN. Kartınız iade ediliyor."

&nbsp; SON-EĞER

&nbsp; 

SONLANDIR

