# 🩺 Göğüs Röntgenlerinden Derin Öğrenme ile Pnömoni Tespiti

Bu proje, göğüs röntgeni (Chest X-Ray) görüntülerinden **Pnömoni (Zatürre)** hastalığını otomatik olarak tespit etmek amacıyla **Derin Öğrenme** yöntemlerini kullanmaktadır. Çalışmada bir adet **özel (custom) CNN modeli** geliştirilmiş ve model performansı çeşitli değerlendirme metrikleri ile analiz edilmiştir.

---

## 📌 Proje Bilgileri
- **Ders:** Derin Öğrenmeye Giriş
- **Proje Türü:** Akademik / Üniversite Projesi
- **Konu:** Tıbbi Görüntü Analizi
- **Amaç:** Göğüs röntgeni görüntülerinden pnömoni tespiti yapmak

---

## 🎯 Projenin Amacı
Bu projenin temel amacı, derin öğrenme tabanlı bir evrişimsel sinir ağı (CNN) modeli kullanarak göğüs röntgeni görüntülerinden pnömoni hastalığını otomatik olarak tespit etmektir. Proje kapsamında geliştirilen modelin doğruluğu ve başarımı akademik ölçütler kullanılarak değerlendirilmiştir.

---

## 🗂️ Kullanılan Veri Seti
- **Kaynak:** Kaggle – Chest X-Ray (Pneumonia) Dataset
- **Sınıflar:**
  - Normal
  - Pneumonia
- **Görüntü Türü:** Gri tonlamalı (Grayscale) göğüs röntgenleri

---

## ⚙️ Veri Ön İşleme (Preprocessing)
Veri ön işleme süreci aşağıdaki adımlardan oluşmaktadır:

- Görüntülerin gri tonlamaya dönüştürülmesi
- Görüntülerin 180 × 180 boyutuna yeniden ölçeklendirilmesi
- Piksel değerlerinin normalize edilmesi ([0–255] → [0–1])
- Verilerin eğitim, doğrulama ve test setlerine ayrılması

### 📊 Veri Dağılımı
- `X_train.shape`: (4215, 180, 180, 1)
- `y_train.shape`: (4215,)
- `X_val.shape`: (469, 180, 180, 1)
- `y_val.shape`: (469,)
- `X_test.shape`: (1172, 180, 180, 1)
- `y_test.shape`: (1172,)

---

## 🧠 Model Geliştirme
Projede **özel olarak tasarlanmış bir Convolutional Neural Network (CNN)** modeli kullanılmıştır.

### Model Mimarisi
- 3 adet Convolution + MaxPooling katmanı
- 1 adet Fully Connected (Dense) katman
- Dropout katmanı ile overfitting önleme
- Sigmoid aktivasyonlu çıkış katmanı

Model, ikili sınıflandırma problemi için eğitilmiştir (Normal / Pneumonia).

---

## 🏋️ Model Eğitimi
- Optimizer: Adam
- Kayıp Fonksiyonu: Binary Crossentropy
- Epoch Sayısı: 20
- Eğitim süresi yaklaşık **1 saat 45 dakika** sürmüştür.

---

## 📈 Model Değerlendirme
Eğitilen model test verisi üzerinde değerlendirilmiş ve aşağıdaki sonuçlar elde edilmiştir:

- **Doğruluk (Accuracy): %95.6**
- Yüksek sınıflandırma başarımı
- Dengeli performans

Model başarımı accuracy metriği üzerinden analiz edilmiştir.

---

## 📁 Proje Dosya Yapısı
```
├── pneumonia_detection.ipynb   # Tüm kodların bulunduğu ana notebook
├── presentation.pdf            # Proje sunum dosyası
└── README.md                   # Proje açıklama dosyası
```

---

## 🚀 Çalıştırma Talimatları
1. `pneumonia_detection.ipynb` dosyasını açın
2. Gerekli Python kütüphanelerini yükleyin
3. Notebook hücrelerini sırasıyla çalıştırın
4. Model eğitimi ve değerlendirme sonuçlarını inceleyin

---

## 📌 Sonuç
Bu çalışma, derin öğrenme yöntemlerinin göğüs röntgeni görüntülerinden pnömoni tespitinde etkili olduğunu göstermektedir. Geliştirilen CNN modeli, yüksek doğruluk oranı ile başarılı sonuçlar üretmiştir.

---

## 🙏 Teşekkürler
Bu proje, akademik amaçlarla geliştirilmiştir ve derin öğrenmenin tıbbi görüntü analizi alanındaki uygulamalarını incelemeyi hedeflemektedir.

