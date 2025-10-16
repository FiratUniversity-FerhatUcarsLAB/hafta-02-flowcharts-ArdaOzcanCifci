BAŞLA
  TANIMLA sistem_durumu = "DEVRE DIŞI"
  
  SÜREKLİ DÖNGÜ
    OKU kullanici_komutu // (ör: 'KUR', 'KAPAT')
    
    EĞER kullanici_komutu = 'KUR' İSE
      sistem_durumu = "KURULU"
      GÖRÜNTÜLE "Sistem kuruldu."
    DEĞİLSE EĞER kullanici_komutu = 'KAPAT' İSE
      sistem_durumu = "DEVRE DIŞI"
      GÖRÜNTÜLE "Sistem devre dışı bırakıldı."
    SON-EĞER
    
    OKU sensor_verileri // (kapı, pencere, hareket)
    
    EĞER sistem_durumu = "KURULU" VE herhangi_bir_sensor_tetiklendi İSE
      İŞLEM Alarmı çal
      İŞLEM Kullanıcıya bildirim gönder ('Tehlike: Hareket algılandı!')
      sistem_durumu = "ALARM" // Tekrar tekrar alarm çalmaması için
    SON-EĞER
    
    BEKLE 1 saniye // Döngü çok hızlı çalışmasın diye
  SON-DÖNGÜ
SONLANDIR