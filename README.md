# Titanic KNN Classifier

Bu proje, Titanic gemisinde hayatta kalan yolcuları tahmin etmek için K-Nearest Neighbors (KNN) algoritmasını kullanmaktadır. Titanic yolcu verileri üzerinde, yolcuların hayatta kalıp kalmadığını tahmin etmek amacıyla çeşitli özellikler (yaş, cinsiyet, sınıf, vb.) kullanılmıştır.

## Proje Özeti

Bu projede, Titanic yolcu veri setini kullanarak, hayatta kalma tahmini yapmak amacıyla bir KNN sınıflandırma modeli oluşturulmuştur. Veriler, yolcuların çeşitli özelliklerini içerir ve model, bu özelliklere dayanarak her bir yolcunun hayatta kalıp kalmadığını tahmin eder.

## Kullanılan Teknolojiler

- **Python**: Proje, Python programlama dili ile yazılmıştır.
- **Pandas**: Veri analizi ve manipülasyonu için kullanılmıştır.
- **Scikit-learn**: KNN algoritması ve model değerlendirme metrikleri için kullanılmıştır.
- **Matplotlib / Seaborn**: Veri görselleştirme araçlarıdır.
- **Git**: Versiyon kontrolü için kullanılmıştır.

## Veri Seti

Titanic veri seti, Titanic felaketi sırasında gemide bulunan yolcuların verilerini içermektedir. Veriler, yolcuların hayatta kalma durumları (Survived), yolcu sınıfı (Pclass), yaş (Age), cinsiyet (Sex) gibi bilgileri içerir.

Veri seti, şu sütunları içerir:

- `PassengerId`: Yolcu kimliği
- `Survived`: Hayatta kalma durumu (0 = Hayatını kaybetti, 1 = Hayatta kaldı)
- `Pclass`: Yolcu sınıfı (1 = 1. sınıf, 2 = 2. sınıf, 3 = 3. sınıf)
- `Name`: Yolcunun adı
- `Sex`: Cinsiyet
- `Age`: Yaş
- `SibSp`: Sibling/Spouse (Yolcunun kardeşi veya eşinin sayısı)
- `Parch`: Parent/Child (Yolcunun ebeveyni veya çocuğunun sayısı)
- `Ticket`: Bilet numarası
- `Fare`: Bilet ücreti
- `Cabin`: Kabin numarası
- `Embarked`: Yolcunun bindiği liman (C = Cherbourg, Q = Queenstown, S = Southampton)

## Model Oluşturma

Model, **K-Nearest Neighbors (KNN)** algoritmasını kullanarak oluşturulmuştur. Bu algoritma, verilerin sınıflandırılmasında yakınlık (distance) ölçümlerini kullanır.

### Adımlar:

1. **Veri Hazırlığı**:
   - Eksik değerler doldurulmuş ve kategorik veriler sayısal verilere dönüştürülmüştür.
   - Özellikler (features) ve hedef değişken (target) ayrılmıştır.

2. **Model Eğitimi**:
   - Veriler eğitim ve test setlerine bölünmüştür.
   - KNN sınıflandırıcısı kullanılarak model eğitilmiştir.

3. **Model Değerlendirmesi**:
   - Modelin doğruluğu, **confusion matrix** ve **accuracy score** kullanılarak değerlendirilmiştir.

## Kullanım

Projeyi kullanmak için aşağıdaki adımları takip edebilirsiniz:

1. **Proje Dosyasını Klonlayın**:
   ```bash
   git clone https://github.com/mehtaapxkrkmz/titanic-knn.git

  ## Sonuçlar

Modelin doğruluk oranı oldukça yüksek olup, Titanic yolcularının hayatta kalıp kalmayacağını tahmin etme görevinde başarılı olmuştur. Modelin değerlendirilmesinde elde edilen **confusion matrix** ve **accuracy score** sonuçları şu şekildedir:

- **50** yolcu doğru şekilde **hayatta kaldı** (True Positive).
- **32** yolcu doğru şekilde **hayatını kaybetti** (True Negative).
- **0** yolcu yanlış bir şekilde **hayatta kaldı** (False Positive).
- **2** yolcu yanlış bir şekilde **hayatını kaybetti** (False Negative).

Model, genellikle doğru tahminler yaparak başarılı bir performans sergilemiştir. Bu sonuçlar, KNN algoritmasının Titanic yolcularının hayatta kalma durumlarını tahmin etmede etkili bir araç olduğunu göstermektedir.

## Lisans

Bu proje, [MIT Lisansı](https://opensource.org/licenses/MIT) altında lisanslanmıştır.  
MIT Lisansı, yazılımın serbestçe kullanılmasına, değiştirilmesine ve dağıtılmasına izin verir, ancak yazılımın kullanımına dair herhangi bir garanti verilmez.
