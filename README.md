# Sadece Yapay Sinir Ağı Kullanarak Balık Sınıflandırma

## Proje Genel Bakış

Bu proje, farklı balık türlerini Yapay Sinir Ağları (ANN) kullanarak sınıflandırmayı amaçlamaktadır. Proje, 9 farklı balık türüne ait 9,000 görüntü içeren bir veri seti kullanmaktadır. Hedef, balıkların görüntülerine dayanarak türlerini doğru bir şekilde tahmin edebilen bir derin öğrenme modeli oluşturmaktır.

## Veri Seti

- **9 balık türü**.
- Her tür için **1,000 görüntü**, toplamda **9,000 görüntü**.
- Görüntüler **256x256 piksel** boyutunda ve RGB formatındadır.

Veri seti, **normalizasyon** ve **one-hot encoding** gibi ön işleme teknikleri kullanılarak hazırlanmıştır.


## Model Mimarisi

- Giriş Katmanı: 256x256x3
- Gizli Katman 1: 512 birim, ReLU aktivasyonu, Batch Normalization ve Dropout (0.5)
- Gizli Katman 2: 256 birim, ReLU aktivasyonu, Batch Normalization ve Dropout (0.5)
- Gizli Katman 3: 128 birim, ReLU aktivasyonu, Batch Normalization ve Dropout (0.5)
- Çıkış Katmanı: 9 birim, Softmax aktivasyonu

## Sonuçlar

- **Test Loss**: 0.3109
- **Test Accuracy**: %89.67
