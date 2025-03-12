# machine_learning
machine_learning çalışmalarım
#1)
# Su Kalitesi Tahmini

## Proje Açıklaması

Bu proje, suyun içilebilir olup olmadığını tahmin etmek için makine öğrenmesi modellerini kullanmaktadır. Decision Tree ve Random Forest algoritmaları ile sınıflandırma işlemi gerçekleştirilmiştir.

## Kullanılan Kütüphaneler

Projede aşağıdaki Python kütüphaneleri kullanılmıştır:

- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `plotly`
- `missingno`
- `sklearn`

## Veri Seti

Proje, `water.csv` adlı veri setini kullanmaktadır. Veri setinde suyun içilebilir olup olmadığını belirleyen çeşitli kimyasal özellikler bulunmaktadır. **Potability** değişkeni, suyun içilebilir olup olmadığını belirleyen hedef değişkendir.

## Veri Analizi ve Temizleme

- Eksik veriler tespit edilerek ortalama değerler ile doldurulmuştur.
- `ph`, `Sulfate` ve `Trihalomethanes` sütunlarındaki eksik veriler, ilgili sütunun ortalama değeri ile doldurulmuştur.
- Verilerin korelasyon analizi yapılmış ve görselleştirilmiştir.

## Model Eğitimi

Projede iki farklı model kullanılmıştır:

1. **Decision Tree Classifier (Karar Ağacı)**
2. **Random Forest Classifier (Rastgele Orman)**

### Eğitim ve Test Verilerinin Hazırlanması

- Veriler `train_test_split` fonksiyonu ile eğitim ve test setlerine bölünmüştür (%70 eğitim, %30 test).
- Özellikler `MinMaxScaler` ile normalize edilmiştir.

### Model Optimizasyonu

- `RandomizedSearchCV` kullanılarak **Decision Tree** ve **Random Forest** modelleri için hiperparametre optimizasyonu yapılmıştır.

## Sonuçlar ve Değerlendirme

- **Precision Score** metriği kullanılarak model başarıları ölçülmüştür.
- **Confusion Matrix** ile tahminlerin doğruluğu analiz edilmiştir.

### En İyi Modeller ve Performansları

| Model | En İyi Parametreler | Başarı Skoru |
|--------|--------------------|--------------|
| **Random Forest (RF)** | `{'n_estimators': 100, 'max_features': 'sqrt', 'max_depth': 7}` | **0.7196** |
| **Decision Tree (DT)** | `{'min_samples_split': 2, 'max_features': 'log2', 'max_depth': 7}` | **0.6572** |

## Kullanım

Projeyi çalıştırmak için:

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install numpy pandas seaborn matplotlib plotly missingno scikit-learn
   ```
2. `water.csv` dosyasını proje dizinine yerleştirin.
3. `main.py` veya ilgili Python dosyasını çalıştırın.

##

