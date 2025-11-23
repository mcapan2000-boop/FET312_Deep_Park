# FET312_Deep_Park
FET312 DERİN ÖĞRENME PROJESİ
Model Uygulama ve Test Süreci (Muhammet Emin Çapan)

Bu çalışmada, otopark doluluk tespiti probleminde araçların bütünsel şeklini daha iyi yakalayabilmek amacıyla filtre genişliği artırılmış (Wide Kernel) bir CNN modeli oluşturulmuş ve test edilmiştir. Uygulanan adımlar şöyledir:

Veri Ön İşleme: Veri seti ImageFolder yapısı ile yüklenmiş, tüm görüntüler 64x64 piksel boyutuna getirilmiş ve veri seti rastgele olarak %80 Eğitim (7199 görsel), %20 Test (1800 görsel) verisi şeklinde ayrılmıştır.

Model Mimarisi: Modelde, standart 3x3 filtreler yerine, ikinci konvolüsyon katmanında daha geniş bir alana (Receptive Field) odaklanabilen 5x5 boyutunda filtreler (kernels) kullanılmıştır. Aktivasyon fonksiyonu olarak ReLU ve boyut azaltma için Max Pooling tercih edilmiştir.

Eğitim Konfigürasyonu: Model, Adam optimizasyon algoritması (lr=0.001) ve sınıflandırma problemleri için uygun olan CrossEntropyLoss kayıp fonksiyonu ile derlenmiştir.

Test: Model 3 epoch (dönem) boyunca eğitilmiş, geniş filtrelerin sağladığı bütünsel algılama yeteneği sayesinde eğitim kaybı hızla düşmüş ve modelin test seti üzerinde %100.00 nihai doğruluk oranı elde edilmiştir.
