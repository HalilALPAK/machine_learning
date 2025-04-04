# Diyabet Tahmin Modeli

Bu proje, çeşitli makine öğrenmesi algoritmaları kullanarak bireylerin diyabet hastası olup olmadığını tahmin etmeyi amaçlamaktadır. Proje kapsamında **Lojistik Regresyon, Karar Ağacı, K-En Yakın Komşu, Naive Bayes, Destek Vektör Makineleri, AdaBoost, Rastgele Orman ve Gradyan Artırma** gibi birçok farklı model test edilmiştir.

## 📊 Kullanılan Veri Seti

Pima Indian Diabetes veri seti kullanılmıştır. Bu veri seti aşağıdaki sütunları içerir:

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome (Hedef değişken: 0 = Diyabet değil, 1 = Diyabet)

## 🧠 Kullanılan Modeller ve Performans Sonuçları

Aşağıda kullanılan modeller, en iyi hiperparametre değerleri ve elde edilen en iyi doğruluk (accuracy) skorları yer almaktadır:

| Model                       | En İyi Parametreler                                 | Doğruluk   |
| --------------------------- | --------------------------------------------------- | ---------- |
| **Lojistik Regresyon (lr)** | `C=0.1, solver=lbfgs`                               | **0.7821** |
| **Karar Ağacı (DT)**        | `max_depth=5, min_samples_split=10`                 | 0.7486     |
| **KNN**                     | `n_neighbors=5, metric=euclidean`                   | 0.7691     |
| **Naive Bayes (NB)**        | `var_smoothing=1e-09`                               | 0.7485     |
| **SVM**                     | `C=0.1, kernel=linear`                              | **0.7858** |
| **AdaBoost (AdaB)**         | `learning_rate=1, n_estimators=200`                 | 0.7635     |
| **Random Forest (RF)**      | `max_depth=20, n_estimators=300`                    | 0.7728     |
| **Gradient Boosting (GBM)** | `learning_rate=0.05, max_depth=3, n_estimators=100` | **0.7839** |

> 🔍 **En iyi doğruluk skoru**: `Gradient Boosting Model` ile **0.7839**

## ⚙️ Kurulum ve Kullanım

1. Gerekli kütüphaneleri yükleyin:

```bash
pip install numpy pandas matplotlib scikit-learn
```
