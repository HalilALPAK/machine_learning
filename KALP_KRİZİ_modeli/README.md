# Kalp Krizi Tahmini - README

## Proje Açıklaması

Bu proje, kalp krizi riskini tahmin etmek için makine öğrenmesi modellerini kullanmaktadır. Logistic Regression, Decision Tree ve Random Forest algoritmaları ile sınıflandırma işlemi gerçekleştirilmiştir.

## Kullanılan Kütüphaneler

Projede aşağıdaki Python kütüphaneleri kullanılmıştır:

- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `sklearn`

## Veri Seti

Proje, `heart.csv` adlı veri setini kullanmaktadır. Veri seti, kalp hastalığı risk faktörlerini içeren çeşitli tıbbi ölçümleri içermektedir. **Hedef değişken**, hastanın kalp hastalığı olup olmadığını gösterir.

## Veri Analizi ve Temizleme

- Eksik veri olup olmadığı kontrol edilmiştir.
- Verilerin korelasyon analizi yapılmış ve görselleştirilmiştir.
- `StandardScaler` kullanılarak özellikler ölçeklendirilmiştir.

## Model Eğitimi

Projede üç farklı model kullanılmıştır:

1. **Logistic Regression (Lojistik Regresyon)**
2. **Decision Tree Classifier (Karar Ağacı)**
3. **Random Forest Classifier (Rastgele Orman)**

### Eğitim ve Test Verilerinin Hazırlanması

- Veriler `train_test_split` fonksiyonu ile eğitim ve test setlerine bölünmüştür (%70 eğitim, %30 test).
- Özellikler `StandardScaler` ile ölçeklendirilmiştir.

### Model Optimizasyonu

- **Logistic Regression** için `GridSearchCV` ile hiperparametre optimizasyonu yapılmıştır.
- **Decision Tree** ve **Random Forest** modelleri için `RandomizedSearchCV` ile en iyi parametreler belirlenmiştir.

## Sonuçlar ve Değerlendirme

- **Accuracy Score** ve **Precision Score** gibi metrikler kullanılarak model başarıları ölçülmüştür.
- **Confusion Matrix** ile tahminlerin doğruluğu analiz edilmiştir.

### En İyi Modeller ve Performansları

| Model | En İyi Parametreler | Başarı Skoru |
|--------|--------------------|--------------|
| **Logistic Regression (LR)** | `{'penalty': 'l2'}` | **0.8681** |
| **Random Forest (RF)** | `{'n_estimators': 50, 'max_features': 'sqrt', 'max_depth': 16}` | **0.8115** |
| **Decision Tree (DT)** | `{'min_samples_split': 2, 'max_features': 'log2', 'max_depth': 10}` | **0.7148** |

## Kullanım

Projeyi çalıştırmak için:

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install numpy pandas seaborn matplotlib scikit-learn
   ```
2. `heart.csv` dosyasını proje dizinine yerleştirin.
3. `main.py` veya ilgili Python dosyasını çalıştırın.

##

